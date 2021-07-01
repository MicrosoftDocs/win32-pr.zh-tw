---
description: 本節說明 Microsoft Windows 所支援的檔技術。
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: XPS 文件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119983"
---
# <a name="xps-documents"></a>XPS 文件

本節說明 Microsoft Windows 所支援的檔技術。

-   [選擇檔技術](#choosing-a-document-technology)
-   [本節內容](#in-this-section)
-   [XPS 檔工具](#xps-document-tools)
-   [相關主題](#related-topics)


## <a name="choosing-a-document-technology"></a>選擇檔技術

Microsoft 提供數種不同的檔技術來支援各種不同的檔應用程式：

-   **XPS 和 OpenXPS**

    在 Windows 8 和更新版本的 Windows 中，可支援 XPS 和 OpenXPS。 請參閱上圖，以判斷 XPS 和 OpenXPS 的正確使用案例。 如需有關這些檔技術的詳細資訊，請參閱 [Open XML 檔規格 (OpenXPS) ](https://www.ecma-international.org/publications/standards/Ecma-388.htm)。

    在搭配 Windows 8 和 Windows Server 2012 使用 OpenXPS 的情況下，僅透過[XPS 檔 API](documents-xps.md)提供支援

    如果您需要在 Microsoft XPS (MSXPS) 與 OpenXPS 之間進行轉換，Microsoft 提供的工具 (XPSConverter.exe) ，可讓您將 MSXPS 格式的檔轉換成 OpenXPS 格式，反之亦然。 此工具是 Windows 驅動程式套件 (WDK) 的一部分。 若要下載 WDK，請參閱 [如何取得 wdk](/windows-hardware/drivers/download-the-wdk)。

    如需有關 OpenXPS 和 Windows 8 的詳細資訊，請參閱 [Windows 中的 OpenXPS 支援](/windows-hardware/drivers/print/driver-support-for-openxps)。

-   **XPS 檔 API**

    XPS 檔 API 是支援 XPS OM 的原生 Windows API。 XPS 檔 API 是在 Windows 7 中引進的，可用於使用者模式程式和 XPSDrv 印表機驅動程式。

    如需詳細資訊，請參閱 XPS 檔 API 和 [Xps 數位簽章 api](xps-digital-signatures.md)。

    \*Windows Vista （含 Service Pack 2） (SP2) 搭配 windows Vista 和 windows Server 2008 （含 SP2）的平臺更新（使用 Windows Server 2008 的平臺更新），也支援 XPS 檔 API。 如需 Windows Vista 平臺更新或 Windows Server 2008 平臺更新的詳細資訊，請參閱 [Windows vista 的平臺更新。](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)

-   **.NET Framework**

    .NET Framework 將 XPS 檔支援提供給使用者模式、managed 程式碼程式。

    Windows XP Service Pack 2 (SP2) 和更新版本的 Windows 用戶端作業系統，以及 Windows Server 2003 （含 Service Pack 2） (SP2) 和更新版本的 Windows server 作業系統都支援 .NET Framework 3.0。

    Windows 用戶端作業系統的 windows XP 版本以及 Windows Server 2003 和更新版本的 Windows server 作業系統都支援 .NET Framework 3.5。

    > [!Note]  
    > 我們建議您使用 .NET Framework 在用戶端應用程式中建立 XPS 檔，而不是在伺服器應用程式中使用，除非應用程式是以用戶端應用程式的方式定期結束。

     

    如需 .NET Framework 中檔支援的詳細資訊，請參閱 [Windows Presentation Foundation 檔](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85))。

> [!Note]  
> 若要在程式中使用 XPS 檔，請使用原生 XPS 檔 API 或 .NET Framework;不支援在相同的程式中同時使用兩者。

 

## <a name="in-this-section"></a>本節內容

本節說明 Microsoft Windows 支援的原生 Windows 檔技術。



| 檔技術                                                                   | 描述                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [XPS 檔 API](documents-xps.md)<br/>                   | 提供電子紙張的可信任格式。<br/> 本節所述的 XPS 檔 API 可讓程式和 XPSDrv 列印驅動程式存取 XPS 檔的內容和中繼資料。<br/> |
| [XPS 數位簽章 API](xps-digital-signatures.md)<br/> | 啟用檔簽署、簽署簽署者的身分識別，以及指出 XPS 檔在簽署之後是否已經變更。<br/>                                                                          |
| [XPS 檔詞彙](xpsapi-glossary.md)<br/>           | [Xps 檔 api](documents-xps.md)和[XPS 數位簽章 api](xps-digital-signatures.md)所使用的詞彙定義。<br/>                                                                              |



 

## <a name="xps-document-tools"></a>XPS 檔工具

下列工具可協助您進行 XPS 檔檔案的測試和疑難排解。

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    測試檔案對 XML 檔規格 (XPS) 和開放式封裝慣例 (OPC) 規格的符合性。

-   [XpsAnalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    一種命令提示字元工具，可分析 XPS 檔檔是否與 XPS 1.0 規格相容。

-   [PTConform](/previous-versions/dd327476(v=msdn.10))

    檢查 PrintTicket 和 PrintCapabilities 檔有效性的工具。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XPS 列印 API](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[包裝](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[列印](./printdocs-printing.md)
</dt> <dt>
  
[列印範例程式](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 

