---
description: 介紹 Windows 檔案總管程式庫和同盟搜尋提供者所使用的搜尋連接器描述架構。
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: 搜尋連接器描述架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8d8ab60ba472cca961a4208b1c551679ef93eacd46e07cf5e080a3e73f3d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226379"
---
# <a name="search-connector-description-schema"></a>搜尋連接器描述架構

介紹 Windows 檔案總管程式庫和同盟搜尋提供者所使用的搜尋連接器描述架構。 架構會指定搜尋連接器描述檔案的結構和需求 (\* searchConnector-ms) 和 Shell 程式庫描述)  (的 **searchConnectorDescriptionType** 元素。 \*

本主題說明與同盟搜尋連接器相關的架構。 如需程式庫和程式庫描述架構的詳細資訊，請參閱連結 [庫描述架構](../shell/library-schema-entry.md)。

本主題包含下列章節：

-   [什麼是搜尋連接器？](#what-are-search-connectors)
-   [搜尋連接器描述檔案的運作方式為何？](#search-connector-description-schema)
-   [什麼是搜尋連接器描述架構？](#what-is-the-search-connector-description-schema)
-   [架構的主要部分有哪些？](#what-are-the-major-parts-of-the-schema)
-   [搜尋連接器描述檔案的範例](#examples-of-search-connector-description-files)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="what-are-search-connectors"></a>什麼是搜尋連接器？

搜尋連接器會將使用者連線到儲存在 web 服務或遠端儲存體位置中的資料。 在 Windows 7 中，使用者可以為位置（例如 web 服務）安裝搜尋連接器，讓他們直接從 Windows 檔案總管搜尋這些位置。 搜尋連接器是搜尋連接器的描述檔案 (\* searchConnector-ms) ，可指定如何連線、傳送查詢，以及從位置接收結果。

除了 web 服務之外，搜尋連接器還可以用來搜尋通訊協定處理常式所建立的本機索引範圍。 例如，使用者可以使用該電子郵件存放區的搜尋連接器，在本機搜尋以 MAPI 通訊協定處理常式編制索引的電子郵件。

## <a name="how-do-search-connector-description-files-work"></a>搜尋連接器描述檔案的運作方式為何？

當使用者的系統上已安裝搜尋連接器描述檔案時，使用者可以開啟 Windows 檔案總管，在流覽窗格中按一下 [搜尋] 連接器，然後輸入搜尋查詢。 WindowsExplorer 會使用搜尋連接器描述檔案中的資訊來傳送查詢，例如要使用的提供者以及搜尋的範圍。 結果會以 RSS 或 Atom 摘要專案的形式傳回，並顯示給使用者，就像是一般的 Shell 專案一樣。

您部署搜尋連接器描述檔案的方式取決於搜尋連接器支援的位置類型：

-   在 OpenSearch 設定 (\* .osdx web 服務的) 檔
-   在通訊協定處理常式安裝過程中

當使用者開啟 .osdx 檔案或安裝通訊協定處理常式時，您應該確保發生下列情況：

-   searchconnector-ms 檔案會建立在使用者的 **Windows 搜尋** 資料夾中 (% userprofile%/Searches) 。
-   在使用者的 [ **連結** ] 資料夾中建立 searchconnector-ms 檔案的快捷方式 (% userprofile%/Links) 。

## <a name="what-is-the-search-connector-description-schema"></a>什麼是搜尋連接器描述架構？

搜尋連接器描述架構是一種 XML 架構，可定義搜尋連接器描述檔案的結構 (\* searchConnector-ms) 。 每個搜尋連接器都必須有搜尋連接器的描述檔案，該檔案會指定如何連線、傳送查詢，以及從位置接收結果。

## <a name="what-are-the-major-parts-of-the-schema"></a>架構的主要部分有哪些？

下表列出架構的主要部分。



| 子元素                                                                         | Description                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | 識別搜尋連接器支援的位置是否為僅限搜尋或搜尋和流覽。                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | 僅供程式庫使用。                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | 僅供程式庫使用。                                                                                                                                                                   |
| [description](search-schema-sconn-description.md)                                     | 描述搜尋連接器。                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | 識別搜尋連接器的自訂圖示位置。                                                                                                                      |
| [imageLink](search-schema-sconn-imagelink.md)                                         | 識別搜尋連接器之自訂縮圖的位置。                                                                                                                 |
| [作者](search-schema-sconn-author.md)                                               | 識別搜尋連接器的作者。                                                                                                                                          |
| [dateCreated](search-schema-sconn-datecreated.md)                                     | 識別建立搜尋連接器的日期。                                                                                                                              |
| [templateInfo](search-schema-sconn-templateinfo.md)                                   | 指定搜尋連接器的資料夾類型。                                                                                                                                       |
| [locationProvider](search-schema-sconn-locationprovider.md)                           | 指定此搜尋連接器要使用的搜尋提供者。                                                                                                                      |
| [範圍 (scope)](search-schema-sconn-scope.md)                                                 | 指定要在搜尋範圍中包含和排除的位置。                                                                                                                |
| [propertyStore](search-schema-sconn-propertystore.md)                                 | 指定此搜尋連接器之 XML 型 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 的位置。 **IPropertyStore** 支援搜尋連接器的 open 中繼資料。 |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | 指定搜尋連接器所表示的位置是否應包含在 [開始] 功能表的搜尋範圍內。                                                                 |
| [域](search-schema-sconn-domain.md)                                               | 識別搜尋連接器的最上層網域。                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | 指定搜尋連接器是否支援 (AQS) 的 Advanced Query 語法。                                                                                                            |
| [isIndexed](search-schema-sconn-isindexed.md)                                         | 指定搜尋連接器所表示的位置是否已編制索引。                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>搜尋連接器描述檔案的範例

以下是同盟搜尋 web 服務的搜尋連接器描述檔案範例。


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



以下是 MAPI 通訊協定處理常式的搜尋連接器描述檔案範例。


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a>其他資源

-   如需程式庫描述架構的詳細資訊，請參閱連結 [庫描述架構](../shell/library-schema-entry.md)。
-   如需安裝搜尋連接器的詳細資訊，請參閱[Windows 中的同盟搜尋](-search-federated-search-overview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Microsoft 下載中心](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
