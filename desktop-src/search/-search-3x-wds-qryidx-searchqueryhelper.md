---
description: 您可以使用 ISearchQueryHelper 介面來查詢索引。 這個介面會實作為 helper 類別，以 ISearchCatalogManager (和 ISearchCatalogManager2) ，而且是藉由呼叫 ISearchCatalogManager：： GetQueryHelper 取得。
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: 使用 ISearchQueryHelper 查詢索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191207"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a>使用 ISearchQueryHelper 查詢索引

您可以使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面來查詢索引。 這個介面會實作為 helper 類別，以 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (和 [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) ，而且是藉由呼叫 [**ISearchCatalogManager：： GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)取得。 此介面允許您：

-   取得連接到 Windows Search 資料庫 OLE DB 連接字串。
-   將 Advanced Query 語法 (AQS) 使用者查詢轉換成 Windows Search 結構化查詢語言 (SQL)  (SQL) 。
-   指定可在 SQL 中表示但無法在 AQS 中表示的查詢限制。

本主題的組織方式如下：

-   [使用 ISearchQueryHelper 開始使用](#getting-started-with-isearchqueryhelper)
-   [使用 GenerateSqlFromUserQuery 方法](#using-the-generatesqlfromuserquery-method)
-   [使用地區設定識別碼](#working-with-locale-identifiers)
-   [使用屬性和資料行](#working-with-properties-and-columns)
-   [使用查詢詞彙展開](#working-with-query-term-expansion)
-   [使用其他 ISearchQueryHelper 方法](#working-with-other-isearchqueryhelper-methods)
-   [相關主題](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>使用 ISearchQueryHelper 開始使用

您必須注意幾個主要介面和方法，才能使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面，以程式設計方式來查詢 Windows Search。 概括而言，您必須遵循下列步驟：

1.  將 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 實例具現化。
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  使用 [**ISearchManager：： GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)取得 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)的實例。 Windows Search 的系統目錄名稱為 `SYSTEMINDEX` 。
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  使用 [**ISearchCatalogManager：： GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)取得 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)的實例。
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  當您擁有 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)的實例之後，就可以取得用來連接到 Windows Search 索引 OLE DB 連接器的連接字串。
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>使用 GenerateSqlFromUserQuery 方法

[**ISearchQueryHelper：： GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery)方法會將使用者輸入轉換成 SQL 查詢字串，然後將其提交給 Windows Search 的 OLE DB 提供者。 這個方法會將 [先進的查詢語法](-search-3x-advancedquerysyntax.md) （ (AQS) 或自然查詢語法）轉譯為使用者在 SQL 中輸入的 (NQS) 查詢，並可讓您視需要新增其他 SQL 片段。

SQL 查詢字串會以下列格式傳回：


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



以下是從呼叫傳回的 SQL 字串範例 `GenerateSQLFromUserQuery("comput")` ：


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> 方法會產生 FREETEXT 和 CONTAINS 述詞，因為 CONTAINS 本身不會產生有意義的等級。

 

## <a name="working-with-locale-identifiers"></a>使用地區設定識別碼



| 方法                                                                                                                                                                                                                                   | 描述                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper：： get \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**ISearchQueryHelper：:p 的 \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | 取得/放置查詢 (LCID) 的語言代碼識別碼。 這有助於取得正確的斷詞工具和字幹分析器，以比較查詢詞彙與目錄/反向索引。 預設值為目前的輸入地區設定。 |
| [**ISearchQueryHelper：： get \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**ISearchQueryHelper：:p 的 \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | 取得/放置當剖析 Advanced Query 語法 (AQS) 關鍵字時，所使用之語言的 LCID。 預設值為預設使用者地區設定。                                                                              |



 

**內容地區** 設定和 **關鍵字地區** 設定是 (LCID) 的地區設定識別碼，可協助搜尋引擎藉由識別查詢詞彙的語言和 AQS 關鍵字的語言，來使用正確的斷詞工具。 這些不一定是相同的 Lcid，因為 Windows Search 是以許多國際版本提供，同時也包含適用于更多語言的多語系消費者介面 (MUI) 套件。 內容地區設定會識別使用者在中輸入其搜尋查詢之語言的 LCID，而關鍵字地區設定會識別搜尋引擎在剖析 Advanced Query 語法 (AQS) 關鍵字時所使用的 LCID。

例如，如果您的英文版沒有任何 MUI 套件，則內容地區設定和關鍵字地區設定都是1033。 如果您有不含 MUI 套件的德文版，則內容地區設定和關鍵字地區設定都是 1031 (gr-gr) 。 但是，如果您有英文版的羅馬尼亞 MUI 套件，則內容地區設定為 2072 (ro) ，而關鍵字地區設定是 1033 (en-us) 。

## <a name="working-with-properties-and-columns"></a>使用屬性和資料行



| 方法                                                                                                                                                                                                                                                  | 描述                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper：： get \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**ISearchQueryHelper：:p 的 \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | 取得/設定 CONTAINS 或 FREETEXT 子句) 中所列之搜尋 (屬性資料行的內容屬性。                                   |
| [**ISearchQueryHelper：： get \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**ISearchQueryHelper：:p 的 \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | 取得/設定在 SELECT 語句中) 要求 (或屬性的資料行。 預設值是 WHERE 子句中使用的 ItemUrl 和屬性。 |



 

專案會在屬性存放區中表示為數據列。 每個資料列都包含數個數據行，這些資料行代表該專案的屬性。 並非所有專案都具有指定屬性的值。 例如，音訊檔案通常不會包含 FromName 屬性的值，但可能會包含有關 System.object 的資訊。

使用這些方法，您可以使用以逗號分隔、以 null 終止的 Unicode 字串來存取或修改屬性，以指定屬性存放區的一或多個資料行名稱： "System.Doc>ument。作者，System.Doc>ument。標題」。

## <a name="working-with-query-term-expansion"></a>使用查詢詞彙展開



| 方法                                                                                                                                                                                                                                 | 描述                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**ISearchQueryHelper：： get \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**ISearchQueryHelper：:p 的 \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | 取得/設定搜尋字詞展開旗標。 |



 

此方法可讓您展開一些具有萬用字元的查詢詞彙，類似于正則運算式擴充。 前置詞展開會搜尋具有相同前置詞 (有趣/漏斗) 的單字。 如果未設定，則預設值為 [搜尋 \_ 詞彙 \_ 首碼] \_ 。 [**搜尋 \_ 詞彙 \_ 展開**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion)列舉支援的值如下所示：

-   搜尋 \_ 詞彙 \_ 首碼 \_ 全部-所有搜尋詞彙都已展開
-   搜尋 \_ 詞彙 \_ 無 \_ 擴充-沒有展開搜尋詞彙

## <a name="working-with-other-isearchqueryhelper-methods"></a>使用其他 ISearchQueryHelper 方法

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)介面中的許多方法都是用來設定查詢引數，或定義傳回的屬性。



| 方法                                                                                                                                                                                                                                                 | 描述                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper：： get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | 傳回 OLE DB 連接字串。 這是取得正確格式化和正確連接字串的慣用方法。                                  |
| [**ISearchQueryHelper：： get \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**ISearchQueryHelper：:p 的 \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | 取得/設定查詢傳回的結果數目上限， (也就是選取前 n 個) 。 預設值為-1，表示不會產生最大結果子句。 |
| [**ISearchQueryHelper：： get \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**ISearchQueryHelper：:p 的 \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | 取得/設定查詢結果集的排序次序， (ORDER BY) 。 如果沒有 ORDER BY 子句存在，則會以不具決定性的順序傳回結果。                   |
| [**ISearchQueryHelper：： get \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**ISearchQueryHelper：:p 的 \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | 取得/設定查詢的語法： Advanced Query 語法或自然查詢語法。                                                                                  |
| [**ISearchQueryHelper：： get \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**ISearchQueryHelper：:p 的 \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | 取得/設定透過 WHERE 子句附加的限制。                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[以程式設計方式查詢索引](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[使用 SQL 和 AQS 方法來查詢索引](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[使用搜尋-ms 通訊協定來查詢索引](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[使用 Windows Search SQL 語法來查詢索引](-search-sql-windowssearch-entry.md)
</dt> <dt>

[以程式設計方式使用 Advanced 查詢語法](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




