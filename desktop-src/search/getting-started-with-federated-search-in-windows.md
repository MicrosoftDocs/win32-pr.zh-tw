---
description: 使用 OpenSearch 技術對遠端資料存放區進行搜尋同盟的 Windows 7 支援，可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: 在 Windows 中使用同盟搜尋開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511085"
---
# <a name="getting-started-with-federated-search-in-windows"></a>在 Windows 中使用同盟搜尋開始使用

使用 OpenSearch 技術對遠端資料存放區進行搜尋同盟的 Windows 7 支援，可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。 您可以建立可使用 Windows 同盟搜尋來搜尋的 web 資料存放區，並透過 Windows 檔案總管啟用豐富的遠端資料源整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。

本主題的組織方式如下：

-   [什麼是同盟搜尋？](#what-is-federated-search)
-   [建立同盟搜尋的步驟](#steps-for-building-federated-search)
-   [同盟搜尋的運作方式](#how-federated-search-works)
-   [在 RSS 或 Atom 中傳送查詢並傳回搜尋結果](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [同盟搜尋範例](#federated-search-examples)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="what-is-federated-search"></a>什麼是同盟搜尋？

Windows 7 支援透過 [OpenSearch](https://github.com/dewitt/opensearch) 通訊協定，將外部來源連接到 windows 用戶端。 這可讓使用者搜尋遠端資料存放區，並從 Windows 檔案總管內查看結果。 [OpenSearch](https://github.com/dewitt/opensearch) v1.1 標準定義了簡單的檔案格式，可用來描述用戶端應該如何查詢資料存放區的 web 服務，以及服務應該如何傳回結果以供用戶端轉譯。 Windows 同盟搜尋會連接到接收 [OpenSearch](https://github.com/dewitt/opensearch) 查詢的 web 服務，並以 RSS 或 Atom XML 格式傳回結果。

下列螢幕擷取畫面說明從遠端搜尋 SharePoint 網站之後所取得的搜尋結果。

![顯示 windows explorer 中所顯示的 sharepoint 網站搜尋結果的螢幕擷取畫面](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>建立同盟搜尋的步驟

若要建立同盟搜尋，請執行下列步驟：

1.  提供可傳回 RSS 或 Atom 格式之結果的 [OpenSearch](https://github.com/dewitt/opensearch)相容 web 服務，讓您可以從 Windows 檔案總管搜尋資料存放區。
2.  建立 .osdx) 檔案的 OpenSearch ( 描述，以描述如何連接至 web 服務，以及如何對應 RSS 或 Atom XML 中的任何自訂元素。
3.  使用 .osdx 檔案將搜尋連接器部署至 Windows 用戶端電腦。

下圖說明建立同盟搜尋的步驟。

![建立同盟搜尋的流程圖表](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>同盟搜尋的運作方式

Windows 檔案總管和您的 [OpenSearch](https://github.com/dewitt/opensearch) web 服務之間的通訊是透過 Windows 資料層執行。 Windows 資料層可透過 Windows 存放區提供者與不同類型的資料存放區進行通訊。 每個提供者都專門與支援特定通訊協定並具有特定功能的資料存放區進行通訊。 例如，下圖說明瞭 [OpenSearch](https://github.com/dewitt/opensearch) 提供者如何與提供支援 [OpenSearch](https://github.com/dewitt/opensearch) 標準之 web 服務的資料存放區進行通訊。

![顯示從用戶端上的 windows explorer 透過遠端伺服器上的 opensearch 資料存放區進行通訊的圖表](images/windowssearchfederationfunctionality.png)

若要讓您的資料存放區支援 Windows 7 中的同盟搜尋，您必須執行一些工作。 下表列出啟用資料存放區的工作、完成每項工作所需的作業，以及可在何處找到檔。



| Task                                                                                                     | 需求                                                                                                                                                                                            | 文件                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 讓 Windows 檔案總管搜尋您的資料存放區。<br/>                                    | 建立與 OpenSearch 相容的 web 服務。<br/>  ( .osdx) 檔案中建立 [OpenSearch 描述]。<br/>                                                                                       | [在 Windows 同盟搜尋中連接您的 web 服務](-search-federated-search-web-service.md)<br/> [在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)<br/> |
| 主動將 web 服務部署至企業內的使用者。<br/>                               | 將 .osdx 檔案提供給您的使用者、將它複製到本機，然後透過快捷方式讓使用者存取。<br/>                                                                                     | [在 Windows 同盟搜尋中部署搜尋連接器](-search-federated-search-deploying.md)<br/>                                                                                                              |
| 在 Windows 檔案總管中列舉搜尋結果，以回應查詢。<br/>                          | 執行可接受查詢字串，並以 RSS 或 Atom 格式傳回結果的 web 服務。<br/>                                                                                              | [在 Windows 同盟搜尋中連接您的 web 服務](-search-federated-search-web-service.md)<br/>                                                                                                            |
| 讓使用者將您的資料存放區新增至其 Windows 檔案總管。<br/>                                | 建立 .osdx 檔案，並將它提供給您的使用者。<br/>                                                                                                                                           | [在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)<br/>                                                                                                                |
| 在 Windows 檔案總管中，將您的專案顯示為類似檔的專案。<br/>                                    | 使用 **主機殼** 或媒體來傳回檔案或內容資料流程的 URL **： content** 元素<br/> 提供用戶端電腦可識別的副檔名或 MIME 類型。<br/> | [在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)<br/>                                                                                                                |
| 除了 RSS 或 Atom 標準所定義的屬性外，也會顯示 Windows 檔案總管中的自訂屬性。<br/> | 在 RSS/Atom 輸出中使用另一個 XML 命名空間，以提供額外的中繼資料。<br/> 將屬性對應新增至 .osdx 檔案。<br/>                                                       | [在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| 自訂 Windows 檔案總管中的專案所顯示的屬性。<br/>               | 將 proplist 對應新增至 .osdx 檔案。<br/>                                                                                                                                                   | [在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| 在預覽窗格中顯示專案的自訂網頁流覽。<br/>                              | 傳回相異的連結與主機殼值。<br/> 將 URL 值對應至 **WebPreviewUrl** Windows Shell 屬性。<br/>                                                               | [在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| 在 Windows 檔案總管中顯示 [命令列] 按鈕，此按鈕會將查詢向前復原到您的網站。<br/>   | `Url format="text/html"`在 .osdx 檔案中提供範本。<br/>                                                                                                                              | [在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>在 RSS 或 Atom 中傳送查詢並傳回搜尋結果

當使用者在 Windows 檔案總管右上角的 [搜尋] 方塊中輸入字詞時，查詢會傳送至 [ [OpenSearch](https://github.com/dewitt/opensearch) 提供者]，然後將查詢傳送到遠端資料存放區。 遠端 web 服務會回應查詢，方法是在 XML 檔（通常稱為摘要）中提供結果，其中有兩種支援的格式 (RSS 或 Atom) 。 摘要中的每個結果專案都包含 XML 子項目，以代表或描述專案中繼資料，例如標題、URL、描述、縮圖影像等等。 [ [OpenSearch](https://github.com/dewitt/opensearch) 提供者] 負責將 XML 元素值對應至 windows 應用程式可以使用的 windows Shell 系統屬性。

## <a name="federated-search-examples"></a>同盟搜尋範例

下列範例 ( 的 [OpenSearch]) 檔案 `ShortName` 是由和元素所組成 `Url` ，這是透過 [OpenSearch] 通訊協定將外部資料存放區連接到 Windows 用戶端的最低必要子項目。


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



下列範例說明如何以 RSS 格式來搜尋可供 web 使用的資料存放區，以及如何指定要傳回的一個搜尋專案：


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



下列範例說明如何將屬性對應至預設的系統屬性，以便排序和分組顯示的專案：


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



下列範例說明如何將縮圖影像顯示新增至 Windows 檔案總管中的每個專案：


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>其他資源

如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](-search-federated-search-overview.md)的「其他資源」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

[在 Windows 同盟搜尋中連接您的 web 服務](-search-federated-search-web-service.md)
</dt> <dt>

[在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)
</dt> <dt>

[在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)
</dt> <dt>

[遵循 Windows 同盟搜尋的最佳作法](-search-fedsearch-best.md)
</dt> <dt>

[在 Windows 同盟搜尋中部署搜尋連接器](-search-federated-search-deploying.md)
</dt> </dl>

 

 




