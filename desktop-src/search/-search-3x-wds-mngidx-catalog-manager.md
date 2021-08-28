---
description: ISearchCatalogManager 和 ISearchCatalogManager2 介面提供管理搜尋目錄的方法，例如造成重新編制索引或設定超時時間。
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: 使用目錄管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc114941f3b9a622012f978e1062d835b5f46eb329be73ae2652b032e5fcfa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937978"
---
# <a name="using-the-catalog-manager"></a>使用目錄管理員

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)和 [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)介面提供管理搜尋目錄的方法，例如造成重新編制索引或設定超時時間。 雖然 Windows Search 目前只使用一個目錄，但這個介面的設計目的是要讓您以更大的控制來管理多個目錄。 介面會以下列方式管理目錄：

- 存取其他介面：抓取編目範圍管理員所需的其他搜尋相關介面、資料變更通知，以及 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面。
- 目錄內容：確保新的資料已編制索引，而且其他應用程式和元件可以正常運作，方法是強制重新編制所有或部分類別目錄的索引，或重設整個目錄。
- 目錄屬性：設定屬性，以決定當連接到通訊協定處理常式時，目錄如何管理時間超時，以及如何在搜尋中處理變音符號標記。
- 目錄狀態-取得目錄的相關資訊，包括狀態、大小和目前的活動狀態。

本主題的組織方式如下：

