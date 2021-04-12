---
title: 使用 VBScript 設定預設進程安全性等級
description: 腳本可以使用預設的 WMI 驗證和模擬設定。 不過，腳本可能需要更多安全性的連接，或可能連接到需要加密連接的命名空間。
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195056"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a>使用 VBScript 設定預設進程安全性等級

腳本可以使用預設的 WMI 驗證和模擬設定。 不過，腳本可能需要更多安全性的連接，或可能連接到需要加密連接的命名空間。 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md) 和 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

在最簡單的情況下，腳本可以使用預設的驗證和模擬設定。 WMI 通常會在共用服務主機中執行，並與主機中的其他進程共用相同的驗證。 如果您想要以不同的驗證層級執行 WMI 進程，請使用 [**winmgmt**](winmgmt.md) 命令搭配 **/standalonehost** 參數來執行 wmi，並一般設定 wmi 的驗證層級。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。

下列腳本會使用模擬和驗證層級的預設設定。


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



您也可以在對 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)的呼叫中使用 [名字](constructing-a-moniker-string.md)，並設定預設安全性設定，如下列範例所示。


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



如需在腳本中設定不同的模擬或驗證層級，或設定電腦預設值的詳細資訊，請參閱下列主題：

-   [使用 VBScript 變更預設驗證認證](#changing-the-default-authentication-credentials-using-vbscript)
-   [使用 VBScript 變更預設模擬設定](#changing-the-default-impersonation-levels-using-vbscript)
-   [使用登錄設定預設模擬等級](#setting-the-default-impersonation-level-using-the-registry)
-   [存取 VBScript 中的 SWbemSecurity 物件](#accessing-the-swbemsecurity-object-in-vbscript)
-   [**SWbemSecurity**](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a>使用 VBScript 變更預設驗證認證

您可以使用 [標記](constructing-a-moniker-string.md) 字串和 [**wbemscripting.swbemlocator**](swbemlocator.md) 和 [**SWbemSecurity**](swbemsecurity.md) 物件來變更腳本中的驗證層級。

驗證層級必須根據您要連接的目標作業系統需求來設定。 如需詳細資訊，請參閱 [在不同的作業系統之間進行連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)。

下列 VBScript 程式碼範例示範如何變更腳本中的驗證層級，以從名為 "Server1" 的遠端電腦取得可用空間資料。


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



在 [腳本的標記與 WMI 的連接] 中，使用下表的 "名字/描述" 資料行中顯示的簡短名稱。 例如，在下列腳本中，驗證層級會設定為 **WbemAuthenticationLevelPktIntegrity**。


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



下表列出您可以設定的驗證層級。 這些層級會在列舉 [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)的 >wbemdisp.tlb 中定義。



| 名稱/值                                                      | Description                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WbemAuthenticationLevelDefault**<br/> 0<br/>      | 標記：預設值<br/> WMI 會使用預設的 Windows 驗證設定。 這是建議的設定，可讓 WMI 協調伺服器傳回資料所需的層級。 但是，如果命名空間需要加密，請使用 **WbemAuthenticationLevelPktPrivacy**。<br/> |
| **WbemAuthenticationLevelNone**<br/> 1<br/>         | 標記：無<br/> 不使用驗證。<br/>                                                                                                                                                                                                                                            |
| **WbemAuthenticationLevelConnect**<br/> 2<br/>      | 標記：連接<br/> 只有當用戶端建立與伺服器之間的關聯性時，才會驗證用戶端的認證。<br/>                                                                                                                                                    |
| **WbemAuthenticationLevelCall**<br/> 3<br/>         | 呼叫<br/> 當伺服器收到要求時，只會在每次呼叫的開頭進行驗證。<br/>                                                                                                                                                                                      |
| **WbemAuthenticationLevelPkt**<br/> 4<br/>          | 標記： Pkt<br/> 驗證收到的所有資料都是來自預期的用戶端。<br/>                                                                                                                                                                                                   |
| **WbemAuthenticationLevelPktIntegrity**<br/> 5<br/> | 標記： PktIntegrity<br/> 驗證並確認在用戶端與伺服器之間傳送的資料都沒有修改。<br/>                                                                                                                                                  |
| **WbemAuthenticationLevelPktPrivacy**<br/> 6<br/>   | 標記： PktPrivacy<br/> 驗證所有先前的模擬層級，並加密每個遠端程序呼叫的引數值。 如果您要連接的命名空間需要加密的連接，請使用此設定。<br/>                                               |



 

若要判斷成功的呼叫，請在變更驗證等級之後，檢查傳回值。

例如，由於本機連接一律具有 **wbemAuthenticationLevelPktPrivacy** 的驗證層級，因此下列範例無法設定驗證層級，因為它會連接到本機電腦。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



提供者可以設定命名空間的安全性，如此就不會傳回任何資料，除非您在與該命名空間的連接中使用封包隱私權 (PktPrivacy) 。 這可確保資料會在網路上進行加密。 如果您嘗試設定較低的驗證等級，您將會收到拒絕存取的訊息。 如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)。

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a>使用 VBScript 變更預設模擬等級

當您對 WMI 的腳本 API 進行呼叫時，建議您使用 WMI 為模擬等級提供的預設值。 遠端呼叫和某些具有多個網路躍點的提供者所需的模擬層級比 WMI 使用的更高。 如果模擬層級不足，提供者可能會拒絕要求或提供不完整的資訊。

如果您未設定 SWbemSecurity 中的模擬等級，或是在安全物件上設定 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) ，請設定作業系統的預設 DCOM 模擬等級。 模擬等級必須根據您要連接的目標作業系統需求來設定。 如需詳細資訊，請參閱 [在不同的作業系統之間進行連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)。

下列 VBScript 程式碼範例示範如何變更上述相同腳本中的模擬等級。


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



下表列出 [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) 中使用的驗證層級。



| 名稱/值                                                    | Description                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wbemImpersonationLevelAnonymous**<br/> 1<br/>   | 標記：匿名<br/> 隱藏呼叫端的認證。 對 WMI 的呼叫可能會因為這個模擬等級而失敗。<br/>                                                                                                  |
| **wbemImpersonationLevelIdentify**<br/> 2<br/>    | 標記：識別<br/> 允許物件查詢呼叫端的認證。 對 WMI 的呼叫可能會因為這個模擬等級而失敗。<br/>                                                                                 |
| **wbemImpersonationLevelImpersonate**<br/> 3<br/> | 標記：模擬<br/> 允許物件使用呼叫端的認證。 這是針對 WMI 呼叫編寫腳本 API 的建議模擬等級。<br/>                                                        |
| **wbemImpersonationLevelDelegate**<br/> 4<br/>    | 標記：委派<br/> 允許物件許可其他物件使用呼叫端的認證。 這種模擬適用于 WMI 呼叫的腳本 API，但可能構成不必要的安全性風險。<br/> |



 

下列範例示範如何在取得 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process)程式的特定實例時，在標記字串中設定模擬。


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。

## <a name="setting-the-default-impersonation-level-using-the-registry"></a>使用登錄設定預設模擬等級

如果您可以存取登錄，也可以設定預設的模擬層級登錄機碼。 此索引鍵會指定適用于 WMI 的腳本 API 所使用的模擬層級（除非另有指定）。 下列路徑會識別登錄路徑。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本** \\ **預設模擬等級**

根據預設，登錄機碼會設定為3，指定模擬模擬等級。 某些提供者可能需要較高的模擬層級。

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a>存取 VBScript 中的 SWbemSecurity 物件

您可以設定模擬等級的另一種方式是從 [**SWbemSecurity**](swbemsecurity.md)安全性物件，此物件會顯示為 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemEventSource**](swbemeventsource.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**wbemscripting.swbemlocator**](swbemlocator.md)物件的 [**security \_**](swbemservices-security-.md)屬性。

WMI 會將父物件的安全性設定傳遞至原始物件的子系。 因此，您可以在使用這個物件或從中建立的物件（例如 [**SWbemObject**](swbemobject.md)類型的物件）登入 WMI 和 API 呼叫之後，設定 [**SWbemServices**](swbemservices.md)物件的模擬等級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[保護腳本用戶端](securing-scripting-clients.md)
</dt> </dl>

 

