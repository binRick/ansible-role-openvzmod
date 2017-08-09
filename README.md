# Ansible Role: openvzmod

This role contains 2 modules to manage OpenVZ containers:

- openvz: Manage OpenVZ containers
- openvz_exec: Execute commands in the OpenVZ container

## Module Options

### openvz options

> <table border=1 cellpadding=4>
> <tr>
> <th class="head">parameter</th>
> <th class="head">required</th>
> <th class="head">default</th>
> <th class="head">choices</th>
> <th class="head">comments</th>
> </tr>
> <tr>
> <td>applyconfig</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --applyconfig</code>.</td>
> </tr>
> <tr>
> <td>avnumproc</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --avnumproc</code>.</td>
> </tr>
> <tr>
> <td>capability</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --capability</code>.</td>
> </tr>
> <tr>
> <td>config</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl create --config</code>.</td>
> </tr>
> <tr>
> <td>cpulimit</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --cpulimit</code>.</td>
> </tr>
> <tr>
> <td>cpumask</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --cpumask</code>.</td>
> </tr>
> <tr>
> <td>cpus</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --cpus</code>.</td>
> </tr>
> <tr>
> <td>cpuunits</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --cpuunits</code>.</td>
> </tr>
> <tr>
> <td>ctid</td>
> <td>yes</td>
> <td></td>
> <td><ul></ul></td>
> <td>Container ID or name to manage.</td>
> </tr>
> <tr>
> <td>dcachesize</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --dcachesize</code>.</td>
> </tr>
> <tr>
> <td>description</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --description</code>.</td>
> </tr>
> <tr>
> <td>dgramrcvbuf</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --dgramrcvbuf</code>.</td>
> </tr>
> <tr>
> <td>disabled</td>
> <td>no</td>
> <td></td>
> <td><ul><li>yes</li><li>no</li></ul></td>
> <td>Parameter passed to <code>vzctl set --disabled</code>.</td>
> </tr>
> <tr>
> <td>diskinodes</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --diskinodes</code>.</td>
> </tr>
> <tr>
> <td>diskspace</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --diskspace</code>.</td>
> </tr>
> <tr>
> <td>features</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --features</code>.</td>
> </tr>
> <tr>
> <td>hostname</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --hostname</code>.</td>
> </tr>
> <tr>
> <td>iolimit</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --iolimit</code>.</td>
> </tr>
> <tr>
> <td>ioprio</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --ioprio</code>.</td>
> </tr>
> <tr>
> <td>iopslimit</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --iopslimit</code>.</td>
> </tr>
> <tr>
> <td>ipadd</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --ipadd</code>.</td>
> </tr>
> <tr>
> <td>ipaddr</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>IP address settings in the idempotent way.  Specify addresses in an array or a space delimited string.</td>
> </tr>
> <tr>
> <td>ipdel</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --ipdel</code>.</td>
> </tr>
> <tr>
> <td>iptables</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --iptables</code>.</td>
> </tr>
> <tr>
> <td>kmemsize</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --kmemsize</code>.</td>
> </tr>
> <tr>
> <td>layout</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl create --layout</code>.</td>
> </tr>
> <tr>
> <td>lockedpages</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --lockedpages</code>.</td>
> </tr>
> <tr>
> <td>mount_opts</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --mount_opts</code>.</td>
> </tr>
> <tr>
> <td>name</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --name</code>.</td>
> </tr>
> <tr>
> <td>nameserver</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --nameserver</code>.</td>
> </tr>
> <tr>
> <td>netif</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Network interface settings in the idempotent way.  Specify interfaces in an array or a space delimited string.</td>
> </tr>
> <tr>
> <td>netif_add</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --netif_add</code>.</td>
> </tr>
> <tr>
> <td>netif_del</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --netif_del</code>.</td>
> </tr>
> <tr>
> <td>nodemask</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --nodemask</code>.</td>
> </tr>
> <tr>
> <td>numfile</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numfile</code>.</td>
> </tr>
> <tr>
> <td>numflock</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numflock</code>.</td>
> </tr>
> <tr>
> <td>numiptent</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numiptent</code>.</td>
> </tr>
> <tr>
> <td>numothersock</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numothersock</code>.</td>
> </tr>
> <tr>
> <td>numproc</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numproc</code>.</td>
> </tr>
> <tr>
> <td>numpty</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numpty</code>.</td>
> </tr>
> <tr>
> <td>numsiginfo</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numsiginfo</code>.</td>
> </tr>
> <tr>
> <td>numtcpsock</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --numtcpsock</code>.</td>
> </tr>
> <tr>
> <td>onboot</td>
> <td>no</td>
> <td></td>
> <td><ul><li>yes</li><li>no</li></ul></td>
> <td>Parameter passed to <code>vzctl set --onboot</code>.</td>
> </tr>
> <tr>
> <td>oomguarpages</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --oomguarpages</code>.</td>
> </tr>
> <tr>
> <td>ostemplate</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl create --ostemplate</code>.</td>
> </tr>
> <tr>
> <td>othersockbuf</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --othersockbuf</code>.</td>
> </tr>
> <tr>
> <td>physpages</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --physpages</code>.</td>
> </tr>
> <tr>
> <td>private</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl create --private</code>.</td>
> </tr>
> <tr>
> <td>privvmpages</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --privvmpages</code>.</td>
> </tr>
> <tr>
> <td>quotatime</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --quotatime</code>.</td>
> </tr>
> <tr>
> <td>quotaugidlimit</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --quotaugidlimit</code>.</td>
> </tr>
> <tr>
> <td>ram</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --ram</code>.</td>
> </tr>
> <tr>
> <td>root</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl create --root</code>.</td>
> </tr>
> <tr>
> <td>searchdomain</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --searchdomain</code>.</td>
> </tr>
> <tr>
> <td>shmpages</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --shmpages</code>.</td>
> </tr>
> <tr>
> <td>state</td>
> <td>no</td>
> <td></td>
> <td><ul><li>started</li><li>stopped</li><li>present</li><li>absent</li></ul></td>
> <td>Container target state.</td>
> </tr>
> <tr>
> <td>swap</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --swap</code>.</td>
> </tr>
> <tr>
> <td>swappages</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --swappages</code>.</td>
> </tr>
> <tr>
> <td>tcprcvbuf</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --tcprcvbuf</code>.</td>
> </tr>
> <tr>
> <td>tcpsndbuf</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --tcpsndbuf</code>.</td>
> </tr>
> <tr>
> <td>userpasswd</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>Parameter passed to <code>vzctl set --userpasswd</code>.</td>
> </tr>
> <tr>
> <td>vmguarpages</td>
> <td>no</td>
> <td></td>
> <td><ul></ul></td>
> <td>UBC parameter passed to <code>vzctl set --vmguarpages</code>.</td>
> </tr>
> </table>

