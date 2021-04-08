---
title: 從本機電腦取得資料
description: 雖然 Windows 遠端管理和 WS-Management 通訊協定是針對遠端通訊明確設計，但是在本機電腦上建立會話是最簡單的情況。
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682384"
---
# <a name="obtaining-data-from-the-local-computer"></a>從本機電腦取得資料

雖然 Windows 遠端管理和 WS-Management 通訊協定是針對遠端通訊明確設計，但是在本機電腦上建立會話是最簡單的情況。 某些腳本可能需要在本機電腦和遠端電腦上存取資料。

**WinRM 2.0 版：  **

所有作業都會被視為遠端，而且必須先啟動 WinRM 服務，才能執行任何操作。 如果未指定遠端目的地，則預設會使用 localhost，而且所有作業都會傳送至本機 WinRM 服務。 如需啟動 WinRM 服務的詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。

使用 WinRM 服務進行本機作業時，應該考慮下列因素：

-   本機 WinRM 設定只能由系統管理員讀取。
-   WMI 命名空間必須設定遠端啟用許可權。 如需詳細資訊，請參閱 [保護遠端 WMI 連接](../wmisdk/securing-a-remote-wmi-connection.md)。
-   如果 [*未建立 winrm 接聽*](windows-remote-management-glossary.md) 程式，則 winrm 服務會接聽埠47001上的本機要求。

每個 WinRM 腳本都必須先藉由建立 [**會話**](session.md) 物件來建立會話或連接到電腦。 建立會話之後，您可以使用 **會話** 物件方法（例如 [**session. 列舉**](session-enumerate.md) 或 [**session. Invoke**](session-invoke.md) ）來取得資料或執行方法。

建立會話有點 [類似于連線至 Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) 命名空間。 此會話基本上是一層，可讓您透過 [*SOAP*](windows-remote-management-glossary.md) 訊息和 WS-Management 的通訊協定來傳送和接收資料。 如需詳細資訊，請參閱 [WS-Management 通訊協定](ws-management-protocol.md)。

呼叫 [**CreateSession**](wsman-createsession.md) 方法來建立 [**會話**](session.md) 物件將會啟動連接到本機 WinRM 的 [*會話*](windows-remote-management-glossary.md) 。

**建立 WSMan 會話並取得資料**

1.  建立 [**WSMan**](wsman.md) 物件。

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  藉由呼叫 [**WSMan. CreateSession**](wsman-createsession.md) 方法來建立會話。 此會話會以您的登入使用者名稱和密碼執行，並可透過本機 WinRM 取得資料。

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  建立資源 [*URI*](windows-remote-management-glossary.md) 來識別您想要管理的資源，或您想要為其取得資料的 [*資源*](windows-remote-management-glossary.md) 。 如需有關如何格式化 URI 的詳細資訊，請參閱 [資源 uri](resource-uris.md)。 此資源 URI 適用于 WMI [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別的特定實例，也就是 Winmgmt 服務。 如需詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  呼叫使用資源 URI 取得或列舉資料的 [**會話**](session.md) 方法。 如需詳細資訊，請參閱 [WinRM 腳本 API](winrm-scripting-api.md)。

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  若要從另一部電腦取得或管理資料，或使用不同的驗證方法，請參閱 [從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)。

下列 VBScript 程式碼範例顯示完整的腳本，該腳本會取得名為 "Winmgmt" 的 WMI [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 的特定實例。


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



下列 VBScript 程式碼範例顯示具有資料轉換的完整腳本。 如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理參考](windows-remote-management-reference.md)
</dt> </dl>

 

 