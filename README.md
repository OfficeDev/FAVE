# Firewall and AntiVirus Exclusion (FAVE) migrator

The FAVE tool is a Windows based desktop application that will migrate your firewall rules or av exclusions from other platforms to the Windows Defender platform. The tool is designed to be run on a non-production reference machine so that firewall rules and av exclusions can be converted to the Defender platform. You can safely use the reference machine to migrate, evaluate, and tune the firewall rules and av exclusions. 

FAVE accepts Symantec and McAfee firewall and av exclusion XML exports, ingests them, and converts them into the Windows Defender format.

## Windows Defender Firewall

Firewall migration process:

![image](https://user-images.githubusercontent.com/33558203/161340568-2d00daa5-f782-43e9-b8e6-0f1efd274dd6.png)

## Windows Defender AV exclusions
AV exclusion extraction process:

![image](https://user-images.githubusercontent.com/33558203/161340523-d37ec540-15a7-4c88-b2d0-795a6e0ba72d.png)




## Migration tasks that FAVE performs

In a traditional migration scenario security or IT is tasked with manually creating new firewall rules or av exclusions on the Windows Defender side, by referencing the source firewall rules. FAVE automates the conversion of firewall rules and av exclusions to the Windows Defender format.

- FAVE can scale up your migration project by quickly converting firewall rules and av exclusions
- FAVE exports firewall rules in the [Windows Defender Firewall rule format](https://docs.microsoft.com/en-us/powershell/module/netsecurity/new-netfirewallrule?view=windowsserver2022-ps)
- FAVE can import the converted firewall rules directly into Windows on the reference machine allowing you to quickly assess, evaluate, and tune
- Firewall rules can be exported to wfw format, and then imported into a group policy
- Firewall rules can also be imported from the reference machine into Intune by using the [Endpoint security firewall rule migration tool](https://docs.microsoft.com/en-us/mem/intune/protect/endpoint-security-firewall-rule-tool)
-  FAVE exports av exclusions in the [Windows Defender AV exclusion format](https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/configure-extension-file-exclusions-microsoft-defender-antivirus?view=o365-worldwide)
- AV exclusions can be taken from the FAVE output and placed into a GPO, SCCM, or Intune
- As the migration to the Defender format is a one time action, once firewall rules and/or av exclusions have been migrated the non-production reference machine can be destroyed!

## Getting started

[Download the FAVE user guide](https://github.com/OfficeDev/FAVE/raw/main/FAVE%20-%20User%20Guide.docx) for a walkthrough of how to get started and use FAVE!

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

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
