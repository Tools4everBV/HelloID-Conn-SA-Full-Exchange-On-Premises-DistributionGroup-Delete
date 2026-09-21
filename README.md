# HelloID-Conn-SA-Full-Exchange-On-Premises-Distribution-Group-Delete

| :information_source: Information                                                                                                                                                                                                                                                                                                                                                          |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| This repository contains the connector and configuration code only. The implementer is responsible for acquiring the connection details such as username, password, certificate, etc. You might even need to sign a contract or agreement with the supplier before implementing this connector. Please contact the client's application manager to coordinate the connector requirements. |

## Description

_HelloID-Conn-SA-Full-Exchange-On-Premises-Distribution-Group-Delete_ is a template designed for use with HelloID Service Automation (SA) Delegated Forms. It can be imported into HelloID and customized according to your requirements.

By using this delegated form, you can delete distribution groups from Exchange On-Premises. The following options are available:

1.  Search for distribution groups by name, alias, or email address
2.  Select the distribution group to delete from the results
3.  The selected distribution group is validated
4.  The distribution group is deleted from Exchange On-Premises
5.  Audit logging is generated for the deletion action

## Getting started

### Requirements

- **Exchange Management Shell Access**:<br>
  The account used to connect must have appropriate permissions to manage distribution groups in Exchange On-Premises.
- **PowerShell Remoting**:<br>
  PowerShell remoting must be enabled on the Exchange server to allow remote session connections.
- **Exchange On-Premises Server**:<br>
  A working Exchange On-Premises environment with remote PowerShell access enabled.

### Connection settings

The following user-defined variables are used by the connector.

| Setting               | Description                                     | Mandatory |
| --------------------- | ----------------------------------------------- | --------- |
| ExchangeConnectionUri | The URI to connect to Exchange On-Premises      | Yes       |
| ExchangeAdminUsername | The username to connect to Exchange On-Premises | Yes       |
| ExchangeAdminPassword | The password to connect to Exchange On-Premises | Yes       |

## Remarks

### Enhanced Error Handling

- **Detailed Error Messages**: The connector includes comprehensive error tracking with line-by-line error reporting for easier troubleshooting.
- **Action Context**: Each operation includes an `actionMessage` variable that provides context about what action was being performed when an error occurred.

### Performance Optimization

- **Selective Property Loading**: The connector explicitly defines which properties to retrieve from Exchange, reducing memory usage and improving query performance.
- **Targeted Command Import**: Only the necessary Exchange cmdlets are imported (`Get-DistributionGroup`, `Remove-DistributionGroup`), reducing session overhead.

### Search Functionality

- **Multiple Search Criteria**: The data source supports searching by Alias, Name, SamAccountName, or PrimarySmtpAddress for flexible distribution group lookups.
- **Wildcard Support**: Use the wildcard character (\*) to search for all distribution groups or specific patterns.

### Security

- **TLS 1.2 Support**: The connector explicitly enables TLS 1.2 for secure communications.
- **Session Options**: Includes configurable session options for certificate validation and revocation checks.

## Development resources

### API endpoints

The following Exchange PowerShell cmdlets are used by the connector:

| Cmdlet                   | Description                         |
| ------------------------ | ----------------------------------- |
| Get-DistributionGroup    | Retrieve distribution group details |
| Remove-DistributionGroup | Delete a distribution group         |

### API documentation

- [Exchange PowerShell Documentation](https://learn.microsoft.com/en-us/powershell/exchange/exchange-management-shell)
- [Get-DistributionGroup Cmdlet](https://learn.microsoft.com/en-us/powershell/module/exchange/get-distributiongroup)
- [Remove-DistributionGroup Cmdlet](https://learn.microsoft.com/en-us/powershell/module/exchange/remove-distributiongroup)
- [Connect to Exchange Servers using Remote PowerShell](https://learn.microsoft.com/en-us/powershell/exchange/connect-to-exchange-servers-using-remote-powershell)

## Getting help

> :bulb: **Tip:**  
> _For more information on Delegated Forms, please refer to our [documentation](https://docs.helloid.com/en/service-automation/delegated-forms.html) pages_.

## HelloID docs

The official HelloID documentation can be found at: https://docs.helloid.com/
