# wordpress

Install wordpress:
```bash
helm upgrade --install wordpress bitnami/wordpress \
  --set wordpressUsername=admin \
  --set wordpressPassword=password \
  --set mariadb.auth.rootPassword=secretpassword \
  --set service.type=ClusterIP \
  --set ingress.enabled=true \
  --set ingress.certManager=true \
  --set ingress.tls=true \
  --set ingress.annotations."cert-manager\.io/cluster-issuer"=letsencrypt \
  --set ingress.hostname=wordpress.k8s.shubhamtatvamasi.com
```


