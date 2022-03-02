load('ext://syncback', 'syncback')

k8s_yaml(['deployment.yaml'])

# Sync back lock files to the host when they are updated.
syncback('syncback-lockfiles', 'deployment.apps/tilt-reproduce-deployment', '/app/myapp/', paths=['composer.lock', 'yarn.lock', 'symfony.lock', 'composer.json', 'package.json'], container='application')