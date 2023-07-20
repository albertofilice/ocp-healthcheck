# Health Check and URL Check ansible playbook for OCP4

## Cluster Check

- Verifies the connection to the cluster
- Verifies the status of the cluster nodes
- Verifies the status of OpenShift services
- Verifies the status of cluster operators
- Verifies the status of CephBlockPool in ODF
- Checks the status of Ceph in ODF
- Checks the available space in Ceph ODF
- Checks the available space on nodes

### RUN

Compile Vars:

```yaml
  vars:
    ocp_username: ""
    ocp_password: ""
    ocp_api_url: ""
    mail_host: ""
    mail_port: ""
    mail_username: ""
    mail_password: ""
    mail_to: ""
    mail_cc: ""
    mail_sender: ""
```
run the playbook for Cluster Health Check:

`$ ansible-playbook cluster_check.yaml`

<table class="table table-bordered">

<thead>

<tr>

<th>Nome controllo</th>

<th>Stato</th>

</tr>

</thead>

<tbody>

<tr>

<td>Verifies the connection to the cluster</td>

<td>passed</td>

</tr>

<tr>

<td>Verifies the status of the cluster nodes</td>

<td>passed</td>

</tr>

<tr>

<td>Verifies the status of OpenShift services</td>

<td>passed</td>

</tr>

<tr>

<td>Verifies the status of cluster operators</td>

<td>passed</td>

</tr>

<tr>

<td>Verifies the status of CephBlockPool in ODF</td>

<td>passed</td>

</tr>

<tr>

<td>Checks the status of Ceph in ODF</td>

<td>passed</td>

</tr>

<tr>

<td>Checks the available space in Ceph ODF</td>

<td>passed</td>

</tr>

<tr>

<td>Checks the available space on nodes</td>

<td>passed</td>

</tr>

</tbody>

</table>


## Site Check

The site check playbook verifies that the website responds to an http request with 200.

Compile Vars:

```yaml
  vars:
    site_urls:
      - 'example.com'
      - 'example.it'
    mail_host: ""
    mail_port: ""
    mail_username: ""
    mail_password: ""
    mail_to: ""
    mail_cc: ""
    mail_sender: ""   
```
run the playbook for Site Check:

`$ ansible-playbook site_check.yaml`


<table class="table table-bordered">

<tbody>

<tr>

<th>Website</th>

<th>Status Code</th>

<th>Status</th>

</tr>

<tr>

<td>example.com</td>

<td>200</td>

<td class="passed">Passed</td>

</tr>

<tr>

<td>example.it</td>

<td>200</td>

<td class="passed">Passed</td>

</tr>


</tbody>

</table>


