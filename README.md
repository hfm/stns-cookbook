STNS Cookbook
===============
stns instarll cookbook

Attributes
----------
#### stns::server
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['stns']['server']['port']</tt></td>
    <td>int</td>
    <td>start up port</td>
    <td><tt>1104</tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['server']['user']</tt></td>
    <td>string</td>
    <td>Basic Auth User</td>
    <td><tt></tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['server']['password']</tt></td>
    <td>string</td>
    <td>Basic Auth Password</td>
    <td><tt></tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['server']['users']</tt></td>
    <td>ArrayHash</td>
    <td>users</td>
    <td><tt>[{}]</tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['server']['groups']</tt></td>
    <td>ArrayHash</td>
    <td>groups</td>
    <td><tt>[{}]</tt></td>
  </tr>
</table>

##### users or groups hash
```
default['stns']['server']['users'] = [
  { 'name' => 'example', 'id' => 1001 }
]

default['stns']['server']['groups'] = [
  { 'name' => 'example', 'id' => 2001 }
]
```
#### stns::client
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['stns']['client']['api_end_point']</tt></td>
    <td>string array</td>
    <td>stns end point</td>
    <td><tt>[http://localhost:1104]</tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['client']['user']</tt></td>
    <td>string</td>
    <td>Basic Auth User</td>
    <td><tt></tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['client']['password']</tt></td>
    <td>string</td>
    <td>Basic Auth Password</td>
    <td><tt></tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['client']['wrapper_path']</tt></td>
    <td>string</td>
    <td>stns query wrapper path</td>
    <td><tt>/usr/local/bin/stns-query-wrapper</tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['client']['chain_ssh_wrapper']</tt></td>
    <td>string</td>
    <td>fail over ssh wrapper</td>
    <td><tt></tt></td>
  </tr>
  <tr>
    <td><tt>['stns']['client']['ssl_verify']</tt></td>
    <td>bool</td>
    <td>disable ssl verify</td>
    <td><tt>true</tt></td>
  </tr>
</table>

#### ref cookbooks
* [nscd](https://github.com/chef-cookbooks/nscd)


Contributing
------------
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
* pyama86
