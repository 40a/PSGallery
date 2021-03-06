
# Saritasa.RemoteManagement

## Export-AppPool

### Synopsis
Export information about all app pools to a file.

### Syntax
Export-AppPool \[\[-ServerHost\] &lt;String&gt;\] \[-OutputFilename\] &lt;String&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine with the app pools.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>OutputFilename</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Path where to save the app pools configuration.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Export-Site

### Synopsis
Export information about all web sites to a file.

### Syntax
Export-Site \[\[-ServerHost\] &lt;String&gt;\] \[-OutputFilename\] &lt;String&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine with the web sites.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>OutputFilename</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Path where to save the web sites configuration.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Import-AppPool

### Synopsis
Update app pool information.

### Syntax
Import-AppPool \[\[-ServerHost\] &lt;String&gt;\] \[-ConfigFilename\] &lt;String&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine with the app pools.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ConfigFilename</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Path to config file containing app pool config information.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Import-Site

### Synopsis
Update web site information.

### Syntax
Import-Site \[\[-ServerHost\] &lt;String&gt;\] \[-ConfigFilename\] &lt;String&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine with the web site.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ConfigFilename</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Path to config file containing web site config information.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Import-SslCertificate

### Synopsis
Import provided PFX certificate to target machine.

### Syntax
Import-SslCertificate \[-ServerHost\] &lt;String&gt; \[-CertificatePath\] &lt;String&gt; \[-CertificatePassword\] &lt;SecureString&gt;
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
			<td><nobr>ServerHost</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Hostname of the machine where the certificate should be installed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>CertificatePath</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Path to certificate file on local machine which should be installed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>CertificatePassword</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Password for the specified PFX certificate.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Install-Arr

### Synopsis
Installs Application Request Routing 3.0.

### Syntax
Install-Arr -ServerHost &lt;String&gt; \[&lt;CommonParameters&gt;\]

Install-Arr -Session &lt;PSSession&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Server hostname.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Open WinRM session.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Install-Iis

### Synopsis
Install IIS web server on target machine.

### Syntax
Install-Iis \[-ServerHost\] &lt;String&gt; \[-ManagementService\] \[-WebDeploy\] \[-UrlRewrite\] \[-Arr\] \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine where IIS should be installed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ManagementService</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Whether or not Web Management Service should be installed.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
		<tr>
			<td><nobr>WebDeploy</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Whether or not WebDeploy should be installed.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
		<tr>
			<td><nobr>UrlRewrite</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Whether or not URL Rewrite module should be installed.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
		<tr>
			<td><nobr>Arr</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td></td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">False</td>
		</tr>
	</tbody>
</table>

## Install-MsiPackage

### Synopsis
Install a product using the MSI installer.

### Syntax
Install-MsiPackage -ServerHost &lt;String&gt; \[-ProductName &lt;String&gt;\] -ProductId &lt;String&gt; -MsiPath &lt;String&gt; \[-LocalFeatures
&lt;String&gt;\] \[&lt;CommonParameters&gt;\]

Install-MsiPackage -Session &lt;PSSession&gt; \[-ProductName &lt;String&gt;\] -ProductId &lt;String&gt; -MsiPath &lt;String&gt; \[-LocalFeatures
&lt;String&gt;\] \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine where the package should be installed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Session which should be used to install the module.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ProductName</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Name of the installing product \(will be written to the information log\).</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>ProductId</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Identifying number of the product.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>MsiPath</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Path to the installation file.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>LocalFeatures</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>List of features that are delimited by commas, and are to be installed locally.</td>
			<td class="visible-lg visible-md">false</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg">ALL</td>
		</tr>
	</tbody>
</table>

### Note
Msiexec supports HTTP links.


## Install-UrlRewrite

### Synopsis
Install UrlRewrite module.

### Syntax
Install-UrlRewrite -ServerHost &lt;String&gt; \[&lt;CommonParameters&gt;\]

Install-UrlRewrite -Session &lt;PSSession&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine where the module should be installed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Session which should be used to install the module.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Install-WebDeploy

### Synopsis
Install WebDeploy module.

### Syntax
Install-WebDeploy -ServerHost &lt;String&gt; \[&lt;CommonParameters&gt;\]

Install-WebDeploy -Session &lt;PSSession&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine where the module should be installed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Session which should be used to install the module.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>

## Install-WebManagementService

### Synopsis
Install Web Management Service on target machine.

### Syntax
Install-WebManagementService -ServerHost &lt;String&gt; \[&lt;CommonParameters&gt;\]

Install-WebManagementService -Session &lt;PSSession&gt; \[&lt;CommonParameters&gt;\]

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
			<td>Hostname of the machine where the service should be installed.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
		<tr>
			<td><nobr>Session</nobr></td>
			<td class="visible-lg visible-md"></td>
			<td>Session which should be used to install the service.</td>
			<td class="visible-lg visible-md">true</td>
			<td class="visible-lg">false</td>
			<td class="visible-lg"></td>
		</tr>
	</tbody>
</table>
