---
description: .
ms.assetid: 8a025bee-65e1-40a7-a269-72a93aca827b
title: 搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c459f59c2a4e9112c35a402eb1fd9f83883cd594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386128"
---
# <a name="search"></a>搜尋

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AutoSummary](./props-system-search-autosummary.md)<br/>                                         | 檔全文檢索的自動化搜尋系統摘要，會顯示在 **Search Explorer** 的搜尋結果查看中。 只有當取用應用程式中的值，而不是提供值給屬性處理常式時，才使用此屬性。<br/>                                                                                                     |
| [ContainerHash](./props-system-search-containerhash.md)<br/>                                     | 雜湊程式碼，用來識別要依據一般容器 url 刪除的附件。<br/>                                                                                                                                                                                                                                                                         |
| [搜尋. 內容](./props-system-search-contents.md)<br/>                                               | 專案的內容。 <br/>                                                                                                                                                                                                                                                                                                                                        |
| [System.servicemodel](./props-system-search-entryid.md)<br/>                                                 | Windows Search 索引中給定目錄內之專案的專案識別碼。<br/>                                                                                                                                                                                                                                                                                      |
| [ExtendedProperties](./props-system-search-extendedproperties.md)<br/>                           |                                                                                                                                                                                                                                                                                                                                                                              |
| [GatherTime](./props-system-search-gathertime.md)<br/>                                           | 日期時間值，表示 Windows Search 收集程式最後將此檔的屬性推送至 Windows Search 收集程式外掛程式的時間。<br/>                                                                                                                                                                                                 |
| [擊中數](./props-system-search-hitcount.md)<br/>                                               | 在 Windows Search 索引上使用 CONTAINS 時，這是詞彙的相符專案數。 如果有多個包含，會計算最少的點擊次數，或計算最大的點擊次數。<br/>                                                                                                                                          |
| [IsClosedDirectory](./props-system-search-iscloseddirectory.md)<br/>                             | 由容器專案發出為 **TRUE** ，表示如果容器專案自上次增量索引驗證編目之後未變更，索引子就不需要列舉其子專案。 這有助於優化索引子效能。<br/>                                                                                       |
| [IsFullyContained](./props-system-search-isfullycontained.md)<br/>                               | 由容器的所有子專案發出為 **true** (例如電子郵件或副檔名為 .zip 的壓縮檔案) ，會發出 [IsClosedDirectory](./props-system-search-iscloseddirectory.md) 為 **true**。 這可確保子專案包含在搜尋索引中。<br/>                                                              |
| [QueryFocusedSummary](./props-system-search-queryfocusedsummary.md)<br/>                         | 檔的查詢焦點摘要。<br/>                                                                                                                                                                                                                                                                                                                        |
| [QueryFocusedSummaryWithFallback](./props-system-search-queryfocusedsummarywithfallback.md)<br/> | 檔的查詢焦點摘要。 如果沒有可用的，則會傳回 AutoSummary。<br/>                                                                                                                                                                                                                                                                     |
| [QueryPropertyHits](props-system-search-querypropertyhits.md)<br/>                                    | 包含查詢中相符屬性的清單。<br/>                                                                                                                                                                                                                                                                                                             |
| [System. Rank](./props-system-search-rank.md)<br/>                                                       | 資料列的關聯次序，範圍從0-1000。 <br/>                                                                                                                                                                                                                                                                                                                 |
| [System.Search.Store](./props-system-search-store.md)<br/>                                                     | 產生專案之通訊協定處理常式的識別碼。 例如，MAPI、CSC、FILE 等等。<br/>                                                                                                                                                                                                                                                          |
| [UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))<br/>                                           | 由容器 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 針對容器內的每個子 URL 發出。 如果子系是在範圍內，則索引子最後會將子系編目。<br/>                                                                                                                                                                                |
| [UrlToIndexWithModificationTime](./props-system-search-urltoindexwithmodificationtime.md)<br/>   | 這個屬性與 [**UrlToIndex**](props-system-search-urltoindex.md) 相同，不同之處在于它包含上次修改 URL 的時間。 這是索引子的優化，因此不需要回呼至通訊協定處理常式來要求這項資訊，以判斷是否需要重新編制內容的索引。 <br/> |



 

 

 
