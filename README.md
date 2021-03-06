# Flynn Deploy for Wercker

Deploys a package from wercker to Flynn via git push interface. 
https://flynn.io/docs/cli


You must set your keys in the wercker deploy variable page.

## Options


* 'flynn_cluster_name' (required) The cluster name (default/staging/production)
* 'flynn_controller_domain' (required) Should be $CLUSTER_DOMAIN
* 'flynn_controller_key' (required) The controller authentication key.
* 'flynn_app_name' (required) A name you want to refer to the cluster by locally.
* 'flynn_tls_cert' (required) A name you want to refer to the cluster by locally.

## Example

    - alekssem/flynn-deploy:
        flynn_cluster_name: $FLYNN_CLUSTER_NAME
        flynn_controller_domain: $FLYNN_CONTROLLER_DOMAIN
        flynn_controller_key: $FLYNN_CONTROLLER_KEY
        flynn_app_name: $FLYNN_APP_NAME
        flynn_tls_cert: $FLYNN_TLS_CERT
