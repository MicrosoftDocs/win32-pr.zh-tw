---
description: 本主題列出針對 Windows 7 引進的新檔。 此處未列出的部分檔也包含新的 Windows 7 內容，例如概念主題，以及現有主題修訂中的新列舉、常數和旗標值。
ms.assetid: 1e6808b0-c00f-46ec-9743-5300117f7d47
title: 適用于 Windows 7 搜尋的新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d088113ad2f0d6d06d9d1c20e1852027fa488b0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981729"
---
# <a name="new-for-windows-7-search"></a>適用于 Windows 7 搜尋的新

本主題列出針對 Windows 7 引進的新檔。 此處未列出的部分檔也包含新的 Windows 7 內容，例如概念主題，以及現有主題修訂中的新列舉、常數和旗標值。

本主題的組織方式如下：

-   [程式碼範例](#code-samples)
-   [概念概覽](#conceptual-overviews)
    -   [同盟搜尋](#federated-search)
    -   [篩選條件](#filters)
    -   [編制索引和查詢索引](#indexing-and-querying-the-index)
    -   [程式庫](#libraries)
-   [列舉](#enumerations)
-   [介面](#interfaces)
-   [Schema 元素](#schema-elements)
-   [結構](#structures)
-   [相關主題](#related-topics)

## <a name="code-samples"></a>程式碼範例



| 主題                                                             | 目錄                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CrawlScopeCommandLine](-search-sample-crawlscopecommandline.md) | CrawlScopeCommandLine 程式碼範例會示範如何定義編目範圍管理員 (CSM) 索引編制作業的命令列選項。<br/>                                                                                           |
| [DSearch](-search-sample-dsearch.md)                             | DSearch 程式碼範例示範如何建立靜態主控台應用程式的類別，以使用 [**ISearchQueryHelper 的**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)來查詢 Windows Search。<br/>      |
| [IFilterSample](-search-sample-ifiltersample.md)                 | IFilterSample 程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的 ifilter 基類。<br/>                                                                                  |
| [OpenSearch](-search-sample-opensearch.md)                       | [OpenSearch 程式碼] 範例示範如何使用 [ [opensearch](https://github.com/dewitt/opensearch) ] 通訊協定建立同盟搜尋服務，以及 ( 的 [ (搜尋) 連接器]) 檔案的 [.osdx]。<br/> |
| [PropertyEdit](-search-sample-propertyedit.md)                   | PropertyEdit 程式碼範例示範如何將標準屬性名稱轉換成 PROPERTYKEY、將屬性存放區的值設定為專案的值，然後將資料寫回檔案資料流程。<br/>                        |
| [ReindexMatchingUrls](-search-sample-reindexmatchingurls.md)     | ReindexMatchingUrls 程式碼範例會示範如何提供三種方式來指定要重新建立索引的檔案：符合檔案類型、mime 類型或指定 WHERE 子句的 Url。<br/>                                                  |
| [SearchEvents](-search-sample-searchevents.md)                   | SearchEvents 程式碼範例會示範如何設定索引事件的優先順序。<br/>                                                                                                                                                       |
| [StructuredQuerySample](-search-sample-structuredquerysample.md) | StructuredQuerySample 程式碼範例示範如何從主控台讀取行、使用系統架構加以剖析，以及顯示產生的條件樹狀結構。<br/>                                                              |
| [WSFromScript](-search-sample-wsfromscript.md)                   | WSFromScript 程式碼範例會示範如何使用 Microsoft ActiveX Data Objects (ADO) ，從 Microsoft Visual Basic 腳本查詢 Windows Search。<br/>                                                                             |
| [WSOleDB](-search-sample-wsoledb.md)                             | WSOleDB 程式碼範例會示範 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取，並示範兩種從 Windows Search 抓取結果的額外方法。<br/>                               |
| [WSSQL](-search-sample-wssql.md)                                 | WSSQL 程式碼範例會示範如何透過結構化查詢語言 (SQL)  (SQL) ，在 Microsoft OLE DB 和 Windows Search 之間進行通訊。<br/>                                                                                         |



 

## <a name="conceptual-overviews"></a>概念概覽

下列領域有 Windows 7 的概念概述。

### <a name="federated-search"></a>同盟搜尋



| 主題                                                                                                         | 目錄                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows 中的同盟搜尋](-search-federated-search-overview.md)                                          | 描述 Windows 7 對遠端資料存放區之搜尋同盟的支援搜尋同盟，這些技術可讓使用者從 Windows 檔案總管記憶體取遠端資料並與其互動。<br/>                                                               |
| [在 Windows 中使用同盟搜尋開始使用](getting-started-with-federated-search-in-windows.md)      | 告訴您如何建立可使用 Windows 同盟搜尋來搜尋的 web 資料存放區，並透過 Windows 檔案總管啟用豐富的遠端資料源整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。<br/>                  |
| [在 Windows 同盟搜尋中連接您的 web 服務](-search-federated-search-web-service.md)           | 描述在您的資料存放區與 Windows 同盟搜尋之間連接 web 服務，以及如何在 RSS 或 Atom 中傳送查詢和傳回搜尋結果時所牽涉到的步驟。<br/>                                                                                  |
| [在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)               | 說明如何讓您的資料存放區可供 [OpenSearch](https://github.com/dewitt/opensearch) web 服務存取，以及如何避免可能的阻礙。<br/>                                                                          |
| [在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md) | 描述如何建立 ( 的 OpenSearch 描述，以將外部資料存放區連接到 Windows 客戶 [端的 .osdx](https://github.com/dewitt/opensearch)) 檔。<br/>                                                              |
| [遵循 Windows 同盟搜尋的最佳作法](-search-fedsearch-best.md)                            | 列出可讓您建立可使用 Windows 同盟搜尋來搜尋之 web 資料存放區的最佳作法，並將您的遠端資料源與 Windows 檔案總管整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。 <br/>   |
| [在 Windows 同盟搜尋中部署搜尋連接器](-search-federated-search-deploying.md)             | 說明如何藉由開啟 ( .osdx) 檔中的 OpenSearch 描述、如何部署 .osdx 檔案，以及如何追蹤您的 [opensearch](https://github.com/dewitt/opensearch) 服務使用方式，來向同盟搜尋註冊新的遠端資料存放區。<br/> |



 

### <a name="filters"></a>篩選器



| 主題                                                                                              | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [開發篩選處理常式](-search-ifilter-conceptual.md)                                       | Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。 您可以藉由撰寫篩選器來解壓縮內容，並使用屬性處理常式來解壓縮檔案的屬性，藉此擴充 Windows Search 來編制新的或專屬檔案類型的索引。<br/>                                                                                                                                                                                                                      |
| [關於 Windows Search 中的篩選處理常式](-search-ifilter-about.md)                               | 篩選處理常式是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行，可掃描檔中的文字和屬性。 篩選處理常式會將這些專案中的文字區塊解壓縮，並篩選出內嵌的格式，並保留文字位置的相關資訊。 它們也會解壓縮值的區塊，也就是檔案屬性。 **IFilter** 是建立高階應用程式的基礎，例如檔索引子和與應用程式無關的檢視器。 <br/>     |
| [在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md) | Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。 您可以藉由撰寫篩選處理常式來將內容解壓縮，並將屬性處理常式解壓縮以解壓縮檔案的內容，藉此擴充 Windows Search 來為新的或專屬的檔案類型編制索引。 篩選器會與檔案類型相關聯，如副檔名、MIME 類型或類別識別碼， (Clsid) 。 雖然一個篩選準則可以處理多個檔案類型，但每個類型只能使用一個篩選準則。<br/> |
| [從篩選處理常式傳回屬性](-search-ifilter-property-filtering.md)               | 您可以使用已註冊的屬性處理常式，或使用針對特定檔案類型註冊的篩選，從專案中解壓縮屬性。 篩選處理常式 ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行) 可以用任意數量的方式解讀檔案類型的內容。<br/>                                                                                                                                                                                                                   |
| [Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)                      | Microsoft 提供數個具有 Windows Search 的標準篩選。 用戶端會呼叫這些篩選器處理常式 (這些是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行，) 從檔中解壓縮文字和屬性。 <br/>                                                                                                                                                                                                                                                                     |
| [在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)         | 說明如何)  ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行，以瞭解篩選處理常式所需的 DLL 結構。<br/>                                                                                                                                                                                                                                                                                                                                                              |
| [註冊篩選處理常式](-search-ifilter-registering-filters.md)                             | 您必須註冊篩選處理常式。 您也可以透過登錄或使用 [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) 介面，找出給定副檔名的現有篩選處理常式。<br/>                                                                                                                                                                                                                                                                                         |
| [測試篩選](-search-ifilter-testing-filters.md)                                             | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)測試套件會驗證您的篩選處理常式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="indexing-and-querying-the-index"></a>編制索引和查詢索引



| 主題                                                                                                   | 目錄                                                                                         |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [在 Windows 7 中編制優先順序和資料列集事件的索引](indexing-prioritization-and-rowset-events.md) | 概述 Windows 7 的索引優先順序和資料列集事件的簡介。<br/> |



 

### <a name="libraries"></a>程式庫



| 主題                                                            | 目錄                                                                                         |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Windows 7 中的程式庫](-search-win7-development-scenarios.md) | 概述 Windows 7 的索引優先順序和資料列集事件的簡介。<br/> |



 

## <a name="enumerations"></a>列舉



| 主題                                                                      | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**案例 \_ 需求**](/windows/desktop/api/Structuredquery/ne-structuredquery-case_requirement)                      | 針對查詢指定關鍵字的案例需求（如果有的話）。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**條件 \_ 建立 \_ 選項**](/windows/desktop/api/Structuredquery/ne-structuredquery-condition_creation_options) | 提供一組要搭配下列介面使用的旗標，以指出條件樹狀節點的類型： [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)、 [**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)、 [**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)、 [**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)和 [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**條件 \_ 運算**](/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation)                | 提供一組要搭配下列方法使用的旗標，以指出 [**ICondition：： GetComparisonInfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo)、 [**ICondition2：： GetLeafConditionInfo**](/windows/desktop/api/Structuredquerycondition/nf-structuredquerycondition-icondition2-getleafconditioninfo)、 [**IConditionFactory：： MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf)、 [**IConditionFactory2：： CreateBooleanLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory2-createbooleanleaf)、 [**IConditionFactory2：： CreateIntegerLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory2-createintegerleaf)、 [**IConditionFactory2：： MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory2-createleaf)、 [**IConditionFactory2：： CreateStringLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory2-createstringleaf)和 [**IConditionGenerator：： GenerateForLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf)中的作業。 <br/> |
| [**條件 \_ 類型**](/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type)                          | 提供一組要搭配下列方法使用的旗標，以指出條件樹狀節點的類型： [**ICondition：： GetConditionType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getconditiontype)、 [**IConditionFactory：： MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor)、 [**IConditionFactory2：： CreateCompoundFromArray**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory2-createcompoundfromarray)和 [**IConditionFactory2：： CreateCompoundFromObjectArray**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory2-createcompoundfromobjectarray)。<br/>                                                                                                                                                                                                                                                                                                          |
| [**優先權 \_ 層級**](/windows/win32/api/searchapi/ne-searchapi-priority_level)                          | [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)介面用來設定或抓取查詢所指定之範圍的目前索引子優先權層級。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)            | 描述項合數據列集搜尋準則的專案目前是否在該資料列集中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ROWSETEVENT \_ 類型**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)                      | 描述資料列集資料的變更類型。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**結構化 \_ 查詢 \_ 語法**](/windows/win32/api/structuredquery/ne-structuredquery-structured_query_syntax)       | 指定查詢語法的類型。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="interfaces"></a>介面



| 主題                                                                  | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)                               | 提供方法來取得搜尋條件的相關資訊。 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)物件表示剖析輸入字串的結果， (使用 [**IQueryParser：:P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse)或 [**IQuerySolution：：) GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery)等方法將輸入字串剖析成搜尋條件節點的樹狀結構。 節點可以是邏輯 AND、OR 或 NOT 來比較子節點，也可以是比較屬性和常數值的分葉節點。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)                             | 擴充 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) 介面的功能。 [**ICondition2**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2) 會提供方法來取得搜尋條件的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)               | 擴充 [**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)的功能。 [**IConditionFactory2**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2) 提供方法來建立或解決透過剖析查詢字串所取得的條件樹狀結構。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)                               | 將資料區塊表示為字串和 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 值。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)                         | 公開接收事件通知的方法。 在 Windows 7 和更新版本中，索引子事件允許資料提供者在其資料列集上接收通知。 利用索引編制事件的提供者能夠以類似實際檔案系統位置的方式來維護其資料列集 (例如，這類非檔案系統位置的程式庫和搜尋) 。 索引子事件是針對程式庫視圖，檔案系統通知是檔案資料夾的流覽。<br/> [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) 必須實作為接收事件的下列通知： [OnChangedItem](/windows/win32/api/searchapi/nf-searchapi-irowsetevents-onchangeditem)、 [OnDeletedItem](/windows/win32/api/searchapi/nf-searchapi-irowsetevents-ondeleteditem)、 [OnNewItem](/windows/win32/api/searchapi/nf-searchapi-irowsetevents-onnewitem) 和 [OnRowsetEvent](/windows/win32/api/searchapi/nf-searchapi-irowsetevents-onrowsetevent)。 [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)和 [**ROWSETEVENT \_ 類型**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)enumeratiors 會分別捕捉專案狀態和資料列集事件。 <br/> |
| [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)         | 設定或抓取此查詢所指定之範圍的目前索引子優先權層級。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) | 擴充 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面的功能。 [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) 提供的方法會通知容器的搜尋引擎進行編目及/或監看，以及在編目或監看時要包含或排除的容器底下的專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="schema-elements"></a>結構描述元素



