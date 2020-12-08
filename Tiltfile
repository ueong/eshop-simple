k8s_yaml(['k8s/backend.yaml','k8s/frontend.yaml','k8s/ingress.yaml','k8s/postgresql.yaml','k8s/redis.yaml'])
docker_build('eshop-frontend-simple','eshop-frontend')
custom_build(
  'eshop-backend-simple',
  'cd eshop-backend && gradlew jibDockerBuild --image %EXPECTED_REF%',
  deps=['src'])