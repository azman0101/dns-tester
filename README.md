#  Tool to test how many dns loopups are slower than 100 ms

Testing of https://github.com/kubernetes/kubernetes/issues/45363#issuecomment-389887505 

You can specify the `DNS_NAME`, `DNS_NAME_TIMEOUT` and `WAIT_BETWEEN_REQUESTS` environment variables.

Start with:

    kubectl create -f kubernetes/deployment.yml

Get logs with:

    kubectl log dns-tester

Clean up with:

    kubectl delete pod dns-tester