| 主題                                                                                     | 目錄                                                                                                                                 |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [搜尋連接器描述架構的總覽](search-sconn-desc-schema-entry.md) | 介紹 Windows 檔案總管程式庫和同盟搜尋提供者所使用的搜尋連接器描述架構。<br/> |



 



| 主題                                                                                                                    | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [author 元素 (搜尋連接器架構) ](search-schema-sconn-author.md)                                               | 選擇性 <author> 元素會指定這個文件庫的作者。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                                                                                            |
| [dateCreated 元素 (搜尋連接器架構) ](search-schema-sconn-datecreated.md)                                     | 選擇性 <dateCreated> 元素會使用 ISO 8601 標準來識別建立此搜尋連接器的日期和時間。 它沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                                 |
| [範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope-depth.md)                                           | <depth>元素會指定搜尋連接器的範圍是否應包含子 url。 允許的值有 `Deep` 與 `Shallow`。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                     |
| [ (搜尋連接器架構) 的 description 元素 ](search-schema-sconn-description.md)                                     | 選擇性 <description> 元素指定此搜尋連接器的描述。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                                                                          |
| [網域元素 (搜尋連接器架構) ](search-schema-sconn-domain.md)                                               | 選擇性 <domain> 元素會指定此搜尋連接器所使用之搜尋服務的 URL。 它會顯示在詳細資料窗格中。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                      |
| [folderType 元素 (搜尋連接器架構) ](search-schema-sconn-foldertype.md)                                       | <folderType>元素指定資料夾類型的 GUID。 如果元素存在，則需要這個元素 <templateInfo> 。 它沒有屬性和子項目。<br/>                                                                                                                                                                                                                                        |
| [iconReference 元素 (搜尋連接器架構) ](search-schema-sconn-iconreference.md)                                 | 選擇性 <iconReference> 元素會指定這個位置的自訂圖示。 此元素沒有屬性和子項目。<br/>                                                                                                                                                                                                                                                                                |
| [imageLink 元素 (搜尋連接器架構) ](search-schema-sconn-imagelink.md)                                         | 選擇性 <imageLink> 元素會指定此搜尋連接器的縮圖。 這個元素有一個必要的子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                                                                    |
| [imageLink url 元素 (搜尋連接器架構) ](search-schema-sconn-imagelink-url.md)                                 | <url>元素指定此搜尋連接器的縮圖 URL。 如果 <imageLink> 存在，則需要這個元素。 它沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                                     |
| [includeInStartMenuScope 元素 (搜尋連接器架構) ](search-schema-sconn-includeinstartmenuscope.md)             | 選擇性的布林值 <includeInStartMenuScope> 元素會指定是否應將此搜尋連接器包含在 [開始] 功能表搜尋範圍內。 使用檔案系統作為資料來源之搜尋連接器的預設值是 true，而針對屬性處理常式所使用的搜尋連接器，則預設值為 false。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                           |
| [isDefaultNonOwnerSaveLocation 元素 (搜尋連接器架構) ](search-schema-sconn-isdefaultnonownersavelocation.md) | 選擇性的布林值 <isDefaultNonOwnerSaveLocation> 元素會指定當來自家庭電腦上另一部電腦的使用者選擇儲存專案時，是否應使用搜尋連接器中所述的位置做為預設的儲存位置。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                            |
| [isDefaultSaveLocation 元素 (搜尋連接器架構) ](search-schema-sconn-isdefaultsavelocation.md)                 | 選擇性的布林值 <isDefaultSaveLocation> 元素會指定是否應該使用搜尋連接器中所述的位置做為預設的儲存位置。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                             |
| [isIndexed 元素 (搜尋連接器架構) ](search-schema-sconn-isindexed.md)                                         | 選擇性的布林值 <isIndexed> 元素會指定是否要使用 Windows Search 4 或更高的) ，在本機或遠端 (搜尋連接器所描述的位置進行索引。 本機資料夾的預設值為 true。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                               |
| [isSearchOnlyItem 元素 (搜尋連接器架構) ](search-schema-sconn-issearchonlyitem.md)                           | 布林值 <isSearchOnlyItem> 元素會指定搜尋提供者是否除了搜尋模式之外，還支援瀏覽模式。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。<br/>                                                                                                                                                                                                                  |
| [locationProvider 元素 (搜尋連接器架構) ](search-schema-sconn-locationprovider.md)                           | 選擇性 <locationProvider> 元素會指定 web 服務提供者搜尋連接器要使用的搜尋提供者。 這個元素包含一個強制屬性和一個選擇性的子項目。<br/>                                                                                                                                                                                                          |
| [範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope-mode.md)                                            | <mode>元素指定是否應該在搜尋連接器的範圍中包含或排除 URL。 允許的值有 `Include` 與 `Exclude`。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                            |
| [ (搜尋連接器架構) 的 property 元素 ](search-schema-sconn-locationproviderproperty.md)                           | 選擇性 <property> 元素會指定位置提供者所使用的屬性。 這些屬性是此位置提供者特有的屬性，因此沒有預先定義的名稱組可供使用。 <property>此元素有兩個屬性，如本主題中所述。<br/>                                                                                                                                         |
| [propertyStore (搜尋連接器架構) 的 property 元素 ](search-schema-sconn-propstore-property.md)                | 選擇性 <property> 元素會指定搜尋連接器所使用的屬性。 這些是此搜尋連接器特有的屬性，因此沒有預先定義的名稱組可供使用。 這個元素沒有任何子項目。<br/>                                                                                                                                                                                        |
| [propertyBag 元素 (搜尋連接器架構) ](search-schema-sconn-propertybag.md)                                     | 必要的 <propertyBag> 元素會指定這個位置提供者所使用的一或多個屬性集合。 <br/>                                                                                                                                                                                                                                                                                                        |
| [propertyStore 元素 (搜尋連接器架構) ](search-schema-sconn-propertystore.md)                                 | 選擇性 <propertyStore> 元素會指定以 XML 為基礎之 IPropertyStore 的位置，以儲存此搜尋連接器的開啟中繼資料。 這個元素沒有任何屬性，而且只有一個子項目。<br/>                                                                                                                                                                                                              |
| [範圍元素 (搜尋連接器架構) ](search-schema-sconn-scope.md)                                                 | 選擇性 <scope> 元素會指定專案的集合 <scopeItem> ，這些專案會定義此特定搜尋連接器的範圍包含與排除專案。 如果 <scope> 存在，則必須包含至少一個 <scopeItem> 元素。 這個元素沒有屬性。<br/>                                                                                                                         |
| [scopeItem 元素 (搜尋連接器架構) ](search-schema-sconn-scopeitem.md)                                         | <scopeItem>元素代表排除/包含範圍資料表中的單一專案。 <scopeItem> 藉由新增可控制資料夾包含和排除的三個新元素、控制結果的深度，以及指定範圍的位置，來擴充標準 shellLinkType 類型。 如果 <scope> 元素存在，則需要這個元素。 它有三個子項目，而且沒有任何屬性。<br/> |
| [scopeItem url 元素 (搜尋連接器架構) ](search-schema-sconn-scope-url.md)                                     | <url>元素指定代表搜尋連接器範圍的 URL。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                                                                           |
| [searchConnectorDescriptionType 元素 (搜尋連接器架構) ](search-schema-searchconnectordescription.md)         | <searchConnectorDescriptionType>元素是搜尋連接器定義的最上層容器。 <br/>                                                                                                                                                                                                                                                                                                        |
| [simpleLocation 元素 (搜尋連接器架構) ](search-schema-sconn-simplelocation.md)                               | 專案 <simpleLocation> 會指定以檔案系統為基礎或依通訊協定處理常式為基礎之搜尋連接器的位置。 此元素有兩個子項目，而且沒有任何屬性。<br/>                                                                                                                                                                                                                               |
| [simpleLocation url 元素 (搜尋連接器架構) ](search-schema-sconn-url.md)                                      | <url>元素指定此搜尋連接器的位置 URL。 此值可以是一般 file://URL，如 RFC 1738 (檔中所定義， https://www.ietf.org/rfc/rfc1738.txt) 或使用 knownfolders： protocol 的 url。 這個元素沒有任何子項目，而且沒有任何屬性。<br/>                                                                                                              |
| [supportsAdvancedQuerySyntax 元素 (搜尋連接器架構) ](search-schema-sconn-supportsadvancedquerysyntax.md)     | 布林值 <supportsAdvancedQuerySyntax> 元素會指定搜尋提供者是否支援 [Advanced 查詢語法](-search-3x-advancedquerysyntax.md)。 預設為 false。 這個元素是選擇性的，且沒有任何子項目且沒有任何屬性。<br/>                                                                                                                                                        |
| [templateInfo 元素 (搜尋連接器架構) ](search-schema-sconn-templateinfo.md)                                   | 這個選擇性 <templateInfo> 元素會指定資料夾類型，以顯示透過此搜尋連接器的查詢結果。 這個元素沒有任何屬性，而且只有一個強制子系。<br/>                                                                                                                                                                                                                        |



 

## <a name="structures"></a>結構



| 主題                                | 目錄                                                                                          |
|--------------------------------------|---------------------------------------------------------------------------------------------------|
| [**HITRANGE**](/windows/win32/api/structuredquery/ns-structuredquery-hitrange) | 當查詢搜尋條件符合索引資料時，識別相符資料的範圍。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 7 搜尋](./-search-3x-wds-overview.md)
</dt> <dt>

[在 Windows 7 中編制優先順序和資料列集事件的索引](indexing-prioritization-and-rowset-events.md)
</dt> <dt>

[Windows 7 中的 windows Shell 程式庫](-search-win7-development-scenarios.md)
</dt> </dl>

 

 