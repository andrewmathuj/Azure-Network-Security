# Detection - Bastion Brute Force

This query uses Azure Bastion audit logs (`MicrosoftAzureBastionAuditLogs`) to detect potential brute force activity by identifying multiple failed session logins (`Message == "Login Failed"`) from the same source IP against Bastion-fronted VMs within a short window. It groups failures by source IP, surfaces the targeted accounts and VMs, and raises a result when the count meets the configured threshold (default: 5 failures in 15 minutes). Adjust the `lookback` and `threshold` parameters to tune sensitivity for your environment.

## Contributing
 
This project welcomes contributions and suggestions.  Most contributions require you to agree to a

Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us

the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.
 
When you submit a pull request, a CLA bot will automatically determine whether you need to provide

a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions

provided by the bot. You will only need to do this once across all repos using our CLA.
 
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).

For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or

contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
