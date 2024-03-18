# Metallb Chart

The following deploys the metallb chart into the cluster. The ippool and l2 advertisement must not be enabled on install since
the CRDs will be missing but can be added in a subsuquent upgrade. You have to ensure that the ips in the IP pool are in the LAN cidr so that a route exists for them, however, keep them out of the range used by DHCP so that no collisions occurr.