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
# <a name="querying-the-index-with-isearchqueryhelper"></a><span data-ttu-id="7a5d4-104">使用 ISearchQueryHelper 查詢索引</span><span class="sxs-lookup"><span data-stu-id="7a5d4-104">Querying the Index with ISearchQueryHelper</span></span>

<span data-ttu-id="7a5d4-105">您可以使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面來查詢索引。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-105">You can use the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface to query the index.</span></span> <span data-ttu-id="7a5d4-106">這個介面會實作為 helper 類別，以 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (和 [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) ，而且是藉由呼叫 [**ISearchCatalogManager：： GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)取得。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-106">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (and [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span> <span data-ttu-id="7a5d4-107">此介面允許您：</span><span class="sxs-lookup"><span data-stu-id="7a5d4-107">This interface permits you to:</span></span>

-   <span data-ttu-id="7a5d4-108">取得連接到 Windows Search 資料庫 OLE DB 連接字串。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-108">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
-   <span data-ttu-id="7a5d4-109">將 Advanced Query 語法 (AQS) 使用者查詢轉換成 Windows Search 結構化查詢語言 (SQL)  (SQL) 。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-109">Convert Advanced Query Syntax (AQS) user queries to Windows Search Structured Query Language (SQL).</span></span>
-   <span data-ttu-id="7a5d4-110">指定可在 SQL 中表示但無法在 AQS 中表示的查詢限制。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-110">Specify query restrictions that can be expressed in SQL, but not in AQS.</span></span>

<span data-ttu-id="7a5d4-111">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="7a5d4-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7a5d4-112">使用 ISearchQueryHelper 開始使用</span><span class="sxs-lookup"><span data-stu-id="7a5d4-112">Getting Started with ISearchQueryHelper</span></span>](#getting-started-with-isearchqueryhelper)
-   [<span data-ttu-id="7a5d4-113">使用 GenerateSqlFromUserQuery 方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-113">Using the GenerateSqlFromUserQuery Method</span></span>](#using-the-generatesqlfromuserquery-method)
-   [<span data-ttu-id="7a5d4-114">使用地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="7a5d4-114">Working with Locale Identifiers</span></span>](#working-with-locale-identifiers)
-   [<span data-ttu-id="7a5d4-115">使用屬性和資料行</span><span class="sxs-lookup"><span data-stu-id="7a5d4-115">Working with Properties and Columns</span></span>](#working-with-properties-and-columns)
-   [<span data-ttu-id="7a5d4-116">使用查詢詞彙展開</span><span class="sxs-lookup"><span data-stu-id="7a5d4-116">Working with Query Term Expansion</span></span>](#working-with-query-term-expansion)
-   [<span data-ttu-id="7a5d4-117">使用其他 ISearchQueryHelper 方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-117">Working with Other ISearchQueryHelper Methods</span></span>](#working-with-other-isearchqueryhelper-methods)
-   [<span data-ttu-id="7a5d4-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a5d4-118">Related topics</span></span>](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a><span data-ttu-id="7a5d4-119">使用 ISearchQueryHelper 開始使用</span><span class="sxs-lookup"><span data-stu-id="7a5d4-119">Getting Started with ISearchQueryHelper</span></span>

<span data-ttu-id="7a5d4-120">您必須注意幾個主要介面和方法，才能使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面，以程式設計方式來查詢 Windows Search。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-120">There are a few key interfaces and methods you should be aware of before you can start programmatically querying Windows Search using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface.</span></span> <span data-ttu-id="7a5d4-121">概括而言，您必須遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="7a5d4-121">At a high level, you need to follow these steps:</span></span>

1.  <span data-ttu-id="7a5d4-122">將 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 實例具現化。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-122">Instantiate an [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) instance.</span></span>
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  <span data-ttu-id="7a5d4-123">使用 [**ISearchManager：： GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)取得 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)的實例。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-123">Obtain an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) using [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span></span> <span data-ttu-id="7a5d4-124">Windows Search 的系統目錄名稱為 `SYSTEMINDEX` 。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-124">The name of the system catalog for Windows Search is `SYSTEMINDEX`.</span></span>
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  <span data-ttu-id="7a5d4-125">使用 [**ISearchCatalogManager：： GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)取得 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)的實例。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-125">Obtain an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) using [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span>
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  <span data-ttu-id="7a5d4-126">當您擁有 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)的實例之後，就可以取得用來連接到 Windows Search 索引 OLE DB 連接器的連接字串。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-126">After you have an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), you can then get the connection string used to connect to the Windows Search index OLE DB connector.</span></span>
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a><span data-ttu-id="7a5d4-127">使用 GenerateSqlFromUserQuery 方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-127">Using the GenerateSqlFromUserQuery Method</span></span>

<span data-ttu-id="7a5d4-128">[**ISearchQueryHelper：： GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery)方法會將使用者輸入轉換成 SQL 查詢字串，然後將其提交給 Windows Search 的 OLE DB 提供者。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-128">The [**ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) method transforms user input into a SQL query string, which can then be submitted to the OLE DB provider for Windows Search.</span></span> <span data-ttu-id="7a5d4-129">這個方法會將 [先進的查詢語法](-search-3x-advancedquerysyntax.md) （ (AQS) 或自然查詢語法）轉譯為使用者在 SQL 中輸入的 (NQS) 查詢，並可讓您視需要新增其他 SQL 片段。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-129">This method translates the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) or Natural Query Syntax (NQS) query entered by the user into SQL, and lets you add other SQL fragments as needed.</span></span>

<span data-ttu-id="7a5d4-130">SQL 查詢字串會以下列格式傳回：</span><span class="sxs-lookup"><span data-stu-id="7a5d4-130">The SQL query string is returned in the following form:</span></span>


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



<span data-ttu-id="7a5d4-131">以下是從呼叫傳回的 SQL 字串範例 `GenerateSQLFromUserQuery("comput")` ：</span><span class="sxs-lookup"><span data-stu-id="7a5d4-131">The following is an example of the SQL string returned from the call `GenerateSQLFromUserQuery("comput")`:</span></span>


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> <span data-ttu-id="7a5d4-132">方法會產生 FREETEXT 和 CONTAINS 述詞，因為 CONTAINS 本身不會產生有意義的等級。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-132">The method generates both the FREETEXT and the CONTAINS predicates because CONTAINS alone does not generate meaningful ranking.</span></span>

 

## <a name="working-with-locale-identifiers"></a><span data-ttu-id="7a5d4-133">使用地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="7a5d4-133">Working with Locale Identifiers</span></span>



| <span data-ttu-id="7a5d4-134">方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-134">Method</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="7a5d4-135">描述</span><span class="sxs-lookup"><span data-stu-id="7a5d4-135">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5d4-136">[**ISearchQueryHelper：： get \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span><span class="sxs-lookup"><span data-stu-id="7a5d4-136">[**ISearchQueryHelper::get\_QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span></span><br/> [<span data-ttu-id="7a5d4-137">**ISearchQueryHelper：:p 的 \_ QueryContentLocale**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-137">**ISearchQueryHelper::put\_QueryContentLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | <span data-ttu-id="7a5d4-138">取得/放置查詢 (LCID) 的語言代碼識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-138">Gets/Puts the language code identifier (LCID) of the query.</span></span> <span data-ttu-id="7a5d4-139">這有助於取得正確的斷詞工具和字幹分析器，以比較查詢詞彙與目錄/反向索引。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-139">This helps get the correct wordbreaker and stemmer to compare query terms against the catalog/inverted index.</span></span> <span data-ttu-id="7a5d4-140">預設值為目前的輸入地區設定。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-140">The default is the current input locale.</span></span> |
| <span data-ttu-id="7a5d4-141">[**ISearchQueryHelper：： get \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span><span class="sxs-lookup"><span data-stu-id="7a5d4-141">[**ISearchQueryHelper::get\_QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span></span><br/> [<span data-ttu-id="7a5d4-142">**ISearchQueryHelper：:p 的 \_ QueryKeywordLocale**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-142">**ISearchQueryHelper::put\_QueryKeywordLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | <span data-ttu-id="7a5d4-143">取得/放置當剖析 Advanced Query 語法 (AQS) 關鍵字時，所使用之語言的 LCID。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-143">Gets/Puts the LCID for the language to use when parsing Advanced Query Syntax (AQS) keywords.</span></span> <span data-ttu-id="7a5d4-144">預設值為預設使用者地區設定。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-144">The default is the default user locale.</span></span>                                                                              |



 

<span data-ttu-id="7a5d4-145">**內容地區** 設定和 **關鍵字地區** 設定是 (LCID) 的地區設定識別碼，可協助搜尋引擎藉由識別查詢詞彙的語言和 AQS 關鍵字的語言，來使用正確的斷詞工具。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-145">The **content locale** and **keyword locale** are locale identifiers (LCID) that help the search engine use the correct word breakers by identifying the language of the query terms and the language the AQS keywords.</span></span> <span data-ttu-id="7a5d4-146">這些不一定是相同的 Lcid，因為 Windows Search 是以許多國際版本提供，同時也包含適用于更多語言的多語系消費者介面 (MUI) 套件。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-146">These are not always the same LCIDs because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="7a5d4-147">內容地區設定會識別使用者在中輸入其搜尋查詢之語言的 LCID，而關鍵字地區設定會識別搜尋引擎在剖析 Advanced Query 語法 (AQS) 關鍵字時所使用的 LCID。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-147">The content locale identifies the LCID for the language users input their search query in, while the keyword locale identifies the LCID the search engine uses when parsing Advanced Query Syntax (AQS) keywords.</span></span>

<span data-ttu-id="7a5d4-148">例如，如果您的英文版沒有任何 MUI 套件，則內容地區設定和關鍵字地區設定都是1033。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-148">For example, if you have the English-US version with no MUI packs, both the content locale and keyword locale are 1033.</span></span> <span data-ttu-id="7a5d4-149">如果您有不含 MUI 套件的德文版，則內容地區設定和關鍵字地區設定都是 1031 (gr-gr) 。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-149">If you have the German version with no MUI packs, then both the content locale and keyword locale are 1031 (gr-gr).</span></span> <span data-ttu-id="7a5d4-150">但是，如果您有英文版的羅馬尼亞 MUI 套件，則內容地區設定為 2072 (ro) ，而關鍵字地區設定是 1033 (en-us) 。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-150">However, if you have the English version with the Romanian MUI pack, the content locale is 2072 (ro) and the keyword locale is 1033 (en-us).</span></span>

## <a name="working-with-properties-and-columns"></a><span data-ttu-id="7a5d4-151">使用屬性和資料行</span><span class="sxs-lookup"><span data-stu-id="7a5d4-151">Working with Properties and Columns</span></span>



| <span data-ttu-id="7a5d4-152">方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-152">Methods</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="7a5d4-153">描述</span><span class="sxs-lookup"><span data-stu-id="7a5d4-153">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5d4-154">[**ISearchQueryHelper：： get \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span><span class="sxs-lookup"><span data-stu-id="7a5d4-154">[**ISearchQueryHelper::get\_QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span></span><br/> [<span data-ttu-id="7a5d4-155">**ISearchQueryHelper：:p 的 \_ QueryContentProperties**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-155">**ISearchQueryHelper::put\_QueryContentProperties**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | <span data-ttu-id="7a5d4-156">取得/設定 CONTAINS 或 FREETEXT 子句) 中所列之搜尋 (屬性資料行的內容屬性。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-156">Gets/Sets the content properties for the search (property column listed in the CONTAINS or FREETEXT clauses).</span></span>                                   |
| <span data-ttu-id="7a5d4-157">[**ISearchQueryHelper：： get \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span><span class="sxs-lookup"><span data-stu-id="7a5d4-157">[**ISearchQueryHelper::get\_QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span></span><br/> [<span data-ttu-id="7a5d4-158">**ISearchQueryHelper：:p 的 \_ QuerySelectColumns**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-158">**ISearchQueryHelper::put\_QuerySelectColumns**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | <span data-ttu-id="7a5d4-159">取得/設定在 SELECT 語句中) 要求 (或屬性的資料行。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-159">Gets/Sets the columns (or properties) requested in the SELECT statement.</span></span> <span data-ttu-id="7a5d4-160">預設值是 WHERE 子句中使用的 ItemUrl 和屬性。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-160">The default is System.ItemUrl and properties used in the WHERE clause.</span></span> |



 

<span data-ttu-id="7a5d4-161">專案會在屬性存放區中表示為數據列。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-161">Items are represented in the property store as a row.</span></span> <span data-ttu-id="7a5d4-162">每個資料列都包含數個數據行，這些資料行代表該專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-162">Each row contains a number of columns that represent properties for that item.</span></span> <span data-ttu-id="7a5d4-163">並非所有專案都具有指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-163">Not all items will have a value for a given property.</span></span> <span data-ttu-id="7a5d4-164">例如，音訊檔案通常不會包含 FromName 屬性的值，但可能會包含有關 System.object 的資訊。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-164">For example, an audio file would typically not contain a value for the System.Property.FromName property but may contain information regarding the System.Music.Artist.</span></span>

<span data-ttu-id="7a5d4-165">使用這些方法，您可以使用以逗號分隔、以 null 終止的 Unicode 字串來存取或修改屬性，以指定屬性存放區的一或多個資料行名稱： "System.Doc>ument。作者，System.Doc>ument。標題」。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-165">With these methods, you access or modify the property with a comma delimited, null-terminated, Unicode string that specifies one or more column names of the property store: "System.Document.Author, System.Document.Title".</span></span>

## <a name="working-with-query-term-expansion"></a><span data-ttu-id="7a5d4-166">使用查詢詞彙展開</span><span class="sxs-lookup"><span data-stu-id="7a5d4-166">Working with Query Term Expansion</span></span>



| <span data-ttu-id="7a5d4-167">方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-167">Methods</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="7a5d4-168">描述</span><span class="sxs-lookup"><span data-stu-id="7a5d4-168">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="7a5d4-169">**ISearchQueryHelper：： get \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-169">**ISearchQueryHelper::get\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [<span data-ttu-id="7a5d4-170">**ISearchQueryHelper：:p 的 \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-170">**ISearchQueryHelper::put\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | <span data-ttu-id="7a5d4-171">取得/設定搜尋字詞展開旗標。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-171">Gets/Sets the search term expansion flag.</span></span> |



 

<span data-ttu-id="7a5d4-172">此方法可讓您展開一些具有萬用字元的查詢詞彙，類似于正則運算式擴充。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-172">This method enables the expansion of some query terms with wild card characters, similar to regular expression expansion.</span></span> <span data-ttu-id="7a5d4-173">前置詞展開會搜尋具有相同前置詞 (有趣/漏斗) 的單字。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-173">Prefix expansion searches for words with the same prefix (fun/funnel).</span></span> <span data-ttu-id="7a5d4-174">如果未設定，則預設值為 [搜尋 \_ 詞彙 \_ 首碼] \_ 。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-174">If not set, the default value is SEARCH\_TERM\_PREFIX\_ALL.</span></span> <span data-ttu-id="7a5d4-175">[**搜尋 \_ 詞彙 \_ 展開**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion)列舉支援的值如下所示：</span><span class="sxs-lookup"><span data-stu-id="7a5d4-175">The supported values of the [**SEARCH\_TERM\_EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) enumeration are as follows:</span></span>

-   <span data-ttu-id="7a5d4-176">搜尋 \_ 詞彙 \_ 首碼 \_ 全部-所有搜尋詞彙都已展開</span><span class="sxs-lookup"><span data-stu-id="7a5d4-176">SEARCH\_TERM\_PREFIX\_ALL - All search terms are expanded</span></span>
-   <span data-ttu-id="7a5d4-177">搜尋 \_ 詞彙 \_ 無 \_ 擴充-沒有展開搜尋詞彙</span><span class="sxs-lookup"><span data-stu-id="7a5d4-177">SEARCH\_TERM\_NO\_EXPANSION - No search terms are expanded</span></span>

## <a name="working-with-other-isearchqueryhelper-methods"></a><span data-ttu-id="7a5d4-178">使用其他 ISearchQueryHelper 方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-178">Working with Other ISearchQueryHelper Methods</span></span>

<span data-ttu-id="7a5d4-179">[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)介面中的許多方法都是用來設定查詢引數，或定義傳回的屬性。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-179">Many of the methods in the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface are used to set query arguments or define the properties returned.</span></span>



| <span data-ttu-id="7a5d4-180">方法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-180">Methods</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="7a5d4-181">描述</span><span class="sxs-lookup"><span data-stu-id="7a5d4-181">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a5d4-182">**ISearchQueryHelper：： get \_ ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-182">**ISearchQueryHelper::get\_ConnectionString**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | <span data-ttu-id="7a5d4-183">傳回 OLE DB 連接字串。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-183">Returns the OLE DB connection string.</span></span> <span data-ttu-id="7a5d4-184">這是取得正確格式化和正確連接字串的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-184">This is the preferred method of getting a properly formatted and correct connection string.</span></span>                                  |
| [<span data-ttu-id="7a5d4-185">**ISearchQueryHelper：： get \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-185">**ISearchQueryHelper::get\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [<span data-ttu-id="7a5d4-186">**ISearchQueryHelper：:p 的 \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-186">**ISearchQueryHelper::put\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | <span data-ttu-id="7a5d4-187">取得/設定查詢傳回的結果數目上限， (也就是選取前 n 個) 。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-187">Gets/Sets the maximum number of results to be returned by a query (that is, SELECT TOP n).</span></span> <span data-ttu-id="7a5d4-188">預設值為-1，表示不會產生最大結果子句。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-188">The default is -1, meaning that no maximum results clause is generated.</span></span> |
| [<span data-ttu-id="7a5d4-189">**ISearchQueryHelper：： get \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-189">**ISearchQueryHelper::get\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [<span data-ttu-id="7a5d4-190">**ISearchQueryHelper：:p 的 \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-190">**ISearchQueryHelper::put\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | <span data-ttu-id="7a5d4-191">取得/設定查詢結果集的排序次序， (ORDER BY) 。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-191">Gets/Sets the sort order for the query result set (ORDER BY).</span></span> <span data-ttu-id="7a5d4-192">如果沒有 ORDER BY 子句存在，則會以不具決定性的順序傳回結果。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-192">If no ORDER BY clause exists, the results are returned in non-deterministic order.</span></span>                   |
| [<span data-ttu-id="7a5d4-193">**ISearchQueryHelper：： get \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-193">**ISearchQueryHelper::get\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [<span data-ttu-id="7a5d4-194">**ISearchQueryHelper：:p 的 \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-194">**ISearchQueryHelper::put\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | <span data-ttu-id="7a5d4-195">取得/設定查詢的語法： Advanced Query 語法或自然查詢語法。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-195">Gets/Sets the syntax of the query: Advanced Query Syntax or Natural Query Syntax.</span></span>                                                                                  |
| [<span data-ttu-id="7a5d4-196">**ISearchQueryHelper：： get \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-196">**ISearchQueryHelper::get\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [<span data-ttu-id="7a5d4-197">**ISearchQueryHelper：:p 的 \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="7a5d4-197">**ISearchQueryHelper::put\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | <span data-ttu-id="7a5d4-198">取得/設定透過 WHERE 子句附加的限制。</span><span class="sxs-lookup"><span data-stu-id="7a5d4-198">Gets/Sets the restrictions appended via WHERE clauses.</span></span>                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="7a5d4-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a5d4-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a5d4-200">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="7a5d4-200">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="7a5d4-201">使用 SQL 和 AQS 方法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="7a5d4-201">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="7a5d4-202">使用搜尋-ms 通訊協定來查詢索引</span><span class="sxs-lookup"><span data-stu-id="7a5d4-202">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="7a5d4-203">使用 Windows Search SQL 語法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="7a5d4-203">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="7a5d4-204">以程式設計方式使用 Advanced 查詢語法</span><span class="sxs-lookup"><span data-stu-id="7a5d4-204">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




