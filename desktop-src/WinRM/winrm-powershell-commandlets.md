---
title: WinRM Windows PowerShell 命令類別的受控參考
description: Windows 遠端管理 2.0 (WinRM) 可以使用 Windows PowerShell Cmdlet 進行系統管理。 Windows PowerShell Cmdlet 可讓系統管理員設定 WinRM，以及取得資料或管理資源。
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- ConnectWSManCommand
- DisableWSManCredSSPCommand
- DisconnectWSManCommand
- EnableWSManCredSSPCommand
- GetWSManCredSSPCommand
- GetWSManInstanceCommand
- InvokeWSManActionCommand
- NewWSManInstanceCommand
- NewWSManSessionOptionCommand
- RemoveWSManInstanceCommand
- SetWSManInstanceCommand
- SetWSManQuickConfigCommand
- TestWSManCommand
- SessionOption
- 驗證機制
- System.management.automation.remoting.proxyaccesstype
- ProxyAuthentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd74af81c1cec7874ec0e881dbc236f5dd94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187608"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>WinRM Windows PowerShell 命令類別的受控參考

Windows 遠端管理 2.0 (WinRM) 可以使用 Windows PowerShell Cmdlet 進行系統管理。 Windows PowerShell Cmdlet 可讓系統管理員設定 WinRM，以及取得資料或管理資源。

WinRM 的 Windows PowerShell Cmdlet 提供與 WinRM 命令列公用程式相同的功能。 不過，Windows PowerShell 也會執行下列動作：

-   以可擴充且管理導向的指令碼語言，將 WinRM 工作自動化。
-   提供適用于所有管理工作的單一工具。

如需詳細資訊，請參閱 [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) 。

## <a name="ws-management-windows-powershell-classes"></a>WS-Management Windows PowerShell 類別

**命名空間**： Microsoft WsMan. 管理

**元件**： System. Management. Automation

下列 WinRM 命令類別是由 Windows PowerShell 所執行。 這些類別包含在此軟體發展工具組中， (SDK) 僅供完整性之用。 這些類別的成員不能直接使用，也無法用來衍生其他類別。



| 類別                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConnectWSManCommand          | 連線到遠端電腦上的 WinRM 服務。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                              |
| DisableWSManCredSSPCommand   | 停用用戶端上的 CredSSP 驗證。<br/> 如需參數的詳細資訊和範例，請參閱 [WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                           |
| DisconnectWSManCommand       | 從遠端電腦上的 WinRM 服務中斷連線。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [中斷連線-WSMan](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                      |
| EnableWSManCredSSPCommand    | 啟用用戶端上的 CredSSP 驗證。<br/> 如需有關參數的範例和詳細資訊，請參閱 [WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                               |
| GetWSManCredSSPCommand       | 取得用戶端的 CredSSP 相關設定。<br/> 如需有關參數的範例和詳細資訊，請參閱 [WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                         |
| GetWSManInstanceCommand      | 顯示由資源 URI 所指定之資源執行個體的管理資訊。<br/> 如需有關參數的範例和詳細資訊，請參閱 [set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                          |
| InvokeWSManActionCommand     | 在資源 URI 與選取器所指定的目標物件上叫用動作。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                         |
| NewWSManInstanceCommand      | 建立管理資源的新執行個體。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                             |
| NewWSManSessionOptionCommand | 建立 WinRM 會話選項雜湊表以做為下列 WSMan Cmdlet 的輸入參數： [set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true)、 [set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)、 [invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)和 [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true)。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [new-wsmansessionoption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) 。<br/> |
| RemoveWSManInstanceCommand   | 刪除管理資源執行個體。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| SetWSManInstanceCommand      | 修改與資源相關的管理資訊。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                       |
| SetWSManQuickConfigCommand   | 針對遠端管理設定本機電腦。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [>set-wsmanquickconfig](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                                      |
| TestWSManCommand             | 測試 WinRM 服務是否已在本機或遠端電腦上執行。 <br/> 如需有關參數的範例和詳細資訊，請參閱 [Test-WSMan]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                        |
| SessionOption                | 定義 WS-Management 工作階段的一組擴充選項。<br/> 如需有關可能值的範例和詳細資訊，請參閱 [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>WS-Management Windows PowerShell 列舉

下列列舉是由 Windows PowerShell 所執行。 這些列舉包含在此軟體發展工具組中 (SDK) 僅供完整性之用。



| 列舉型別             | 描述                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 驗證機制 | 指定用於伺服器的驗證機制。 <br/> 如需有關可能值的範例和詳細資訊，請參閱 [Connect-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>      |
| System.management.automation.remoting.proxyaccesstype         | 指定尋找 Proxy 伺服器的機制。<br/> 如需有關可能值的範例和詳細資訊，請參閱 [new-wsmansessionoption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) Cmdlet。<br/> |
| ProxyAuthentication     | 指定要在 Proxy 使用的驗證方法。<br/> 如需有關可能值的範例和詳細資訊，請參閱 [new-wsmansessionoption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) Cmdlet。<br/>      |



 

 

