# Setting up the Astarte Voyager Ingress

---
**IMPORTANT**: Due to changes in Voyager policies and to the
[announcement](https://blog.byte.builders/post/voyager-v2021.09.15/) that, starting from Dec 31st
2021, it will not possible to pull older Voyager docker images the Astarte Voyager Ingress is
deprecated and will be dropped in a future release (i.e.: `v1.1`). Please, consider using the NGINX
based drop-in replacement for Astarte called
[`AstarteDefaultIngress`](064-setup_astartedefaultingress.html).
---

Once your Cluster [is up and running](060-setup_cluster.html), to expose it to the outer world you
need to set up an Ingress. The current page focuses on the deployment of the
[Voyager](https://github.com/appscode/voyager) based AstarteVoyagerIngress. 

Of course, ensure you have installed [Voyager
Operator](https://voyagermesh.com/docs/v12.0.0/setup/install) before you begin.

## Creating an AstarteVoyagerIngress

Most information needed for exposing your Ingress have already been given in your main Astarte
resource. If your Kubernetes installation supports LoadBalancer ingresses (most managed ones do),
you should be able to get away with the most standard CR:

```yaml
apiVersion: api.astarte-platform.org/v1alpha1
kind: AstarteVoyagerIngress
metadata:
  name: example-minimal
  namespace: astarte
spec:
  # The Astarte Instance the Ingress will be attached to
  astarte: example-minimal
  api:
    exposeHousekeeping: true
  dashboard:
    ssl: true
    host: "dashboard.astarte.yourdomain.com" # When not specified, dashboard will be deployed in /dashboard in the API host.
  letsencrypt:
    use: true
    acmeEmail: info@yourdomain.com
    challengeProvider:
      dns:
        provider: digitalocean
        credentialSecretName: voyager-digitalocean
```

As you might see, there's only one very important thing to be noted: the `astarte` field must reference the name of an
existing Astarte installation in the same namespace, and the Ingress will be configured and attached to that instance.

## SSL and Certificates

Astarte heavily requires SSL in a number of interactions, even though this can be bypassed with `ssl: false`. If you
do not have any SSL Certificates for your domains, you can leverage Voyager's Let's Encrypt integration.
AstarteVoyagerIngress integrates directly with Voyager's native types, and you can follow along
[Voyager's Let's Encrypt guide](https://github.com/appscode/voyager/tree/master/docs/guides/certificate).
Simply set `letsencrypt.use` to `true`, and fill the `challengeProvider` with the right parameters.

## API Paths

`AstarteVoyagerIngress` deploys a well-known tree of APIs to the `host` you specified in the main `Astarte` resource.
In particular, assuming your API host was `api.astarte.yourdomain.com`:

* Housekeeping API base URL will be https://api.astarte.yourdomain.com/housekeeping/v1
* Realm Management API base URL will be https://api.astarte.yourdomain.com/realmmanagement/v1
* Pairing API base URL will be https://api.astarte.yourdomain.com/pairing/v1
* AppEngine API base URL will be https://api.astarte.yourdomain.com/appengine/v1

## Further customization

`AstarteVoyagerIngress` has a number of advanced options that can be used to accommodate needs of the most diverse
deployments. Consult the [CRD
Documentation](https://docs.astarte-platform.org/snapshot/astarte-kubernetes-operator/) to learn
more.
