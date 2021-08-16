---
description: 您可以使用 wmi 腳本類型程式庫，從 Microsoft Visual Studio 和 Windows 腳本主機 w2kmiguser.wsf 檔中呼叫 wmi 腳本 API 方法。
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: 使用 WMI 腳本型別程式庫
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d53f74db0ff4b744077c4e208be52dd749c2f4f150d867c3cfc7214c0e66ae2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120768"
---
# <a name="using-the-wmi-scripting-type-library"></a>使用 WMI 腳本型別程式庫

您可以使用 wmi 腳本類型程式庫，從 Microsoft Visual Studio 和 Windows 腳本主機 w2kmiguser.wsf 檔中呼叫 wmi 腳本 API 方法。

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>使用 WMI 腳本類型程式庫搭配 Microsoft Visual Studio

> [!Note]  
> Visual InterDev 6.0 功能已整合至[Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx)中。

 

下列程式描述如何啟用 (IDE) 的整合式開發環境，以感知 WbemScripting 型別程式庫。

**將 WMI 腳本類型程式庫加入至專案參考**

1.  選取 [ **Project** ] 功能表中的 [**加入參考**]。
2.  在 [ **加入參考** ] 方塊的 [COM] 索引標籤中，選取 [Microsoft WMI 腳本1.2 程式庫]。
3.  如果 [參考] 清單中沒有出現適當的選項，請使用 [**參考**] 方塊中的 **[流覽]** 將它加入。 **流覽** 會開啟 [**新增參考**] 方塊，讓您找出 WbemScripting 型別程式庫。

    WbemScripting 類型程式庫位於% windir% \\ System32 Wbem 目錄中的 >wbemdisp.tlb 檔案。 \\

4.  選取檔案，然後按一下 [開啟]。 [參考] 清單中會顯示 Microsoft WMI 腳本1.2 程式庫。 確定您在清單中選取此專案旁的方塊。

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>使用 WMI 腳本類型程式庫搭配 Windows 腳本主機2。0

您可以在 Windows 腳本主機 w2kmiguser.wsf 檔中包含 **WbemScripting. wbemscripting.swbemlocator** 的參考，而不像撰寫 Visual Basic、腳本撰寫版或其他指令碼語言的腳本。 這可讓您使用常數名稱，而不是值。 例如，在設定驗證時，請使用 **WbemAuthenticationLevelPktPrivacy** ，而不是值6。

腳本可以使用下列方法，與 WMI 類型程式庫的腳本 API 連接：

-   在 VBScript 方法 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 和 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)中指定 WbemScripting GUID。

    這會警示 Windows 腳本主機，以連接至 WMI 物件集。

    下列 VBScript 程式碼範例會建立新的 [**SWbemDateTime**](swbemdatetime.md) 物件。

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   取得新的或現有的物件時，使用 [標記字串](constructing-a-moniker-string.md) "winmgmts："。

    下列 VBScript 程式碼範例會使用 "winmgmts：" 標記來取得具有 **控制碼** 屬性 0 (零) 的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)實例。 **控制碼** 是這個類別的索引鍵屬性。

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   使用 <reference> WSH 2.0 XML 檔案格式的標記參考 WMI 類型程式庫。 如果您使用 <reference> 標記，標記必須有一個 **uuid** 屬性，其值為 WMI 類型程式庫的 **GUID** ，或 (建議) 物件屬性，其值是您可以建立的任何 WMI 腳本物件的 **PROGID** 。

    下列 VBScript 程式碼範例會使用 "WbemScripting" 的 PROGID。 若要執行腳本，請將文字儲存在副檔名為 w2kmiguser.wsf 的檔案中。

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   使用 <**物件**> 標記來建立 WMI 腳本物件。 您可以使用參考您想要建立之 WMI 腳本物件的名稱值來指定 **id** 屬性，讓 **PROGID** 屬性等於 WMI 腳本物件的 PROID。

    下列 WSH 腳本會顯示主機名稱和本機電腦上的處理器數目。 若要執行腳本，請將文字儲存在副檔名為 w2kmiguser.wsf 的檔案中。

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)
</dt> </dl>

 

 
