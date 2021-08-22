---
title: Windows遠端系統管理和 WMI
description: Windows遠端系統管理可以用來取出 Windows Management Instrumentation 所公開的資料。
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d4fab5cd1ee27f664fc43838a62db949c5892147818466edf649641eff203b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642468"
---
# <a name="windows-remote-management-and-wmi"></a>Windows遠端系統管理和 WMI

Windows遠端系統管理可以用來取出 Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)和[MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)) 所公開的資料。 您可以使用使用 [Winrm 腳本 API](winrm-scripting-api.md) 的腳本或應用程式，或透過 **winrm** 命令列工具，來取得 WMI 資料。

WinRM 支援大部分常見的 WMI 類別和作業，包括內嵌的物件。 WinRM 可以利用 WMI 來收集 [*資源*](windows-remote-management-glossary.md)的相關資料，或管理以 Windows 為基礎的作業系統上的資源。 這表示您可以透過現有的 [WMI 類別](/windows/desktop/WmiSdk/wmi-classes)集，取得有關您企業中之物件（例如磁片、網路介面卡、服務或進程）的資料。 您也可以存取標準 WMI [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)所提供的硬體資料。

## <a name="identifying-a-wmi-resource"></a>識別 WMI 資源

您可以使用 WinRM 中的 [*資源*](windows-remote-management-glossary.md) 或 WS-Management 通訊協定來參考 WMI 類別：受管理的實體類型，例如服務或磁片。

WMI 類別或方法是由 [*URI*](windows-remote-management-glossary.md)所識別，就像使用 WS-Management 通訊協定時的任何其他資源一樣。 URI 可以指定 WMI 資源 (類別) 、WMI 動作 (方法) ，或是在透過網路傳送的 [*訊息*](windows-remote-management-glossary.md) 中識別類別的特定實例。 如需詳細資訊，請參閱 [資源 uri](resource-uris.md)。

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>建立 WMI 類別的 URI 前置詞

URI 前置詞包含固定部分和 WMI 命名空間。 例如，Windows Server 中包含前置詞固定部分的 URI 前置詞為： `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` 。 這可讓您為任何 WMI 命名空間產生 URI 前置詞。 例如，若要存取 **根 \\ 預設** WMI 命名空間，請使用下列 URI 首碼： `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` 。

大部分的管理 WMI 類別都是在 **根 \\ cimv2** 命名空間中。 若要存取 **根 \\ cimv2** 命名空間中的類別和實例，請使用 URI 首碼： `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` 。 如需詳細資訊，請參閱 [資源 uri](resource-uris.md)。

## <a name="generating-a-complete-uri-for-wmi-classes"></a>產生 WMI 類別的完整 URI

您提供給 **Winrm** 命令列工具或腳本的 URI，是由前置詞加上資源規格所組成。

下列程式說明如何產生資源 URI，以取得 WMI 類別或在列舉作業中使用。

**產生 WMI 類別的資源 URI**

1.  以表示應使用 WS-Management 通訊協定架構的前置詞開頭。

    https://schemas.microsoft.com/wbem/wsman/1

    WMI 類別的資源 URI 前置詞一律相同。 如需詳細資訊，請參閱 [URI 首碼](uri-prefixes.md)。

2.  將 WMI 命名空間新增至前置詞。

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  新增類別名稱。

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  若要設定屬性的值，或叫用特定的方法，請為類別新增必要的索引鍵值或值。

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    如果您將金鑰值保留空白，則不會改變原始的屬性值。

    > [!Note]  
    > 將索引鍵值保留空白會將屬性值設定為 **Null**。

     

## <a name="locating-a-wmi-resource-with-winrm"></a>使用 WinRM 找出 WMI 資源

您可以透過命令列工具、 **Winrm**，或透過使用 [winrm 腳本 API](winrm-scripting-api.md)的 Visual Basic 腳本來取得 WMI 資料。 您未使用 [WMI 路徑](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) 來找出資源。 相反地，您會將 WMI 命名空間和階層轉換成 [*URI*](windows-remote-management-glossary.md)。

WMI 類別的 WinRM URI 包含兩個部分： [URI 前置](uri-prefixes.md) 詞和您想要存取的類別。

例如，您可以將下列 URI 提供給 [**會話。列舉**](session-enumerate.md) 方法可列出電腦上的所有服務。 URI 前置詞為 `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` ，而類別是 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

在 WMI 中，以數種方式列出資源或類別的所有實例資料：

-   該資源之所有實例的查詢。

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   呼叫 [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof)或 [**\_ SWbemObject 實例**](/windows/desktop/WmiSdk/swbemobject-instances-)。

    `Set colServices = InstancesOf("Win32_Service")`

在 WinRM 中，有一種方式可列出資源的所有實例： [**Session。列舉**](session-enumerate.md)。


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>尋找 WMI 資源的特定實例

在 WMI 中，您可以藉由指定索引鍵屬性的值，或查詢符合屬性值清單的實例，來指定類別的特定實例。 索引鍵屬性具有 WMI [**金鑰限定詞**](/windows/desktop/WmiSdk/key-qualifier)。

您可以透過數種方式取得類別的特定實例：

-   呼叫 [**Session。**](session-enumerate.md) 使用 *篩選* 和 *方言* 參數列舉來建立查詢。

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   呼叫 [**SWbemServices。 Get**](/windows/desktop/WmiSdk/swbemservices-get)。 若為 [**Session**](session-get.md)，您必須提供一或多個特定的索引鍵值，並在前面加上問號 (？ ) 。

    特定實例之 URI 的格式為 `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` 。

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    WMI 類別可以有一個以上的索引鍵。 索引鍵名稱/值組是以 "+" 符號分隔。 在此情況下，格式為： `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` 。

    取得單一 WMI 物件的 WinRM 語法與 WMI 不同。 Singleton 是定義的 WMI 類別，因此只允許一個實例。 [**Win32 \_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) 或 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) 是 WMI singleton 類別的範例。

    下列 VBScript 程式碼範例會顯示 singleton 的 WMI 語法。

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    下列範例顯示不使用 "@" 的 WinRM singleton 語法。

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   將 [*選取器*](windows-remote-management-glossary.md) 加入至 [**ResourceLocator**](resourcelocator.md) 或 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) 物件。

    下列 VBScript 程式碼範例顯示如何使用選取器來取得特定的 [**Win32 \_ 處理器**](/windows/desktop/CIMWin32Prov/win32-processor)實例。

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[URI 首碼](uri-prefixes.md)
</dt> <dt>

[資源 URI](resource-uris.md)
</dt> <dt>

[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)
</dt> </dl>
