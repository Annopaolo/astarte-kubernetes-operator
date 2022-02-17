+++
title = "api.astarte-platform.org/v1alpha2"
type = "docs"
description = "Package v1alpha2 contains API Schema definitions for the api v1alpha2 API group"
+++
<p>Packages:</p>
<ul>
<li>
<a href="#api.astarte-platform.org%2fv1alpha2">api.astarte-platform.org/v1alpha2</a>
</li>
</ul>
<h2 id="api.astarte-platform.org/v1alpha2">api.astarte-platform.org/v1alpha2</h2>
<div>
<p>Package v1alpha2 contains API Schema definitions for the api v1alpha2 API group</p>
</div>
Resource Types:
<ul></ul>
<h3 id="api.astarte-platform.org/v1alpha2.Astarte">Astarte
</h3>
<div>
<p>Astarte is the Schema for the astartes API</p>
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
<a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">
AstarteSpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>version</code><br/>
<em>
string
</em>
</td>
<td>
<p>The Astarte Version for this Resource</p>
</td>
</tr>
<tr>
<td>
<code>imagePullPolicy</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#pullpolicy-v1-core">
Kubernetes core/v1.PullPolicy
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>imagePullSecrets</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
[]Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>distributionChannel</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>deploymentStrategy</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#deploymentstrategy-v1-apps">
Kubernetes apps/v1.DeploymentStrategy
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>features</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteFeatures">
AstarteFeatures
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>rbac</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>storageClassName</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>api</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteAPISpec">
AstarteAPISpec
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>rabbitmq</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQSpec">
AstarteRabbitMQSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>cassandra</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraSpec">
AstarteCassandraSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>vernemq</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVerneMQSpec">
AstarteVerneMQSpec
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>cfssl</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLSpec">
AstarteCFSSLSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>components</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">
AstarteComponentsSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>astarteSystemKeyspace</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteSystemKeyspaceSpec">
AstarteSystemKeyspaceSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>manualMaintenanceMode</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>ManualMaintenanceMode pauses all reconciliation activities but still computes the resource
status. It should be used only when the managed Astarte resources requires manual intervention
and the Operator cannot break out of the problem by itself. Do not set this field unless you
know exactly what you are doing.</p>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteStatus">
AstarteStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteAPISpec">AstarteAPISpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
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
<code>ssl</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
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
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteAppengineAPISpec">AstarteAppengineAPISpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">AstarteComponentsSpec</a>)
</p>
<div>
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
<code>AstarteGenericAPISpec</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericAPISpec">
AstarteGenericAPISpec
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericAPISpec</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>maxResultsLimit</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>roomEventsQueueName</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Configures the name of the Room Events queue. Should be configured only in installations with a highly
customized RabbitMQ. It is advised to leave empty unless you know exactly what you&rsquo;re doing.</p>
</td>
</tr>
<tr>
<td>
<code>roomEventsExchangeName</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Configures the name of the Room Events exchange. Should be configured only in installations with a highly
customized RabbitMQ. It is advised to leave empty unless you know exactly what you&rsquo;re doing.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningCAConstraintSpec">AstarteCFSSLCARootConfigSigningCAConstraintSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningDefaultSpec">AstarteCFSSLCARootConfigSigningDefaultSpec</a>)
</p>
<div>
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
<code>max_path_len</code><br/>
<em>
int
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>is_ca</code><br/>
<em>
bool
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>max_path_len_zero</code><br/>
<em>
bool
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningDefaultSpec">AstarteCFSSLCARootConfigSigningDefaultSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningSpec">AstarteCFSSLCARootConfigSigningSpec</a>)
</p>
<div>
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
<code>usages</code><br/>
<em>
[]string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>expiry</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>ca_constraint</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningCAConstraintSpec">
AstarteCFSSLCARootConfigSigningCAConstraintSpec
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningSpec">AstarteCFSSLCARootConfigSigningSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSpec">AstarteCFSSLCARootConfigSpec</a>)
</p>
<div>
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
<code>default</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningDefaultSpec">
AstarteCFSSLCARootConfigSigningDefaultSpec
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSpec">AstarteCFSSLCARootConfigSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLSpec">AstarteCFSSLSpec</a>)
</p>
<div>
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
<code>signing</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSigningSpec">
AstarteCFSSLCARootConfigSigningSpec
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCACASpec">AstarteCFSSLCSRRootCACASpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCASpec">AstarteCFSSLCSRRootCASpec</a>)
</p>
<div>
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
<code>expiry</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCAKeySpec">AstarteCFSSLCSRRootCAKeySpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCASpec">AstarteCFSSLCSRRootCASpec</a>)
</p>
<div>
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
<code>algo</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>size</code><br/>
<em>
int
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCANamesSpec">AstarteCFSSLCSRRootCANamesSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCASpec">AstarteCFSSLCSRRootCASpec</a>)
</p>
<div>
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
<code>C</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>L</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>O</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>OU</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>ST</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCASpec">AstarteCFSSLCSRRootCASpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLSpec">AstarteCFSSLSpec</a>)
</p>
<div>
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
<code>CN</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>key</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCAKeySpec">
AstarteCFSSLCSRRootCAKeySpec
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>names</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCANamesSpec">
[]AstarteCFSSLCSRRootCANamesSpec
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>ca</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCACASpec">
AstarteCFSSLCSRRootCACASpec
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLDBConfigSpec">AstarteCFSSLDBConfigSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLSpec">AstarteCFSSLSpec</a>)
</p>
<div>
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
<code>driver</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>dataSource</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCFSSLSpec">AstarteCFSSLSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
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
</td>
</tr>
<tr>
<td>
<code>url</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>caExpiry</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>caSecret</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>certificateExpiry</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>dbConfig</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLDBConfigSpec">
AstarteCFSSLDBConfigSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>resources</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Compute Resources for this Component.</p>
</td>
</tr>
<tr>
<td>
<code>version</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>image</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>storage</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstartePersistentStorageSpec">
AstartePersistentStorageSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>csrRootCa</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCSRRootCASpec">
AstarteCFSSLCSRRootCASpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>caRootConfig</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLCARootConfigSpec">
AstarteCFSSLCARootConfigSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCassandraConnectionSpec">AstarteCassandraConnectionSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraSpec">AstarteCassandraSpec</a>)
</p>
<div>
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
<code>poolSize</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>autodiscovery</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>sslConfiguration</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraSSLConfigurationSpec">
AstarteCassandraSSLConfigurationSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>secret</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.LoginCredentialsSecret">
LoginCredentialsSecret
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>username</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>password</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCassandraSSLConfigurationSpec">AstarteCassandraSSLConfigurationSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraConnectionSpec">AstarteCassandraConnectionSpec</a>)
</p>
<div>
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
<code>enabled</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>customCASecret</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>sni</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>customSNI</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteCassandraSpec">AstarteCassandraSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
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
<code>AstarteGenericClusteredResource</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericClusteredResource</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>nodes</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>maxHeapSize</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>heapNewSize</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>storage</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstartePersistentStorageSpec">
AstartePersistentStorageSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>connection</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraConnectionSpec">
AstarteCassandraConnectionSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteClusterHealth">AstarteClusterHealth
(<code>string</code> alias)</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteStatus">AstarteStatus</a>)
</p>
<div>
<p>AstarteClusterHealth represents the overall health of the cluster</p>
</div>
<table>
<thead>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody><tr><td><p>&#34;green&#34;</p></td>
<td><p>AstarteClusterHealthGreen means the cluster is healthy, up and running</p>
</td>
</tr><tr><td><p>&#34;red&#34;</p></td>
<td><p>AstarteClusterHealthRed means the cluster is experiencing serious malfunctions or is down</p>
</td>
</tr><tr><td><p>&#34;yellow&#34;</p></td>
<td><p>AstarteClusterHealthYellow means the cluster is experiencing downtimes related to a single service</p>
</td>
</tr></tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteComponent">AstarteComponent
(<code>string</code> alias)</h3>
<div>
<p>AstarteComponent describes an internal Astarte Component</p>
</div>
<table>
<thead>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody><tr><td><p>&#34;appengine_api&#34;</p></td>
<td><p>AppEngineAPI represents Astarte AppEngine API</p>
</td>
</tr><tr><td><p>&#34;dashboard&#34;</p></td>
<td><p>Dashboard represents Astarte Dashboard</p>
</td>
</tr><tr><td><p>&#34;data_updater_plant&#34;</p></td>
<td><p>DataUpdaterPlant represents Astarte Data Updater Plant</p>
</td>
</tr><tr><td><p>&#34;flow&#34;</p></td>
<td><p>FlowComponent represents Astarte Flow</p>
</td>
</tr><tr><td><p>&#34;housekeeping&#34;</p></td>
<td><p>Housekeeping represents Astarte Housekeeping</p>
</td>
</tr><tr><td><p>&#34;housekeeping_api&#34;</p></td>
<td><p>HousekeepingAPI represents Astarte Housekeeping API</p>
</td>
</tr><tr><td><p>&#34;pairing&#34;</p></td>
<td><p>Pairing represents Astarte Pairing</p>
</td>
</tr><tr><td><p>&#34;pairing_api&#34;</p></td>
<td><p>PairingAPI represents Astarte Pairing API</p>
</td>
</tr><tr><td><p>&#34;realm_management&#34;</p></td>
<td><p>RealmManagement represents Astarte Realm Management</p>
</td>
</tr><tr><td><p>&#34;realm_management_api&#34;</p></td>
<td><p>RealmManagementAPI represents Astarte Realm Management API</p>
</td>
</tr><tr><td><p>&#34;trigger_engine&#34;</p></td>
<td><p>TriggerEngine represents Astarte Trigger Engine</p>
</td>
</tr></tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">AstarteComponentsSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
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
<code>resources</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Compute Resources for this Component.</p>
</td>
</tr>
<tr>
<td>
<code>flow</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericAPISpec">
AstarteGenericAPISpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>housekeeping</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericComponentSpec">
AstarteGenericComponentSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>realmManagement</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericComponentSpec">
AstarteGenericComponentSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>pairing</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericComponentSpec">
AstarteGenericComponentSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>dataUpdaterPlant</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteDataUpdaterPlantSpec">
AstarteDataUpdaterPlantSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>appengineApi</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteAppengineAPISpec">
AstarteAppengineAPISpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>triggerEngine</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteTriggerEngineSpec">
AstarteTriggerEngineSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>dashboard</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteDashboardSpec">
AstarteDashboardSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteDashboardConfigAuthSpec">AstarteDashboardConfigAuthSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteDashboardConfigSpec">AstarteDashboardConfigSpec</a>)
</p>
<div>
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
<code>type</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>oauth_api_url</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteDashboardConfigSpec">AstarteDashboardConfigSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteDashboardSpec">AstarteDashboardSpec</a>)
</p>
<div>
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
<code>realmManagementApiUrl</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>appEngineApiUrl</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>pairingApiUrl</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>flowApiUrl</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>defaultRealm</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>defaultAuth</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>auth</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteDashboardConfigAuthSpec">
[]AstarteDashboardConfigAuthSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteDashboardSpec">AstarteDashboardSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">AstarteComponentsSpec</a>)
</p>
<div>
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
<code>AstarteGenericClusteredResource</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericClusteredResource</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>Config</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteDashboardConfigSpec">
AstarteDashboardConfigSpec
</a>
</em>
</td>
<td>
<p>
(Members of <code>Config</code> are embedded into this type.)
</p>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteDataUpdaterPlantSpec">AstarteDataUpdaterPlantSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">AstarteComponentsSpec</a>)
</p>
<div>
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
<code>AstarteGenericClusteredResource</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericClusteredResource</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>dataQueueCount</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>prefetchCount</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>Controls the prefetch count for Data Updater Plant. When fine-tuning Astarte, this parameter
can make a difference for what concerns Data Updater Plant ingestion performance. However,
it can also degrade performance significantly and/or increase risk of data loss when misconfigured.
Configure this value only if you know what you&rsquo;re doing and you have experience with RabbitMQ.
Defaults to 300</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteFeatures">AstarteFeatures
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
<p>AstarteFeatures enables/disables selectively a set of global features in Astarte</p>
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
<code>realmDeletion</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteGenericAPISpec">AstarteGenericAPISpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteAppengineAPISpec">AstarteAppengineAPISpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">AstarteComponentsSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteGenericComponentSpec">AstarteGenericComponentSpec</a>)
</p>
<div>
<p>AstarteGenericAPISpec represents a generic Astarte API Component in the Deployment spec</p>
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
<code>AstarteGenericClusteredResource</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericClusteredResource</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>disableAuthentication</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">AstarteGenericClusteredResource
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraSpec">AstarteCassandraSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteDashboardSpec">AstarteDashboardSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteDataUpdaterPlantSpec">AstarteDataUpdaterPlantSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteGenericAPISpec">AstarteGenericAPISpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteGenericComponentSpec">AstarteGenericComponentSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQSpec">AstarteRabbitMQSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteTriggerEngineSpec">AstarteTriggerEngineSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteVerneMQSpec">AstarteVerneMQSpec</a>)
</p>
<div>
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
</td>
</tr>
<tr>
<td>
<code>replicas</code><br/>
<em>
int32
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>antiAffinity</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>customAffinity</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#affinity-v1-core">
Kubernetes core/v1.Affinity
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>deploymentStrategy</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#deploymentstrategy-v1-apps">
Kubernetes apps/v1.DeploymentStrategy
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>version</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>image</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>resources</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Compute Resources for this Component.</p>
</td>
</tr>
<tr>
<td>
<code>additionalEnv</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#envvar-v1-core">
[]Kubernetes core/v1.EnvVar
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Additional environment variables for this Component</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteGenericComponentSpec">AstarteGenericComponentSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">AstarteComponentsSpec</a>)
</p>
<div>
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
<code>api</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericAPISpec">
AstarteGenericAPISpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>backend</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteGenericIngressSpec">AstarteGenericIngressSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressAPISpec">AstarteVoyagerIngressAPISpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressBrokerSpec">AstarteVoyagerIngressBrokerSpec</a>)
</p>
<div>
<p>AstarteGenericIngressSpec is a common struct for all Ingresses defined by AstarteVoyagerIngress</p>
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
</td>
</tr>
<tr>
<td>
<code>replicas</code><br/>
<em>
int32
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>type</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>loadBalancerIp</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>nodeSelector</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
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
</td>
</tr>
<tr>
<td>
<code>tlsRef</code><br/>
<em>
<a href="https://pkg.go.dev/github.com/appscode/voyager/apis/voyager/v1beta1#LocalTypedReference">
github.com/astarte-platform/astarte-kubernetes-operator/external/voyager/v1beta1.LocalTypedReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>annotationsService</code><br/>
<em>
map[string]string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstartePersistentStorageSpec">AstartePersistentStorageSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLSpec">AstarteCFSSLSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraSpec">AstarteCassandraSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQSpec">AstarteRabbitMQSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteVerneMQSpec">AstarteVerneMQSpec</a>)
</p>
<div>
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
<code>size</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#quantity-resource-api">
Kubernetes resource.Quantity
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>className</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>volumeDefinition</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#volume-v1-core">
Kubernetes core/v1.Volume
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteRabbitMQConnectionSpec">AstarteRabbitMQConnectionSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQSpec">AstarteRabbitMQSpec</a>)
</p>
<div>
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
<code>host</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>port</code><br/>
<em>
int16
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>username</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>password</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>virtualHost</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>sslConfiguration</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQSSLConfigurationSpec">
AstarteRabbitMQSSLConfigurationSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>secret</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.LoginCredentialsSecret">
LoginCredentialsSecret
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteRabbitMQSSLConfigurationSpec">AstarteRabbitMQSSLConfigurationSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQConnectionSpec">AstarteRabbitMQConnectionSpec</a>)
</p>
<div>
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
<code>enabled</code><br/>
<em>
bool
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>customCASecret</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>sni</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>customSNI</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteRabbitMQSpec">AstarteRabbitMQSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
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
<code>AstarteGenericClusteredResource</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericClusteredResource</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>connection</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQConnectionSpec">
AstarteRabbitMQConnectionSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>storage</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstartePersistentStorageSpec">
AstartePersistentStorageSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>additionalPlugins</code><br/>
<em>
[]string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>dataQueuesPrefix</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Configures the data queues prefix on RabbitMQ. You should change this setting only
in custom RabbitMQ installations.</p>
</td>
</tr>
<tr>
<td>
<code>eventsExchangeName</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Configures the events exchange name on RabbitMQ. You should change this setting only
in custom RabbitMQ installations.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteResourceEvent">AstarteResourceEvent
(<code>string</code> alias)</h3>
<div>
<p>AstarteResourceEvent represents a v1.Event reason for various events. They are all stated
in this enum to ease understanding and as a reference to users.</p>
</div>
<table>
<thead>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody><tr><td><p>&#34;ErrCritical&#34;</p></td>
<td><p>AstarteResourceEventCriticalError represents an unrecoverable error which requires manual intervention on the cluster</p>
</td>
</tr><tr><td><p>&#34;ErrInconsistentVersion&#34;</p></td>
<td><p>AstarteResourceEventInconsistentVersion means the requested Astarte version is inconsistent or unexpected</p>
</td>
</tr><tr><td><p>&#34;Migration&#34;</p></td>
<td><p>AstarteResourceEventMigration means the current Astarte Resource will be migrated from a previous one</p>
</td>
</tr><tr><td><p>&#34;ErrReconcile&#34;</p></td>
<td><p>AstarteResourceEventReconciliationFailed means there was a temporary failure in resource Reconciliation</p>
</td>
</tr><tr><td><p>&#34;Status&#34;</p></td>
<td><p>AstarteResourceEventStatus represents a generic Status event - in common situations, this is the most common event type</p>
</td>
</tr><tr><td><p>&#34;ErrUnsupportedVersion&#34;</p></td>
<td><p>AstarteResourceEventUnsupportedVersion means the requested Astarte version is not supported by the Operator</p>
</td>
</tr><tr><td><p>&#34;Upgrade&#34;</p></td>
<td><p>AstarteResourceEventUpgrade represents an event happening during a Cluster Upgrade</p>
</td>
</tr><tr><td><p>&#34;ErrUpgrade&#34;</p></td>
<td><p>AstarteResourceEventUpgradeError represents an error happening during a Cluster Upgrade</p>
</td>
</tr></tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.Astarte">Astarte</a>)
</p>
<div>
<p>AstarteSpec defines the desired state of Astarte</p>
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
<code>version</code><br/>
<em>
string
</em>
</td>
<td>
<p>The Astarte Version for this Resource</p>
</td>
</tr>
<tr>
<td>
<code>imagePullPolicy</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#pullpolicy-v1-core">
Kubernetes core/v1.PullPolicy
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>imagePullSecrets</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
[]Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>distributionChannel</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>deploymentStrategy</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#deploymentstrategy-v1-apps">
Kubernetes apps/v1.DeploymentStrategy
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>features</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteFeatures">
AstarteFeatures
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>rbac</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>storageClassName</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>api</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteAPISpec">
AstarteAPISpec
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>rabbitmq</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQSpec">
AstarteRabbitMQSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>cassandra</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraSpec">
AstarteCassandraSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>vernemq</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVerneMQSpec">
AstarteVerneMQSpec
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>cfssl</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteCFSSLSpec">
AstarteCFSSLSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>components</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">
AstarteComponentsSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>astarteSystemKeyspace</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteSystemKeyspaceSpec">
AstarteSystemKeyspaceSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>manualMaintenanceMode</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>ManualMaintenanceMode pauses all reconciliation activities but still computes the resource
status. It should be used only when the managed Astarte resources requires manual intervention
and the Operator cannot break out of the problem by itself. Do not set this field unless you
know exactly what you are doing.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteStatus">AstarteStatus
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.Astarte">Astarte</a>)
</p>
<div>
<p>AstarteStatus defines the observed state of Astarte</p>
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
<code>phase</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.ReconciliationPhase">
ReconciliationPhase
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>astarteVersion</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>operatorVersion</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>health</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteClusterHealth">
AstarteClusterHealth
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>baseAPIURL</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>brokerURL</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteSystemKeyspaceSpec">AstarteSystemKeyspaceSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
<p>astarteSystemKeyspace configures the main system keyspace for Astarte. As of now, these settings
have effect only upon cluster initialization, and will be ignored otherwise.</p>
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
<code>replicationFactor</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>The Replication Factor for the keyspace</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteTriggerEngineSpec">AstarteTriggerEngineSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteComponentsSpec">AstarteComponentsSpec</a>)
</p>
<div>
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
<code>AstarteGenericClusteredResource</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericClusteredResource</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>eventsQueueName</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Configures the name of the Events queue. Should be configured only in installations with a highly
customized RabbitMQ. It is advised to leave empty unless you know exactly what you&rsquo;re doing.</p>
</td>
</tr>
<tr>
<td>
<code>eventsRoutingKey</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Configures the routing key for Trigger Events. Should be configured only in installations
with a highly customized RabbitMQ and a custom Trigger Engine setup. It is advised to leave
empty unless you know exactly what you&rsquo;re doing, misconfiguring this value can cause heavy
breakage within Trigger Engine.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVerneMQSpec">AstarteVerneMQSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteSpec">AstarteSpec</a>)
</p>
<div>
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
<code>AstarteGenericClusteredResource</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericClusteredResource">
AstarteGenericClusteredResource
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericClusteredResource</code> are embedded into this type.)
</p>
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
</td>
</tr>
<tr>
<td>
<code>port</code><br/>
<em>
int16
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>caSecret</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>storage</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstartePersistentStorageSpec">
AstartePersistentStorageSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>deviceHeartbeatSeconds</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>Controls the device heartbeat from the broker to Astarte. The heartbeat is sent periodically
to prevent Astarte from keeping up stale connections from Devices in case the broker misbehaves
and does not send disconnection events. You should usually not tweak this value. Moreover, keep
in mind that when a lot of devices are connected simultaneously, having a short heartbeat time
might cause performance issues. Defaults to an hour.</p>
</td>
</tr>
<tr>
<td>
<code>maxOfflineMessages</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>The maximum number of QoS 1 or 2 messages to hold in the offline queue.
Defaults to 1000000. Set to -1 for no maximum (not recommended). Set to 0
if no messages should be stored offline.</p>
</td>
</tr>
<tr>
<td>
<code>persistentClientExpiration</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>This option allows persistent clients ( = clean session set to
false) to be removed if they do not reconnect within &lsquo;persistent_client_expiration&rsquo;.
This is a non-standard option. As far as the MQTT specification is concerned,
persistent clients persist forever.
The expiration period should be an integer followed by one of &rsquo;d&rsquo;, &lsquo;w&rsquo;, &rsquo;m&rsquo;, &lsquo;y&rsquo; for
day, week, month, and year.
Default: 1 year</p>
</td>
</tr>
<tr>
<td>
<code>mirrorQueue</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>sslListener</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
<p>This option allows, when true, to handle SSL termination at VerneMQ level.
Default: false</p>
</td>
</tr>
<tr>
<td>
<code>sslListenerCertSecretName</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Reference the name of the secret containing the TLS certificate for VerneMQ.
The secret must be present in the same namespace in which Astarte resides.
The field will be used only if SSLListener is set to true.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVoyagerIngress">AstarteVoyagerIngress
</h3>
<div>
<p>AstarteVoyagerIngress is the Schema for the astartevoyageringresses API</p>
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
<code>status</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressStatus">
AstarteVoyagerIngressStatus
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>spec</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressSpec">
AstarteVoyagerIngressSpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>imagePullPolicy</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#pullpolicy-v1-core">
Kubernetes core/v1.PullPolicy
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>astarte</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>api</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressAPISpec">
AstarteVoyagerIngressAPISpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>dashboard</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressDashboardSpec">
AstarteVoyagerIngressDashboardSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>broker</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressBrokerSpec">
AstarteVoyagerIngressBrokerSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>letsencrypt</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressLetsEncryptSpec">
AstarteVoyagerIngressLetsEncryptSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</table>
</td>
</tr>
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
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressAPISpec">AstarteVoyagerIngressAPISpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressSpec">AstarteVoyagerIngressSpec</a>)
</p>
<div>
<p>AstarteVoyagerIngressAPISpec defines the specification of the APIs</p>
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
<code>AstarteGenericIngressSpec</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericIngressSpec">
AstarteGenericIngressSpec
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericIngressSpec</code> are embedded into this type.)
</p>
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
with serveMetricsToSubnet</p>
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
ACL src syntax (e.g.: 10.0.0.0/16)</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressBrokerSpec">AstarteVoyagerIngressBrokerSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressSpec">AstarteVoyagerIngressSpec</a>)
</p>
<div>
<p>AstarteVoyagerIngressBrokerSpec defines the specification of the Broker</p>
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
<code>AstarteGenericIngressSpec</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteGenericIngressSpec">
AstarteGenericIngressSpec
</a>
</em>
</td>
<td>
<p>
(Members of <code>AstarteGenericIngressSpec</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>maxConnections</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressDashboardSpec">AstarteVoyagerIngressDashboardSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressSpec">AstarteVoyagerIngressSpec</a>)
</p>
<div>
<p>AstarteVoyagerIngressDashboardSpec defines the specification of the Dashboard</p>
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
<code>ssl</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
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
</td>
</tr>
<tr>
<td>
<code>tlsRef</code><br/>
<em>
<a href="https://pkg.go.dev/github.com/appscode/voyager/apis/voyager/v1beta1#LocalTypedReference">
github.com/astarte-platform/astarte-kubernetes-operator/external/voyager/v1beta1.LocalTypedReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressLetsEncryptSpec">AstarteVoyagerIngressLetsEncryptSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressSpec">AstarteVoyagerIngressSpec</a>)
</p>
<div>
<p>AstarteVoyagerIngressLetsEncryptSpec defines the specification of the Let&rsquo;s Encrypt Integration</p>
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
<code>use</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>staging</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>acmeEmail</code><br/>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>domains</code><br/>
<em>
[]string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>autoHTTPChallenge</code><br/>
<em>
bool
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>challengeProvider</code><br/>
<em>
<a href="https://pkg.go.dev/github.com/appscode/voyager/apis/voyager/v1beta1#ChallengeProvider">
github.com/astarte-platform/astarte-kubernetes-operator/external/voyager/v1beta1.ChallengeProvider
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressSpec">AstarteVoyagerIngressSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngress">AstarteVoyagerIngress</a>)
</p>
<div>
<p>AstarteVoyagerIngressSpec defines the desired state of AstarteVoyagerIngress</p>
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
<code>imagePullPolicy</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#pullpolicy-v1-core">
Kubernetes core/v1.PullPolicy
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>astarte</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>api</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressAPISpec">
AstarteVoyagerIngressAPISpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>dashboard</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressDashboardSpec">
AstarteVoyagerIngressDashboardSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>broker</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressBrokerSpec">
AstarteVoyagerIngressBrokerSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>letsencrypt</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressLetsEncryptSpec">
AstarteVoyagerIngressLetsEncryptSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.AstarteVoyagerIngressStatus">AstarteVoyagerIngressStatus
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteVoyagerIngress">AstarteVoyagerIngress</a>)
</p>
<div>
<p>AstarteVoyagerIngressStatus defines the observed state of AstarteVoyagerIngress</p>
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
<h3 id="api.astarte-platform.org/v1alpha2.BlockWorker">BlockWorker
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.ContainerBlockSpec">ContainerBlockSpec</a>)
</p>
<div>
<p>BlockWorker defines a Worker for a Container Block</p>
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
<code>id</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>dataProvider</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.DataProvider">
DataProvider
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.ContainerBlockSpec">ContainerBlockSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.FlowSpec">FlowSpec</a>)
</p>
<div>
<p>ContainerBlockSpec defines a Container Block in a Flow</p>
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
<code>id</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>image</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>imagePullSecrets</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
[]Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>environment</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#envvar-v1-core">
[]Kubernetes core/v1.EnvVar
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>resources</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>config</code><br/>
<em>
string
</em>
</td>
<td>
<p>Configuration represents the JSON string carrying the user configuration for this block</p>
</td>
</tr>
<tr>
<td>
<code>workers</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.BlockWorker">
[]BlockWorker
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.DataProvider">DataProvider
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.BlockWorker">BlockWorker</a>)
</p>
<div>
<p>DataProvider is a struct which defines which Data Providers (e.g. Brokers) are available for a
Worker</p>
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
<code>rabbitmq</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.RabbitMQDataProvider">
RabbitMQDataProvider
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.Flow">Flow
</h3>
<div>
<p>Flow is the Schema for the flows API</p>
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
<a href="#api.astarte-platform.org/v1alpha2.FlowSpec">
FlowSpec
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
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>astarteRealm</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>nativeBlocks</code><br/>
<em>
int
</em>
</td>
<td>
<p>Defines the amount of non-container blocks in the Flow</p>
</td>
</tr>
<tr>
<td>
<code>nativeBlocksResources</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#resourcelist-v1-core">
Kubernetes core/v1.ResourceList
</a>
</em>
</td>
<td>
<p>Defines the overall resources consumed by Native Blocks</p>
</td>
</tr>
<tr>
<td>
<code>flowPool</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<p>EE Only: Defines the Flow Pool in which the Flow will be allocated.</p>
</td>
</tr>
<tr>
<td>
<code>blocks</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.ContainerBlockSpec">
[]ContainerBlockSpec
</a>
</em>
</td>
<td>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.FlowStatus">
FlowStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.FlowSpec">FlowSpec
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.Flow">Flow</a>)
</p>
<div>
<p>FlowSpec defines the desired state of Flow</p>
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
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>astarteRealm</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>nativeBlocks</code><br/>
<em>
int
</em>
</td>
<td>
<p>Defines the amount of non-container blocks in the Flow</p>
</td>
</tr>
<tr>
<td>
<code>nativeBlocksResources</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#resourcelist-v1-core">
Kubernetes core/v1.ResourceList
</a>
</em>
</td>
<td>
<p>Defines the overall resources consumed by Native Blocks</p>
</td>
</tr>
<tr>
<td>
<code>flowPool</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#localobjectreference-v1-core">
Kubernetes core/v1.LocalObjectReference
</a>
</em>
</td>
<td>
<p>EE Only: Defines the Flow Pool in which the Flow will be allocated.</p>
</td>
</tr>
<tr>
<td>
<code>blocks</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.ContainerBlockSpec">
[]ContainerBlockSpec
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.FlowState">FlowState
(<code>string</code> alias)</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.FlowStatus">FlowStatus</a>)
</p>
<div>
<p>FlowState describes the global state of a Flow</p>
</div>
<table>
<thead>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody><tr><td><p>&#34;Flowing&#34;</p></td>
<td><p>FlowStateFlowing means the Flow is currently active and all of its blocks are stable. A healthy flow should stay
in this state for most of its lifecycle.</p>
</td>
</tr><tr><td><p>&#34;Unhealthy&#34;</p></td>
<td><p>FlowStateUnhealthy means the Flow is currently having some non-transient or unrecoverable errors.
Manual intervention might be required.</p>
</td>
</tr><tr><td><p>&#34;&#34;</p></td>
<td><p>FlowStateUnknown represents an Unknown State of the Flow. When in this state, it might
have never been reconciled.</p>
</td>
</tr><tr><td><p>&#34;Unstable&#34;</p></td>
<td><p>FlowStateUnstable means the Flow is either reconciling or restarting some of its blocks.
It usually transitions to this State before moving to Flowing.</p>
</td>
</tr></tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.FlowStatus">FlowStatus
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.Flow">Flow</a>)
</p>
<div>
<p>FlowStatus defines the observed state of Flow</p>
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
<code>state</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.FlowState">
FlowState
</a>
</em>
</td>
<td>
<p>State defines the overall state of the Flow</p>
</td>
</tr>
<tr>
<td>
<code>totalContainerBlocks</code><br/>
<em>
int
</em>
</td>
<td>
<p>Represents the total number of the Container Blocks in the Flow</p>
</td>
</tr>
<tr>
<td>
<code>readyContainerBlocks</code><br/>
<em>
int
</em>
</td>
<td>
<p>Represents the total number of Ready Container Blocks in the Flow. In a healthy Flow,
this matches the number of Total Container Blocks.</p>
</td>
</tr>
<tr>
<td>
<code>resources</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#resourcelist-v1-core">
Kubernetes core/v1.ResourceList
</a>
</em>
</td>
<td>
<p>The overall resources allocated in the cluster for this Block</p>
</td>
</tr>
<tr>
<td>
<code>failingContainerBlocks</code><br/>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>Represents the total number of Container Blocks with non temporary failures. Present only
if any of the Blocks is in such state. When present, manual intervention is most likely required.</p>
</td>
</tr>
<tr>
<td>
<code>unrecoverableFailures</code><br/>
<em>
<a href="https://v1-19.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#containerstate-v1-core">
[]Kubernetes core/v1.ContainerState
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>UnrecoverableFailures lists all the ContainerStates of failing containers, for further inspection.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.LoginCredentialsSecret">LoginCredentialsSecret
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteCassandraConnectionSpec">AstarteCassandraConnectionSpec</a>, <a href="#api.astarte-platform.org/v1alpha2.AstarteRabbitMQConnectionSpec">AstarteRabbitMQConnectionSpec</a>)
</p>
<div>
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
<code>name</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>usernameKey</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>passwordKey</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.RabbitMQConfig">RabbitMQConfig
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.RabbitMQDataProvider">RabbitMQDataProvider</a>)
</p>
<div>
<p>RabbitMQConfig represents configuration for RabbitMQ</p>
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
<code>host</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>port</code><br/>
<em>
int16
</em>
</td>
<td>
<em>(Optional)</em>
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
</td>
</tr>
<tr>
<td>
<code>username</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>password</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.RabbitMQDataProvider">RabbitMQDataProvider
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.DataProvider">DataProvider</a>)
</p>
<div>
<p>RabbitMQDataProvider is a representation of a Data Provider based upon RabbitMQ</p>
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
<code>queues</code><br/>
<em>
[]string
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>exchange</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.RabbitMQExchange">
RabbitMQExchange
</a>
</em>
</td>
<td>
<em>(Optional)</em>
</td>
</tr>
<tr>
<td>
<code>rabbitmq</code><br/>
<em>
<a href="#api.astarte-platform.org/v1alpha2.RabbitMQConfig">
RabbitMQConfig
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>RabbitMQConfig is an optional field which allows to specify configuration for an external RabbitMQ
broker. If not specified, Astarte&rsquo;s main Broker will be used.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.RabbitMQExchange">RabbitMQExchange
</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.RabbitMQDataProvider">RabbitMQDataProvider</a>)
</p>
<div>
<p>RabbitMQExchange is a representation of a RabbitMQ Exchange</p>
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
<code>name</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>routingKey</code><br/>
<em>
string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="api.astarte-platform.org/v1alpha2.ReconciliationPhase">ReconciliationPhase
(<code>string</code> alias)</h3>
<p>
(<em>Appears on:</em><a href="#api.astarte-platform.org/v1alpha2.AstarteStatus">AstarteStatus</a>)
</p>
<div>
<p>ReconciliationPhase describes the reconciliation phase the Resource is in</p>
</div>
<table>
<thead>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody><tr><td><p>&#34;Failed&#34;</p></td>
<td><p>ReconciliationPhaseFailed means the Resource failed to reconcile. If this state persists, a manual intervention
might be necessary.</p>
</td>
</tr><tr><td><p>&#34;Disabled, in Manual Maintenance Mode&#34;</p></td>
<td><p>ReconciliationPhaseManualMaintenanceMode means the Resource is currently not being reconciled as the resource is in
Manual Maintenance Mode. This happens only when the user explicitly requires that.</p>
</td>
</tr><tr><td><p>&#34;Reconciled&#34;</p></td>
<td><p>ReconciliationPhaseReconciled means the Resource is currently reconciled and stable. The resource should stay in this
state for most of the time.</p>
</td>
</tr><tr><td><p>&#34;Reconciling&#34;</p></td>
<td><p>ReconciliationPhaseReconciling means the Resource is currently in the process of being reconciled</p>
</td>
</tr><tr><td><p>&#34;&#34;</p></td>
<td><p>ReconciliationPhaseUnknown represents an Unknown Phase of the Resource. When in this state, it might
have never been reconciled</p>
</td>
</tr><tr><td><p>&#34;Upgrading&#34;</p></td>
<td><p>ReconciliationPhaseUpgrading means the Resource is currently in the process of being upgraded to a new Astarte version.
When successful, the Resource will transition to ReconciliationPhaseReconciling</p>
</td>
</tr></tbody>
</table>
<hr/>
<p><em>
Generated with <code>gen-crd-api-reference-docs</code>
on git commit <code>2725e75</code>.
</em></p>
