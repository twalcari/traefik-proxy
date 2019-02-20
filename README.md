========================
JupyterHub Traefik Proxy
========================

An implementation of the JupyterHub proxy api with `traefik <https://traefik.io>`__ : an extremely lightweight,
portable reverse proxy implementation, that supports load balancing and can configure itself automatically and dynamically.

There are two versions for the proxy, depending on how traefik stores the routes:

* TraefikTomlProxy - *for* **smaller**, *single-node deployments*
* TraefikEtcdProxy - *for* **distributed** *setups*

### Instalation

You can find a complete installation guide [here](https://jupyterhub-traefik-proxy.readthedocs.io/en/latest/install.html).


### Documentation

The latest documentation is available [here](https://jupyterhub-traefik-proxy.readthedocs.io/en/latest/).

### Running the tests

There are some tests that use *etcdctl* command line client for etcd.
Make sure to set environment variable ETCDCTL_API=3 before running the tests, so that the v3 API to be used, e.g.:

```
$ export ETCDCTL_API=3
```

You can then run the all the test suite from the *traefik-proxy* directory with:

```
$ pytest -v ./tests
```

Or you can run a specific test with:

```
$ pytest -v ./tests/<test-file-name>
```

### Example setups:

* For TraefikEtcdProxy: https://jupyterhub-traefik-proxy.readthedocs.io/en/latest/etcd.html#example-setup
* For TraefikTomlProxy: https://jupyterhub-traefik-proxy.readthedocs.io/en/latest/toml.html#example-setup

