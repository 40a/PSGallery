
# Saritasa.AppDeploy

## Invoke-DesktopProjectDeployment

### Synopsis
Deploys the folder contents to a remote computer.

### Syntax
Invoke-DesktopProjectDeployment \[-Session\] &lt;PSSession&gt; \[-BinPath\] &lt;String&gt; \[-DestinationPath\] &lt;String&gt;
\[\[-BeforeDeploy\] &lt;ScriptBlock&gt;\] \[\[-AfterDeploy\] &lt;ScriptBlock&gt;\] \[\[-OverwriteMode\] \{Backup | Overwrite\}\]
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
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td></td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>BinPath</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Folder path which contents will be copied over</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>DestinationPath</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Folder path where the files should be placed</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>BeforeDeploy</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td></td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>AfterDeploy</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td></td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>OverwriteMode</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The logic which should be used during copy  
If set to Backup, the destination folder first will be backed up and then the files will be transferred  
If set to Overwrite, the destination folder contents will be overwritten with the BinPath fiels</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">Backup</td>
		</tr>
	</tbody>
</table>

### Examples
**EXAMPLE 1**
```
$s = New-PSSession

```
PS C:\\&gt; Invoke-DesktopProjectDeployment $s -BinPath .\\Project\\MyProject\\bin\\Release -DestinationPath  
C:\\inetpub\\www\\myproject -OverwriteMode \[AppDeployOverwriteMode\]::Overwrite  
  
In this example, the contents of MyProject\\bin\\Release folder will be placed on a remote server under myproject folder.  
If this folder already exists, the files in it will be replaced with newest version.  
Files which do exist in destination folder, but not exist in source folder, will not be deleted.

## Invoke-ServiceProjectDeployment

### Synopsis
Deploys a service to a remote computer.

### Syntax
Invoke-ServiceProjectDeployment \[-Session\] &lt;PSSession&gt; \[-ServiceName\] &lt;String&gt; \[-ProjectName\] &lt;String&gt; \[-BinPath\]
&lt;String&gt; \[-DestinationPath\] &lt;String&gt; \[\[-ServiceCredential\] &lt;PSCredential&gt;\] \[&lt;CommonParameters&gt;\]

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
			<td></td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ServiceName</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Name of deploying service on a remote computer</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ProjectName</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>The name of executable which should be used to run the service</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>BinPath</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Folder path containing files which should be deployed</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>DestinationPath</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Destination path on remote computer</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ServiceCredential</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Credentials to be used to create a new service if it does not exist on remote computer</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

### Note
User should have 'Log on as a service right \(https://technet.microsoft.com/en-us/library/cc739424\(v=ws.10\).aspx\).
Local user name example: .\\administrator

Service user accounts: LocalService, NetworkService, LocalSystem
https://msdn.microsoft.com/en-us/library/windows/desktop/ms686005\(v=vs.85\).aspx

Credentials for built-in service user accounts:
New-Object System.Management.Automation.PSCredential\('NT AUTHORITY\\LocalService', \(New-Object
System.Security.SecureString\)\)
New-Object System.Management.Automation.PSCredential\('NT AUTHORITY\\NetworkService', \(New-Object
System.Security.SecureString\)\)
New-Object System.Management.Automation.PSCredential\('.\\LocalSystem', \(New-Object System.Security.SecureString\)\)


### Examples
**EXAMPLE 1**
```
$s = New-PSSession

```
PS C:\\&gt; Invoke-ServiceProjectDeployment $s -ServiceName MyWebSite -ProjectName Web -BinPath  
.\\Project\\MyWebSite\\bin\\Release -DestinationPath C:\\inetpub\\www\\MyWebSite
