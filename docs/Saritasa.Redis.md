
# Saritasa.Redis

## Initialize-Redis

### Synopsis
Configure some basic Redis parameters.

### Syntax
Initialize-Redis \[\[-Host\] &lt;String&gt;\] \[\[-Port\] &lt;Int32&gt;\] \[\[-Credential\] &lt;PSCredential&gt;\] \[\[-UseSsl\] &lt;Boolean&gt;\]
\[&lt;CommonParameters&gt;\]

### Parameters

<table class="table table-striped table-bordered table-condensed visible-on">
	<thead>
		<tr>
			<th>Name</th>
			<th class="visible-lg visible-md">Alias</th>
			<th>Description</th>
			<th class="visible-lg visible-md">Required?</th>
			<th class="visible-lg">Pipeline Input</th>
			<th class="visible-lg">Default Value</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td><nobr>Host</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Redis hostname.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Port</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Redis port.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">0</td>
		</tr>
		<tr>
			<td><nobr>Credential</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Credential containing password to Redis.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>UseSsl</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Whether or not to use secure connection.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">True</td>
		</tr>
	</tbody>
</table>

### Note
StackExchange.Redis.dll file should be located in the same directory with this script.


### Examples
**EXAMPLE 1**
```
$password = "123" | ConvertTo-SecureString -asPlainText -Force

```
$credential = New-Object System.Management.Automation.PSCredential "username", $password  
Initialize-Redis myredis.host.com -Port 1433 -Credential $credential

## Invoke-FlushRedis

### Synopsis
Delete all the keys of the Redis database.

### Syntax
Invoke-FlushRedis \[&lt;CommonParameters&gt;\]

### Note
For more info, see http://redis.io/commands/flushdb


## Ping-Redis

### Synopsis
Pings the Redis instance.

### Syntax
Ping-Redis \[&lt;CommonParameters&gt;\]
