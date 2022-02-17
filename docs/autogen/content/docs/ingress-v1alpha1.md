+++
title = "ingress.astarte-platform.org/v1alpha1"
type = "docs"
description = "Package v1alpha1 contains API Schema definitions for the ingress v1alpha1 API group"
+++
<p>Packages:</p>
<ul>
<li>
<a href="#ingress.astarte-platform.org%2fv1alpha1">ingress.astarte-platform.org/v1alpha1</a>
</li>
</ul>
<h2 id="ingress.astarte-platform.org/v1alpha1">ingress.astarte-platform.org/v1alpha1</h2>
<div>
<p>Package v1alpha1 contains API Schema definitions for the ingress v1alpha1 API group</p>
</div>
Resource Types:
<ul></ul>
<h3 id="ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngress">AstarteDefaultIngress
</h3>
<div>
<p>AstarteDefaultIngress is the Schema for the astartedefaultingresses API</p>
</div>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>metadata</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#objectmeta-v1-meta">
Kubernetes meta/v1.ObjectMeta
</a>
</em>
</td>
<td>
Refer to the Kubernetes API documentation for the fields of the
<code>metadata</code> field.
</td>
</tr>
<tr>
<td>
<code>spec</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressSpec">
AstarteDefaultIngressSpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>astarte</code><br/>
<em>
string
</em>
</td>
<td>
<p>The name of the Astarte instance served by the AstarteDefaultIngress.</p>
</td>
</tr>
<tr>
<td>
<code>ingressClass</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>In clusters with more than one instance of the Ingress-NGINX controller, all
instances of the controllers must be aware of which Ingress object they must serve.
The ingressClass field of a ingress object is the way to let the controller know about that.
Default: &ldquo;nginx&rdquo;.</p>
</td>
</tr>
<tr>
<td>
<code>api</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressAPISpec">
AstarteDefaultIngressAPISpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Define the desired state of the AstarteDefaultIngressAPISpec resource.</p>
</td>
</tr>
<tr>
<td>
<code>dashboard</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressDashboardSpec">
AstarteDefaultIngressDashboardSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Define the desired state of the AstarteDefaultIngressDashboardSpec resource.</p>
</td>
</tr>
<tr>
<td>
<code>broker</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressBrokerSpec">
AstarteDefaultIngressBrokerSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Define the desired state of the AstarteDefaultIngressBrokerSpec resource.</p>
</td>
</tr>
<tr>
<td>
<code>tlsSecret</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>The secret containing the TLS certificates and keys used to connect to Astarte. The secret
must be present in the namespace in which Astarte resides and it will be used to authenticate
requests for API and Dashboard. If specific configurations are required,
the TLSSecret can be overridden by setting the secret in any of AstarteDefaultIngressAPISpec
and AstarteDefaultIngressDashboardSpec.</p>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressStatus">
AstarteDefaultIngressStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressAPISpec">AstarteDefaultIngressAPISpec
</h3>
<p>
(<em>Appears on:</em><a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressSpec">AstarteDefaultIngressSpec</a>)
</p>
<div>
<p>AstarteDefaultIngressAPISpec defines how the Astarte APIs are served.</p>
</div>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>deploy</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>When true, deploy the API ingress.</p>
</td>
</tr>
<tr>
<td>
<code>tlsSecret</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>The secret containing the TLS certificates and keys used to access the Astarte API. The secret
must be present in the namespace in which Astarte resides. If set, this secret overrides the TLSSecret
field contained in AstarteDefaultIngressSpec.</p>
</td>
</tr>
<tr>
<td>
<code>cors</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>When true, enable Cross-Origin Resource Sharing (CORS). Default: false.</p>
</td>
</tr>
<tr>
<td>
<code>exposeHousekeeping</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>When true, the housekeeping endpoint is publicly exposed. Default: true.</p>
</td>
</tr>
<tr>
<td>
<code>serveMetrics</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>When true, all /metrics endpoints for Astarte services will be served by the Ingress.
Beware this might be a security hole. You can control which IPs can access /metrics
with serveMetricsToSubnet. Default: false.</p>
</td>
</tr>
<tr>
<td>
<code>serveMetricsToSubnet</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>When specified and when serveMetrics is true, /metrics endpoints will be served only to IPs
in the provided subnet range. The subnet has to be compatible with the HAProxy
ACL src syntax (e.g.: &ldquo;10.0.0.0/16&rdquo;). Default: &ldquo;&rdquo;.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressBrokerSpec">AstarteDefaultIngressBrokerSpec
</h3>
<p>
(<em>Appears on:</em><a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressSpec">AstarteDefaultIngressSpec</a>)
</p>
<div>
<p>AstarteDefaultIngressBrokerSpec defines how the Astarte Broker is served.</p>
</div>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>deploy</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>When true, expose the Broker.</p>
</td>
</tr>
<tr>
<td>
<code>serviceType</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#servicetype-v1-core">
Kubernetes core/v1.ServiceType
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Set the type of service employed to expose the broker. Supported values are &ldquo;NodePort&rdquo; and &ldquo;LoadBalancer&rdquo;.
The AstarteDefaultIngress handles TLS termination at VerneMQ level and, as such, no TLSSecret is needed to
configure the broker service.
Default: &ldquo;LoadBalancer&rdquo;</p>
</td>
</tr>
<tr>
<td>
<code>loadBalancerIP</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Set the LoadBalancerIP if and only if the broker service is of type &ldquo;LoadBalancer&rdquo;. This feature depends on
whether the cloud provider supports specifying the LoadBalancerIP when a load balancer is created.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressDashboardSpec">AstarteDefaultIngressDashboardSpec
</h3>
<p>
(<em>Appears on:</em><a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressSpec">AstarteDefaultIngressSpec</a>)
</p>
<div>
<p>AstarteDefaultIngressDashboardSpec defines how the Astarte Dashboard is served.</p>
</div>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>deploy</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>When true, deploy the Ingress for the Dashboard.</p>
</td>
</tr>
<tr>
<td>
<code>ssl</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>When true, enable TLS authentication for the Dashboard.</p>
</td>
</tr>
<tr>
<td>
<code>host</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>The host handling requests addressed to the dashboard. When deploy is true and host is not set,
the dashboard will be exposed at the following URL: https://<astarte-base-url>/dashboard.</p>
</td>
</tr>
<tr>
<td>
<code>tlsSecret</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>The secret containing the TLS certificates and keys used to access the Astarte Dashboard. The secret
must be present in the namespace in which Astarte resides. If set, this secret overrides the TLSSecret
field contained in AstarteDefaultIngressSpec.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressSpec">AstarteDefaultIngressSpec
</h3>
<p>
(<em>Appears on:</em><a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngress">AstarteDefaultIngress</a>)
</p>
<div>
<p>AstarteDefaultIngressSpec defines the desired state of the AstarteDefaultIngress resource</p>
</div>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>astarte</code><br/>
<em>
string
</em>
</td>
<td>
<p>The name of the Astarte instance served by the AstarteDefaultIngress.</p>
</td>
</tr>
<tr>
<td>
<code>ingressClass</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>In clusters with more than one instance of the Ingress-NGINX controller, all
instances of the controllers must be aware of which Ingress object they must serve.
The ingressClass field of a ingress object is the way to let the controller know about that.
Default: &ldquo;nginx&rdquo;.</p>
</td>
</tr>
<tr>
<td>
<code>api</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressAPISpec">
AstarteDefaultIngressAPISpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Define the desired state of the AstarteDefaultIngressAPISpec resource.</p>
</td>
</tr>
<tr>
<td>
<code>dashboard</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressDashboardSpec">
AstarteDefaultIngressDashboardSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Define the desired state of the AstarteDefaultIngressDashboardSpec resource.</p>
</td>
</tr>
<tr>
<td>
<code>broker</code><br/>
<em>
<a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressBrokerSpec">
AstarteDefaultIngressBrokerSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Define the desired state of the AstarteDefaultIngressBrokerSpec resource.</p>
</td>
</tr>
<tr>
<td>
<code>tlsSecret</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>The secret containing the TLS certificates and keys used to connect to Astarte. The secret
must be present in the namespace in which Astarte resides and it will be used to authenticate
requests for API and Dashboard. If specific configurations are required,
the TLSSecret can be overridden by setting the secret in any of AstarteDefaultIngressAPISpec
and AstarteDefaultIngressDashboardSpec.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngressStatus">AstarteDefaultIngressStatus
</h3>
<p>
(<em>Appears on:</em><a href="#ingress.astarte-platform.org/v1alpha1.AstarteDefaultIngress">AstarteDefaultIngress</a>)
</p>
<div>
<p>AstarteDefaultIngressStatus defines the observed state of AstarteDefaultIngress</p>
</div>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<hr/>
<p><em>
Generated with <code>gen-crd-api-reference-docs</code>
on git commit <code>2725e75</code>.
</em></p>
