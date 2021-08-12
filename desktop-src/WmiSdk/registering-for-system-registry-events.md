---
description: 若要從系統登錄提供者接收通知，管理應用程式必須註冊為暫存事件取用者。
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: 註冊系統登錄事件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c6f60b21dee729a879aaeab676da67b06ca0a822bcfd6509bc0f406f96fecec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554243"
---
# <a name="registering-for-system-registry-events"></a>註冊系統登錄事件

若要從 [系統登錄](/previous-versions/windows/desktop/regprov/system-registry-provider) 提供者接收通知，管理應用程式必須註冊為暫存事件取用者。 註冊 System Registry 提供者的大部分需求與其他任何事件註冊相同，不過您也必須執行下列程式。

登錄提供者會為系統登錄中的事件提供事件類別。 如需一般事件註冊的詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。

下列程式說明如何註冊系統登錄事件。

**註冊系統登錄事件**

1.  呼叫通知查詢方法。

    在腳本或 c + + 中，請使用通知查詢，例如 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 或 [**IWbemServices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)。 針對 **IWbemServices：： ExecNotificationQueryAsync** 的 *bstrQuery* 參數或腳本中的 *strQuery* 建立查詢字串。

2.  決定您想要接收的事件種類，並建立查詢。

    下表列出您可以使用的登錄事件類別。

    

    | 事件類別                                                      | Hive 位置        | 描述                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/A<br/>       | 登錄中變更的抽象基類。<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | 監視索引鍵階層的變更。<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | 監視單一金鑰的變更。<br/>                |
    | [**Registryvaluechangeeven**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | 監視單一值的變更。<br/>              |

    

     

    這些類別具有一個名為 **Hive** 的屬性，可識別要監視的金鑰階層（例如 **HKEY \_ 本機 \_ 電腦**）。

    **HKEY \_ 類別 \_ 根目錄** 和 **HKEY \_ 目前 \_ 使用者** hive 的變更不受 [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)或衍生自它的類別（例如 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)）的支援。

3.  為您的事件註冊建立 WHERE 子句。

    System Registry provider 具有 WHERE 子句的特定規則。 如需詳細資訊，請參閱為登錄 [提供者建立適當的 WHERE 子句](creating-a-proper-where-clause-for-the-registry-provider.md)。 如需有關建立 WHERE 子句的一般資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。

4.  判斷您的取用者是否正在接收事件。

    系統登錄提供者不保證會傳遞所有傳送的事件。 如需詳細資訊，請參閱 [接收登錄事件](receiving-registry-events.md)。

下列 VBScript 程式碼範例說明如何偵測 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** hive 或子樹中的登錄變更。 這是一個監視腳本，基於示範目的，會在名為 Wscript.exe 的進程中執行，直到它在 **工作管理員** 中終止、WMI 已停止或作業系統重新開機。 腳本會使用 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)的 [*半同步*](gloss-s.md)呼叫。 如需有關半同步呼叫的詳細資訊，請參閱 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



下列 VBScript 程式碼範例示範如何藉由登錄登錄提供者事件種類 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)，來監視金鑰值的變更。 腳本會呼叫非同步方法， [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)。 如需非同步呼叫和安全性的詳細資訊，請參閱 [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)。

下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。 若要手動停止腳本，請使用工作管理員停止進程。 若要以程式設計方式停止它，請在 Win32 Process 類別中使用 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) 方法 \_ 。


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

