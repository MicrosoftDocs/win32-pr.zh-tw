---
description: 從 Windows 7，在 url 的處理和剖析中仍有不一致的情況。 本主題提供流覽檔案 URL 格式不一致的限制指南。
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: URL 格式設定需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1bb413501548922eaf1b60801b6d35495d7f8a37dc743675052d4e0e5bae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462230"
---
# <a name="url-formatting-requirements"></a>URL 格式設定需求

從 Windows 7，在 url 的處理和剖析中仍有不一致的情況。 本主題提供流覽檔案 URL 格式不一致的限制指南。

本主題的組織方式如下：

-   [使用中的 URL 格式](#url-formats-in-use)
-   [斜線方向、尾端星號和結尾的斜線敏感度](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [依 API 和查詢的 URL 格式](#url-formats-by-api-and-query)
-   [相關主題](#related-topics)

## <a name="url-formats-in-use"></a>使用中的 URL 格式

協力廠商通訊協定負責定義其 URL 格式，並以符合其標準的方式來定義查詢。 例如，Microsoft Outlook 支援包含任一字元的資料夾名稱，包括 url 中不合法的字元（例如 `"?"` 字元）。 MAPI 通訊協定處理常式會執行其 Url 的 URL 編碼。 因此，索引會儲存 `"%3F"` 而非 `"?"` ，而 Outlook 必須在建立查詢時將此納入考慮。

下表列出不同的格式，每個格式都會被指派一個字母識別碼，以便稍後在本主題中參考它們。



| 識別碼  | 本機檔案 URL 或遠端 | 範例                     |
|-----|--------------------------|-----------------------------|
| A   | 本機                    | file:///c： \\ 測試 \\ 範例\\ |
| B   | 本機                    | file： c：/test/example/       |
| C   | 本機                    | c： \\ 測試 \\ 範例\\         |
| D   | 遠端                   | file:/// \\ \\ 伺服器 \\ 共用\\ |
| E   | 遠端                   | file://server/share/        |
| F   | 遠端                   | \\\\伺服器 \\ 共用\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>斜線方向、尾端星號和結尾的斜線敏感度

在 Windows Search 的斜線方向幾乎沒有任何機密性。 如果接受格式 `c:\test\example` ，則也會接受 c：/test/example。 不過，雖然 [範圍](-search-sql-folderdepth.md) 通常不區分斜線方向，但在遠端 URL 格式 F 的情況下，它對斜線方向是敏感的。因此， `Scope = '//server/share'` 無法運作。

唯一可區分尾端星星並區分 `c:\test\ ` 和 `c:\test\*` 的 API 是 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)。 如果有排除規則 `c:\test\*` ，則 URL 目錄 `c:\test` 本身仍會編制索引。 但是，如果排除 URL 是 `c:\test\` ，則不會 `c:\test` 編制 url 目錄本身的索引。

有兩個地方 Windows Search 可區分尾端斜線： ItemUrl 和 Path 查詢。 如果有目錄 `c:\test` ，Windows Search 會將與 `c:\test\` `c:\test` 和類似的述詞視為不同 `path = 'c:\test'` `System.ItemUrl = 'c:\test'` 。 例如，此述詞 `path='file:c:/test'` 會比對目錄 `c:\test` ，但 `path='file:c:/test/'` 不會因為尾端斜線而不相符。

## <a name="url-formats-by-api-and-query"></a>依 API 和查詢的 URL 格式

下表列出由所選 Api 和查詢接受的本機檔案 URL 格式。 這些格式會與字母 (A 到 F) ，也就是本主題稍早的「[使用中的 URL 格式](#url-formats-in-use)」一節中表示的意義。



| API 或查詢                                                                                                    | 格式化 A | 格式 B | 格式 C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | Y        | N        | Y        |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | Y        | N        | N        |
| [**ISearchCatalogManager2：:P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | Y        | Y        | Y        |
| 範圍 =                                                                                                          | N        | Y        | Y        |
| 目錄 =                                                                                                      | N        | Y        | Y        |
| ItemUrl =                                                                                                        | N        | Y        | Y        |
| 路徑 =                                                                                                           | N        | Y        | Y        |



 

下表列出選取的查詢所接受的遠端檔案 URL 格式。



| 查詢                                                                                                           | 格式 D | 格式 E | 格式 F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/A      | N/A      | N/A      |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/A      | N/A      | N/A      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/A      | N/A      | N/A      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/A      | N/A      | N/A      |
| [**ISearchCatalogManager2：:P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/A      | N/A      | N/A      |
| 範圍 =                                                                                                          | Y        | Y        | Y        |
| 目錄 =                                                                                                      | Y        | Y        | Y        |
| ItemUrl =                                                                                                        | Y        | Y        | Y        |
| 路徑 =                                                                                                           | Y        | Y        | Y        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[索引中包含的內容](-search-indexing-process-overview.md)
</dt> <dt>

[Windows Search 中的編制索引進程](-search-indexing-process-overview.md)
</dt> <dt>

[在 Windows Search 中查詢進程](querying-process--windows-search-.md)
</dt> <dt>

[Windows Search 中的通知處理](-search-3x-wds-support.md)
</dt> </dl>

 

 
