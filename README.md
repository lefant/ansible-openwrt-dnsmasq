openwrt-dnsmasq
===============

dnsmasq specific config of your openwrt system.
compare: [http://wiki.openwrt.org/doc/uci/dhcp]

currently only zone specific forwarder config is implemented.

at least [custom domains] would be nice to add some day.

Role Variables
--------------

there is a nested dict `dnsmasq`. look at tasks and defaults. the
layout is a bit weird because i use with_subelements.

you may want to consider `hash_behaviour=merge` in your ansible.cfg

Dependencies
------------

[lefant.openwrt-uci]

Example Playbook
----------------

[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]

Requirements
------------

must be kept minimal as this is supposed to run on openwrt embedded
systems. in particular we try get by with plain POSIX shell, using
neither python nor bash in any way. lua could be an option as that
seems to be the openwrt scripting language of choice.

License
-------

BSD

Author Information
------------------

Fabian Linzberger, [http://e.lefant.net/]



[http://wiki.openwrt.org/doc/uci/dhcp]: http://wiki.openwrt.org/doc/uci/dhcp
[custom domains]: http://wiki.openwrt.org/doc/uci/dhcp#custom.domain
[lefant.openwrt-uci]: https://galaxy.ansible.com/list#/roles/1645
[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]: https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml
[http://e.lefant.net/]: http://e.lefant.net/
