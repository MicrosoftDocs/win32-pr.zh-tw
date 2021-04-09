---
description: WMI 腳本可以壓縮 c + + 程式所需的許多步驟。
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: 使用 VBScript 連接至 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850780"
---
# <a name="connecting-to-wmi-with-vbscript"></a>使用 VBScript 連接至 WMI

WMI 腳本可以壓縮 c + + 程式所需的許多步驟。 它們可以連接至 WMI，而不只是透過 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件，也可以透過「winmgmts：」標記。 「名字標記」（namespace）是在 WMI 中尋找命名空間、類別或實例的簡短名稱。 名稱 "winmgmts：" 是告知 Windows Script Host 使用 WMI 物件、連接至預設命名空間，並取得 [**SWbemServices**](swbemservices.md) 物件的 wmi 標記。 其他連接資訊（例如模擬層級或特定類別或實例）會出現在字串後面的 [標記名稱] 中。 您可以在建立或取得 WMI 物件的呼叫中使用名字。 如需詳細資訊，請參閱 [建立標記字串](constructing-a-moniker-string.md)。

下列程式說明如何使用 **wbemscripting.swbemlocator** 連接到 WMI。

**使用 Wbemscripting.swbemlocator 連接到 WMI**

1.  使用 [CreateObject](/previous-versions//xzysf6hc(v=vs.85))的呼叫來取出定位器物件。

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  使用 [**ConnectServer**](swbemlocator-connectserver.md) 方法的呼叫來登入命名空間。

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    如果您未在 [**ConnectServer**](swbemlocator-connectserver.md)的呼叫中指定電腦，則 WMI 會連接到本機電腦。 如果您沒有指定命名空間，則 WMI 會連接到登錄機碼中指定的命名空間。

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本** \\ **預設命名空間**

    預設命名空間是 \\ 根 \\ cimv2。 如需命名空間的詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。

3.  使用 [**SWbemServices \_**](swbemservices-security-.md)方法的呼叫來設定模擬等級。

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

4.  實行腳本的用途。

    WMI 公開各種腳本物件，這些物件是用來存取和操作網路上的資料。 如需詳細資訊，請參閱操作 WMI 的 [類別和實例資訊](manipulating-class-and-instance-information.md) 和 [腳本 API](scripting-api-for-wmi.md)。

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

下列程式描述如何連接至 WMI，並使用標記來取得物件。

**若要連接至 WMI 並使用標記抓取物件**

1.  使用輸入參數中的標記來呼叫 [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) 。

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Moiniker 包含數個您可以用來連線到 WMI 的元素：

    -   "Winmgmts：" 會告知 WSH 使用 [腳本 API 物件](scripting-api-objects.md)。 在此特定範例中，WSH 會知道它應該會傳回描述系統上第一個 Win32 Register-scheduledjob 的 SWbemObject \_ 。 其他可能傳回的物件將會是 SWbemCollection 或 [**SWbemServices**](swbemservices.md) 物件，取決於所述的名字。

    -   您可以選擇性地設定連接的安全性層級。 不過請注意，您不能在標記中設定名稱和密碼資訊。 如需詳細資訊，請參閱 [保護腳本用戶端](securing-scripting-clients.md)。

    -   您可以選擇性地定義 WMI 物件的路徑。 這包括本機或遠端電腦、命名空間，以及類別的名稱。 如需在 WMI 腳本中使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) 的詳細資訊，請參閱 [建立實例](creating-an-instance.md) 和抓取 [wmi 實例](retrieving-an-instance.md)。

2.  除了抓取單一專案或集合，您也可以選擇取出 [**SWbemServices**](swbemservices.md) 物件 (如先前範例) 所述。 之後，您就可以在傳回的物件上呼叫其他查詢。

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    在上述範例中，模擬或 impersonationLevel = 3 是預設的進程安全性層級。 在下列範例中，除非您需要將進程安全性變更為 **委派**，否則不需要指定此進程的安全性層級。 如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
