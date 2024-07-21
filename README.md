# k8s_lb_https_hello_world

- Straight-forward  way how to use cloudflare DNS domain together with GCP external load balancer.
what i did:
1) Setup external static IP on GCP
2) buy domain and set A record to that IP, set ssl/tls mode as full
3) generate STL key and cert from cloudflare website and save it locally. Push it to GCP as secret and link it to ingress
4) Unfortunately it is not enough, you have to use some sign service like let's encrypt and issuer because GCP is not sure...
5) use this k8s configuration
6) it should be all.


Debug helpers:
curl https://yourdomain -kv
kubectl describe ingress srs-ingress