### openvz_exec options

> <table border=1 cellpadding=4>
> <tr>
> <th class="head">parameter</th>
> <th class="head">required</th>
> <th class="head">default</th>
> <th class="head">choices</th>
> <th class="head">comments</th>
> </tr>
> <tr>
> <td>ctid</td>
> <td>yes</td>
> <td></td>
> <td><ul></ul></td>
> <td>Container ID or name to execute commands.</td>
> </tr>
> <tr>
> <td>exec</td>
> <td>yes</td>
> <td></td>
> <td><ul></ul></td>
> <td>Shell commands to execute in the container.</td>
> </tr>
> </table>

## Requirements

None.

## Role Variables

None.

## Dependencies

None.

## Example Playbook

```yaml
---
- hosts: vzhost
  sudo: yes
  roles:
  - yaegashi.openvzmod
  tasks:
  - openvz:
      ctid: 1000
      state: started
      ostemplate: ubuntu-14.04-x86_64-minimal
      ram: 1G
      swap: 512M
      diskspace: 2G
      hostname: vzguest
      name: vzguest
      ipaddr:
      - 192.168.0.100
      - 192.168.0.101
      nameserver: 192.168.0.1
      userpasswd: ansible:secret
      description: Ubuntu trusty amd64 container
```

```yaml
---
- hosts: vzhost
  sudo: yes
  roles:
  - yaegashi.openvzmod
  tasks:
  - openvz_exec:
      ctid: 1000
      exec: |
        adduser --system --group --uid 999 ansible
        adduser ansible sudo
        echo ansible:secret | chpasswd
```

## TODO

Some other ideas for possible OpenVZ container management modules:

- openvz_snapshot: Manipulate ploop snapshots
- openvz_exec: Add support for executing a local script file
- Connection plugin for vzctl exec

## License

GPLv3+

