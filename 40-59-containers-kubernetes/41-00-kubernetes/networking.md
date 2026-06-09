# Kubernetes networking

By default Kubernetes has a flat network, meaning pods can freely communicate with other pods without NAT. This is made possible by the CNI that implements 1 of 2 things, either overlay networks (tunneling) or direct routing. The former is done by encapsulation, essentially wrapping pod-to-pod packets inside another packet (common protocols are VXLAN and Geneve).
