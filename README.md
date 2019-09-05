# ansible-role-zerotierone

Ansible role for ZeroTier One Vpn


Role Variables
zerotier_network_id

Type: string
Default value:
Description: The 16 character network ID of the network the new members should join. The node will not join any network if omitted.
zerotier_member_register_short_hostname

Type: boolean
Default value: false
Description: By default inventory_hostname will be used to name a member in a network. If set to true, inventory_hostname_short will be used instead.
zerotier_member_ip_assignments

Type: list
Default value: []
Description: A list of IP addresses to assign this member. The member will be automatically assigned an address on the network if left out.
zerotier_member_description

Type: string
Default value: ""
Description: Optional desription for a member.
zerotier_api_accesstoken

Type: string
Default value: ""
Description: The access token needed to authorize with the ZeroTier API. You can generate one in your account settings at https://my.zerotier.com/. If this is left out then the newly joined member will not be automatically authorized.
zerotier_api_url

Type: string
Default value: https://my.zerotier.com
Description: The url where the Zerotier API lives. Must use HTTPS protocol.
zerotier_api_delegate

Type: string
Default value: localhost
Description: Option to delegate tasks for Zerotier API calls. This is usefull in a situation where API calls can only be made from a whitelisted management server, for example.
