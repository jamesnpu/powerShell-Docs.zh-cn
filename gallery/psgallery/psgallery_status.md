---
description: 
manager: carolz
ms.topic: article
author: jpjofre
ms.prod: powershell
keywords: powershell,cmdlet,gallery
ms.date: 2016-10-14
contributor: manikb
title: psgallery_status
ms.technology: powershell
translationtype: Human Translation
ms.sourcegitcommit: e6c526d1074f61154d03b92b6bf6f599976f5936
ms.openlocfilehash: 69df41ae0a9dfd9fb71655cf6334f60f1d39ae94

---

PowerShell 库状态
=========================


## 2016/8/10 - 已解决：无法将电子邮件发送到 cgadmin@microsoft.com

__影响摘要__：2016/8/5 - 2016/8/10 期间，客户不能将电子邮件发送到 cgadmin@microsoft.com，也不能使用“联系我们”功能。  
__根本原因__：工程师确定原因为电子邮件帐户的配置更改。  
__解决办法__：工程师努力解决了配置问题。  
__后续步骤__：如果在此期间使用了“联系我们”链接或向 cgadmin@microsoft.com 发送了电子邮件，但我们没有回复，请重试。 感谢你的耐心等待。



## 2016/7/13 - 下载项目失败

__影响摘要__：2016/7/11 - 2016/7/13 期间，部分客户在从 PowerShell 库下载项目时遇到问题。 该问题可能会表现为从 Install-Module/Install-Script 或 Save-Module/Save-Script 返回的以下错误信息：

```PowerShell
PS C:\> Install-Module xStorage 
PackageManagement\Install-Package : Package 'xStorage' failed to be installed because: 
End of Central Directory record could not be found. At C:\Program 
Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1375 char:21 + ... 
$null = PackageManagement\Install-Package @PSBoundParameters + 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ + CategoryInfo : InvalidResult: 
(xStorage:String) [Install-Package], Exception + FullyQualifiedErrorId : Package '{0}' 
failed to be installed because: {1},Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage 
```

__初始根本原因__：工程师发现 2016/7/11 部署到 PowerShell 库的 Azure Content Deliver Network (CDN) 出现问题。  
__缓解__：工程师在 PowerShell 库中禁用 Azure CDN。  
__后续步骤__：调查根本原因并制定解决方案，防止将来再次发生。


## 2016/5/19 - 下载项目失败
__影响摘要__：2016/5/17 - 2016/5/19 期间，部分客户从 PowerShell 库下载项目时遇到问题。 该问题可能会表现为从 Install-Module/Install-Script 或 Save-Module/Save-Script 返回的以下错误信息：

```PowerShell
VERBOSE: Hash for package 'AzureRM.OperationalInsights' does not match hash provided from the server.
VERBOSE: InstallPackageLocal' - name='AzureRM.OperationalInsights', version='1.0.8',
destination='C:\Users\jbritt\AppData\Local\Temp\2\1741355729'
WARNING: Package 'AzureRM.OperationalInsights' failed to be installed because: 
End of Central Directory record could not be found. 
WARNING: Dependent Package 'AzureRM.OperationalInsights' failed to install. 
WARNING: Package 'AzureRM' failed to install. 
VERBOSE: Module 'AzureRM.Network' was saved successfully. 
VERBOSE: Saving the dependency module 'AzureRM.NotificationHubs' with version '1.0.8' for the 
module 'AzureRM'. 
VERBOSE: Module 'AzureRM.NotificationHubs' was saved successfully. 
PackageManagement\Save-Package : Unable to save the module 'AzureRM'. At C:\Program 
Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1187 char:21 + 
$null = PackageManagement\Save-Package @PSBoundParameters + 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ + 
CategoryInfo : InvalidOperation: (Microsoft.Power...ets.SavePackage:SavePackage) 
[Save-Package], Exception + FullyQualifiedErrorId : ProviderFailToDownloadFile,
Microsoft.PowerShell.PackageManagement.Cmdlets.SavePackage 
```

__初始根本原因__：工程师发现 2016/5/17 部署到 PowerShell 库的 Azure Content Deliver Network (CDN) 的基础提供程序中断。  
__缓解__：工程师在 PowerShell 库中禁用 Azure CDN。  
__后续步骤__：调查根本原因并制定解决方案，防止将来再次发生。




<!--HONumber=Oct16_HO2-->


