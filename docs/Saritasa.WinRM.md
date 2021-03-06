
# Saritasa.WinRM

## Get-RemoteTempPath

### Synopsis
Creates a new directory in remote server's %TEMP%.

### Syntax
Get-RemoteTempPath \[-Session\] &lt;PSSession&gt; \[&lt;CommonParameters&gt;\]

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
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Session to be used to access the computer's temp folder.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Initialize-RemoteManagement

### Synopsis
Initialize remote management settings.

### Syntax
Initialize-RemoteManagement \[\[-Credential\] &lt;PSCredential&gt;\] \[\[-Port\] &lt;Int32&gt;\] \[\[-Authentication\] \{Default | Basic |
Negotiate | NegotiateWithImplicitCredential | Credssp | Digest | Kerberos\}\] \[&lt;CommonParameters&gt;\]

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
			<td><nobr>Credential</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Credentials to be used for requests.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Port</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Specify to override default WinRM port.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">0</td>
		</tr>
		<tr>
			<td><nobr>Authentication</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Specify to override preferred authentication mechanism.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Install-WinrmHttps

### Synopsis
Configures server to accept WinRM connections over HTTPS.

### Syntax
Install-WinrmHttps \[\[-CertificateThumbprint\] &lt;String&gt;\] \[-Force\] \[\[-AlternativeDnsNames\] &lt;String\[\]&gt;\]
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
			<td><nobr>CertificateThumbprint</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Certificate thumbprint to be used for securing the connection.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Force</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>If specified, all required properties will be re-installed instead of reusing existing.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
		<tr>
			<td><nobr>AlternativeDnsNames</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Alternative DNS names to be registered with new certificate \(if certificate thumbprint was not provided\).</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Note
For Windows Server 2008 and 2008 R2 you should execute following statement to disable remote UAC:
Set-ItemProperty –Path HKLM:\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System –Name
LocalAccountTokenFilterPolicy –Value 1 –Type DWord
Restart-Computer


## Invoke-RemoteScript

### Synopsis
Executes a script on a remote server.

### Syntax
Invoke-RemoteScript -Path &lt;String&gt; \[-Parameters &lt;Hashtable&gt;\] -ServerHost &lt;String&gt; \[&lt;CommonParameters&gt;\]

Invoke-RemoteScript -Path &lt;String&gt; \[-Parameters &lt;Hashtable&gt;\] -Session &lt;PSSession&gt; \[&lt;CommonParameters&gt;\]

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
			<td><nobr>Path</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Path to script to be executed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Parameters</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Parameters to be passed to specified script.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ServerHost</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Hostname of the machine on which the script should be executed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Session against which the script will be executed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Note
Based on code by mjolinor.
http://stackoverflow.com/a/27799658/991267


## Start-RemoteSession

### Synopsis
Start a new PowerShell session.

### Syntax
Start-RemoteSession \[-ServerHost\] &lt;String&gt; \[&lt;CommonParameters&gt;\]

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
			<td><nobr>ServerHost</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Hostname of the computer.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>