- [存取相關介面](#accessing-related-interfaces)
- [管理目錄內容](#managing-the-catalog-contents)
- [管理目錄狀態](#managing-catalog-status)
- [管理目錄屬性](#managing-catalog-properties)
- [以提高許可權模式執行](#running-in-elevated-mode)
- [相關主題](#related-topics)

## <a name="accessing-related-interfaces"></a>存取相關介面

Windows Search 平臺中的某些實用介面需要目錄管理員的實例，才能使用這些介面。 若要為指定的目錄建立目錄管理員，請呼叫 [**ISearchManager：： GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) 方法。 然後，您可以使用目錄管理員的方法來具現化並傳回以指定目錄為基礎的介面。

| 方法                                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | 取得目前目錄之 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面的實例，可讓您輕鬆地建立查詢。                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | 取得此搜尋目錄的 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)實例，以讓開發人員修改 Windows Search 索引子的編目範圍。                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | 取得 [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) 介面的實例，用戶端應用程式會在用戶端想要建立專案的索引狀態資訊以支援提供者管理的通知時，用來通知索引子的變更。 如需詳細資訊，請參閱 [通知索引的變更](-search-3x-wds-notifyingofchanges.md) 。 |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | 取得 [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)的實例，用戶端應用程式會在用戶端不想編制索引狀態資訊 (索引子管理的通知) 時，使用此實例來通知索引子的變更。 如需詳細資訊，請參閱 [通知索引的變更](-search-3x-wds-notifyingofchanges.md) 。            |

## <a name="managing-the-catalog-contents"></a>管理目錄內容

有兩個主要工作牽涉到管理目錄：在索引子的編目範圍中重新編制所有或部分 Url 的索引，以及重設整個基礎目錄。 當您重新建立 Url 的索引時，舊資料會保留在目錄中，直到或取代為新資料。 當您重設類別目錄時，會重建整個目錄，並重新編制編目範圍中的所有 Url。 此程式可能需要花費很多時間，而且只能做為解決問題（例如可能損毀的索引）的最後手段。

當您安裝新的應用程式、通訊協定處理常式或篩選器時，安裝應用程式應該將其目錄或根目錄新增至編目範圍，以確保索引子包含該應用程式資料的位置。 如果在索引子將編目範圍編目之後，資料未出現在目錄中，您應該先確定資料的位置包含在編目範圍中。 您可以使用 Windows Search 選項或[編目範圍管理員](-search-3x-wds-extidx-csm.md)的使用者介面來加入它。 如果位置似乎在編目範圍內，您可以使用 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 介面的下列方法，以手動方式在索引子的編目範圍或子集內手動強制重新編制所有 url 的索引。

| 重新編制索引方法                                                                                                                                                                                                                | 描述                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager：：重新索引**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | 重新索引目錄中的所有 Url。 舊的資訊會一直保留到以新資訊取代。                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | 重新編制符合模式的 Url，或從特定的根目錄開始 (例如，file:///C： \\ 資料夾 \\ Subfoldername \\) 。 這適用于 recrawling 特定目錄中的所有專案，或具有特定副檔名的所有專案，就像安裝應用程式時一樣。 |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | 指示索引子使用符合指定模式的 Url 來排列索引編制專案的優先順序，以完成其他編制索引工作。                                                                                                                                    |

**正在重設索引。** 您可以呼叫 [**ISearchCatalogManager：： reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset)來重設整個索引。 這會重設基礎目錄，方法是重建資料庫，並執行編目範圍中所有 Url 的完整索引。 此程式可能需要花費很多時間，而且只能做為解決問題（例如可能損毀的索引）的最後手段。

> [!IMPORTANT]
> 因為這些方法可能會造成索引編制的速度變慢，所以當您嘗試找出索引或類別目錄問題時，應該謹慎使用這些方法。 首先，請確定已在編目範圍管理員中新增您的搜尋根目錄和範圍規則，然後確定檔案和資料夾已正確設定 FANCI 位 (檔案屬性未編制內容索引) 。 如果您已確認這些都是正確的，請先嘗試 ReindexSearchRoot，然後最後再重新編制索引。 如果這兩項工作都沒有，請嘗試重設為最後的手段。

如需相關資訊，請參閱使用 ISearchQueryHelper 來[通知索引變更](-search-3x-wds-notifyingofchanges.md)和[查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)。

## <a name="managing-catalog-status"></a>管理目錄狀態

目錄管理員可以用來取得應用程式的目錄狀態，而這些應用程式想要自訂目錄的管理方式 (例如，自訂「目錄狀態」監視應用程式) 。 但在大部分搜尋相關的開發案例中，通常不需要目錄管理員。 常見用途適用于「目錄狀態」監視應用程式或主控台樣式的應用程式。

下表說明用來管理目錄狀態的 ISearchCatalogManager 方法。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>方法</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a></td>
<td>取得目前正在編制索引的 URL。 如果您嘗試識別索引子是否 &quot; 卡 &quot; 在某個專案上，這個方法會很有用。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a></td>
<td>取得目錄中的專案數。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a></td>
<td>抓取下列有關要編制索引之專案的資訊：
<ul>
<li>plIncrementalCount-要在下一個增量索引中編制索引的專案數</li>
<li>plNotificationQueue-通知佇列中的專案數。 這項資訊對於需要檢查索引子是否接收應用程式傳送通知的通知應用程式很有用。</li>
<li>plHighPriorityQueue-高優先順序佇列中的專案數。 系統會先編制 plHighPriorityQueue 中的專案的索引。</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a></td>
<td>取得目錄的狀態，並傳回可提供目前狀態的列舉值。 以下是可能的目錄狀態：
<ul>
<li>閒置：不需要任何索引。</li>
<li>已暫停：索引會因電池電力偏低或高 CPU 使用量而暫停 (，例如) 。</li>
<li>正在復原：正在復原索引。</li>
<li>完整編目：索引子正在執行爬網範圍的完整編目。</li>
<li>增量編目：索引子正在執行增量編目。</li>
<li>處理通知：索引子正在處理通知。</li>
<li>正在關閉：索引子正在關閉。</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a></td>
<td>取得 <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>ISearchManager：： GetCatalog</strong></a> 方法中指定的目前目錄名稱。 目前唯一支援的目錄是 SystemIndex。</td>
</tr>
</tbody>
</table>

## <a name="managing-catalog-properties"></a>管理目錄屬性

您可以使用目錄管理員來管理三個目錄屬性：

- **區分變音符號。** 文字標記是新增至字母的重音符號，以表示單字的意義或發音。 這個屬性會決定目錄是否區分文字元號，而且在您或您的使用者搜尋和編制多種語言的文字索引時很重要。 例如，將此屬性設定為 **FALSE** 時，目錄會將 "resume" 和 "resumé" 視為相同的單字。
- **連接逾時。** 此屬性代表等待伺服器或資料存放區之連接回應的時間量，以 [**TIMEOUT \_ 資訊**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) 結構表示。 您可以使用這個屬性來微調 Windows Search。
- **資料超時** 這個屬性工作表示等候索引子和通訊協定處理常式或篩選之間的資料交易所需的時間量（以 [**TIMEOUT \_ 資訊**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) 結構表示）。 如果經過這段時間，就會終止篩選背景程式的進程，以防止鎖死和其他資源問題。

最後兩個屬性主要用於未來用途。 每個屬性都有 `get` 和 `put` 方法。

| 方法                                                                                                                                                                                                          | 描述                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**put \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | 如果目錄應以變音符號來區分單字，則為 TRUE。 如果目錄應該忽略變音符號，則 **為 FALSE** 。 變更此屬性需要重建索引，因為索引的索引鍵可能會變成無效。                       |
| [**取得 \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**put \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | 索引子應該等待伺服器或資料存放區之連接回應的時間（以秒為單位）。 如果有許多網站沒有回應，設定過高可能會導致延遲。 設定過低可能會導致某些網站未進行編目。 |
| [**取得 \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**put \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | 索引子應該等候資料交易的時間（以秒為單位）。                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>以提高許可權模式執行

更新 SystemIndex 的任何方法呼叫都需要提高許可權執行您的應用程式。 否則，您的應用程式將會失敗，並出現「拒絕存取」錯誤。

## <a name="related-topics"></a>相關主題


[管理索引](-search-3x-wds-mngidx-overview.md)

[用於管理索引的介面](interfaces-for-managing-the-index.md)

[使用搜尋管理員](-search-3x-wds-mngidx-searchmanager.md)

[使用編目範圍管理員](-search-3x-wds-extidx-csm.md)
