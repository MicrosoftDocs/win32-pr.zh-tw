---
description: 您可以建立連線物件來建立與 WMI 的遠端連線。 此物件包含電腦的名稱、您想要連接的 WMI 命名空間，以及任何相關的認證和驗證層級。
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: 使用 VBScript 從遠端連線至 WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982354"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>使用 VBScript 從遠端連線至 WMI

您可以建立連線物件來建立與 WMI 的遠端連線。 此物件包含電腦的名稱、您想要連接的 WMI 命名空間，以及任何相關的認證和驗證層級。

**使用 VBScript 連接到遠端系統**

1.  指定連接資訊，例如遠端電腦名稱稱、認證，以及連線的驗證層級。

    如果您要使用相同的認證連接到遠端電腦 (網域和使用者名稱) 您登入時，您可以在 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[名字](constructing-a-moniker-string.md)中指定連接資訊，如下列程式碼範例所述。

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    一般來說，您應該指定要在遠端電腦上連接的 WMI 命名空間。 這是因為在不同的電腦上，預設命名空間可能不相同。 指定命名空間可確保您連接至所有電腦上的相同命名空間。

    如需 VBScript 常數的詳細資訊，以及使用 [標記] 連接的腳本字串，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

2.  如果您連接到不同網域中的遠端電腦，或是使用不同的使用者名稱和密碼，則必須使用 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 方法。

    如同使用標記，您可以使用 **ConnectServer** 來指定認證、驗證層級，以及遠端連線的命名空間。 下列程式碼範例說明如何使用 ConnectServer 來存取使用系統管理員帳戶和密碼的遠端電腦。

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  針對遠端連線使用 [**ConnectServer**](swbemlocator-connectserver.md) 函式時，請在對 [**SWbemServices**](swbemservices-security-.md)的呼叫所取得的安全性物件上設定模擬和驗證。 您可以使用列舉 [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) 來指定模擬層級。

    下列程式碼範例會設定舊版 VBScript 程式碼範例的模擬等級。

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    請注意，某些連接需要特定的驗證層級。 如需詳細資訊，請參閱 [設定用戶端應用程式流程安全性](setting-client-application-process-security.md) 和 [保護腳本用戶端](securing-scripting-clients.md)。

    尤其是，如果您要在遠端電腦上連接的命名空間需要加密連線才能傳回資料，則您應該將驗證層級設定為 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 或6。 您也可以使用此驗證等級，即使命名空間不需要它也一樣。 這可確保資料會在網路上進行加密。 如果您嘗試設定較低的驗證等級，則會傳回拒絕存取訊息。 如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

建立連線之後，您可以繼續存取 WMI 資料。 如需詳細資訊，請參閱 [腳本和應用程式的 WMI](wmi-tasks-for-scripts-and-applications.md)工作。

## <a name="examples"></a>範例

如需更大的 VBScript 範例，請參閱 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 參考頁面中的範例一節。

下列 VBScript 程式碼範例會藉由建立遠端電腦名稱稱陣列，然後在每部電腦上顯示隨插即用裝置（ [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)的實例）的名稱，連接到同一網域中的一組遠端電腦。 若要執行下列腳本，您必須是遠端電腦上的系統管理員。 請注意，在 [模擬 \\ \\ 等級] 設定之後，腳本會新增遠端電腦名稱稱之前所需的 ""。 如需 WMI 路徑的詳細資訊，請參閱 [描述 Wmi 物件的位置](describing-the-location-of-a-wmi-object.md)。


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



下列 VBScript 程式碼範例可讓您使用不同的認證連接到遠端電腦。 例如，位於不同網域的遠端電腦，或是連接到需要不同使用者名稱和密碼的遠端電腦。 在此情況下，請使用 [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) 連接。


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
