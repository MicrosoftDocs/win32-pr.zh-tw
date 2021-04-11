---
description: 本主題說明與 Windows Search 相關的技術。
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: 相關搜尋技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112472"
---
# <a name="related-search-technologies"></a>相關搜尋技術

本主題說明與 [Windows Search](-search-3x-wds-overview.md)相關的技術。

本主題的組織方式如下：

-   [企業搜尋](#enterprise-search)
    -   [SharePoint 企業搜尋](#sharepoint-enterprise-search)
-   [Windows 桌面搜尋2。x](#windows-desktop-search-2x)
-   [Platform SDK：索引服務](#platform-sdk-indexing-service)
-   [相關主題](#related-topics)

## <a name="enterprise-search"></a>企業搜尋

如需 [Microsoft 企業搜尋](https://www.microsoft.com/enterprisesearch/en/us/default.aspx)的技術資源總覽，請參閱：

-   [企業搜尋資源中心](https://developer.microsoft.com/office/docs)
-   [Microsoft 企業搜尋的 Blog](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>SharePoint 企業搜尋

SharePoint Foundation 2010 提供 [從伺服器端程式碼查詢](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) ，以及 [從用戶端程式代碼查詢](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14))的查詢。 如需有關查詢、搜尋新內容以及改善與 Sharepoint Server 2010 企業搜尋之相關性的詳細資訊，請參閱 [企業搜尋基礎](/previous-versions/office/ee554857(v=office.14))。

Windows 7 搜尋支援使用 OpenSearch 技術來搜尋遠端資料存放區，讓使用者能夠從 Windows 檔案總管記憶體取遠端資料並與其互動。 SharePoint Search Server 2008 和 MOSS 2007 SP2 也支援使用 OpenSearch 進行遠端伺服器的同盟搜尋。 如需有關使用 Office SharePoint Server 2007 部署搜尋伺服器2008的詳細資訊，請參閱同盟[搜尋 \[ 搜尋伺服器 2008 \] ](/previous-versions/office/bb931109(v=office.14))。 如需 MOSS 多面向搜尋的資訊，其中搜尋結果是依類別 refinded，請參閱 [Codeplex](https://www.codeplex.com/FacetedSearch)。

Windows Search 通訊協定處理常式會使用與 SharePoint Server 類似的設計規格，而且通常可以交換使用。 因此，當使用者需要搜尋舊版資料庫、電子郵件存放區或 Windows Search 不支援的其他資料結構時，您應該先判斷該資料存放區的通訊協定處理常式是否已存在，或許可以與其他應用程式（例如 SharePoint Server）一起使用。 若是如此，您可以在系統上安裝該通訊協定處理常式。

## <a name="windows-desktop-search-2x"></a>Windows 桌面搜尋2。x

強烈建議您不要使用和開發 Microsoft Windows 桌面搜尋)  (的2.x 版。 使用[Windows Search](-search-3x-wds-overview.md)和[Windows Search API](-search-reference-entry-page.md)，而不是使用[Windows Desktop Search](../lwef/-search-2x-wds-overview.md)2.x。

## <a name="platform-sdk-indexing-service"></a>Platform SDK：索引服務

[PLATFORM SDK：索引服務](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) 已從 Windows XP 淘汰。 請改為使用 [Windows Search](-search-3x-wds-overview.md) 並 [Windows Search API](-search-reference-entry-page.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 概觀](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search 開發人員指南](-search-developers-guide-entry-page.md)
</dt> <dt>

[Windows Search 參考](-search-reference-entry-page.md)
</dt> <dt>

[Windows Search 程式碼範例](-search-samples-ovw.md)
</dt> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

[Windows Search 詞彙](search-glossary.md)
</dt> </dl>

 

 
