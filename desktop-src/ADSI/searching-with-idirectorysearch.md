---
title: 使用 >idirectorysearch 介面搜尋
description: '>idirectorysearch 介面提供高階且低額外負荷的介面來查詢目錄或通用類別目錄的資料。'
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch 介面 ADSI 搜尋
- 查詢 ADSI、查詢介面、>idirectorysearch
- ADSI ADSI，範例程式碼 C/c + +，使用 >idirectorysearch 搜尋目錄
- 使用搜尋目錄來 >idirectorysearch ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842743"
---
# <a name="searching-with-the-idirectorysearch-interface"></a><span data-ttu-id="62be4-107">使用 >idirectorysearch 介面搜尋</span><span class="sxs-lookup"><span data-stu-id="62be4-107">Searching with the IDirectorySearch Interface</span></span>

<span data-ttu-id="62be4-108">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面提供高階且低額外負荷的介面來查詢目錄或通用類別目錄的資料。</span><span class="sxs-lookup"><span data-stu-id="62be4-108">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides a high-level and low-overhead interface for querying data of a directory or a global catalog.</span></span> <span data-ttu-id="62be4-109">**>idirectorysearch** COM 介面只能與 vtable 搭配使用，因此不能用於以 Automation 為基礎的開發環境。</span><span class="sxs-lookup"><span data-stu-id="62be4-109">The **IDirectorySearch** COM interface can be used only with a vtable, and thus, is not available to Automation-based development environments.</span></span>

<span data-ttu-id="62be4-110">**執行搜尋**</span><span class="sxs-lookup"><span data-stu-id="62be4-110">**To perform a search**</span></span>

1.  <span data-ttu-id="62be4-111">系結至目錄中的物件。</span><span class="sxs-lookup"><span data-stu-id="62be4-111">Bind to an object in the directory.</span></span>
2.  <span data-ttu-id="62be4-112">呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 指標。</span><span class="sxs-lookup"><span data-stu-id="62be4-112">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span>
3.  <span data-ttu-id="62be4-113">使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 指標執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="62be4-113">Run the search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span> <span data-ttu-id="62be4-114">呼叫 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 方法，並傳遞搜尋篩選、要求的屬性名稱及其他參數。</span><span class="sxs-lookup"><span data-stu-id="62be4-114">Call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method, and pass a search filter, the requested attribute names, and other parameters.</span></span>

<span data-ttu-id="62be4-115">如需搜尋篩選語法的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="62be4-115">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="62be4-116">查詢執行是提供者特定的。</span><span class="sxs-lookup"><span data-stu-id="62be4-116">Query execution is provider-specific.</span></span> <span data-ttu-id="62be4-117">有些提供者在呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) 或 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 之前，不會執行實際的查詢。</span><span class="sxs-lookup"><span data-stu-id="62be4-117">With some providers, the actual query execution does not occur until [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) is called.</span></span> <span data-ttu-id="62be4-118">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可直接搭配搜尋篩選使用。</span><span class="sxs-lookup"><span data-stu-id="62be4-118">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface works with search filters directly.</span></span> <span data-ttu-id="62be4-119">SQL 方言或 LDAP 方言都不需要。</span><span class="sxs-lookup"><span data-stu-id="62be4-119">Neither the SQL dialect nor the LDAP dialect are required.</span></span>

<span data-ttu-id="62be4-120">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面會提供方法來列舉結果集（依資料列）。</span><span class="sxs-lookup"><span data-stu-id="62be4-120">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides methods to enumerate the result set, row by row.</span></span> <span data-ttu-id="62be4-121">[**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)方法會抓取第一個資料列，而 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)會將您移至目前資料列中的下一個資料列。</span><span class="sxs-lookup"><span data-stu-id="62be4-121">The [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) method retrieves the first row and [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) moves you to the next row from the current row.</span></span> <span data-ttu-id="62be4-122">當您到達最後一個資料列時，呼叫這些方法會傳回 \_ \_ NOMORE 資料 \_ 列錯誤碼的廣告。</span><span class="sxs-lookup"><span data-stu-id="62be4-122">When you have reached the last row, calling these methods returns the S\_ADS\_NOMORE\_ROWS error code.</span></span> <span data-ttu-id="62be4-123">相反地， [**>idirectorysearch：： GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) 會一次將您移回一個資料列。</span><span class="sxs-lookup"><span data-stu-id="62be4-123">Conversely, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) moves you back one row at a time.</span></span> <span data-ttu-id="62be4-124">S \_ ADS \_ NOMORE ROWS 傳回 \_ 值指出您已達到結果集的第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="62be4-124">An S\_ADS\_NOMORE\_ROWS return value indicates that you have reached the first row of the result set.</span></span> <span data-ttu-id="62be4-125">這些方法會在用戶端上的結果集（常駐于記憶體中）上運作。</span><span class="sxs-lookup"><span data-stu-id="62be4-125">These methods operate on the result set, resident in memory, on the client.</span></span> <span data-ttu-id="62be4-126">因此，當您執行分頁和非同步搜尋並關閉快取 \_ \_ 結果選項時，回溯滾動可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="62be4-126">Thus, when paged and asynchronous searches are performed and the \_CACHE\_RESULTS option is turned off, backward scrolling can have unexpected consequences.</span></span>

<span data-ttu-id="62be4-127">當您找到適當的資料列時，請呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 來取得資料項目、依資料行的資料行。</span><span class="sxs-lookup"><span data-stu-id="62be4-127">When you have located the appropriate row, call [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) to obtain data items, column by column.</span></span> <span data-ttu-id="62be4-128">每次呼叫時，您都會傳遞感興趣之資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="62be4-128">For each call, you pass the name of the column of interest.</span></span> <span data-ttu-id="62be4-129">傳回的資料項目是 [**廣告 \_ 搜尋資料 \_ 行**](/windows/desktop/api/Iads/ns-iads-ads_search_column) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="62be4-129">The data item returned is a pointer to an [**ADS\_SEARCH\_COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) structure.</span></span> <span data-ttu-id="62be4-130">**GetColumn** 會為您配置此結構，但您必須使用 [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn)來釋放它。</span><span class="sxs-lookup"><span data-stu-id="62be4-130">**GetColumn** allocates this structure for you, but you must free it using [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span></span> <span data-ttu-id="62be4-131">呼叫 [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) 以完成搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="62be4-131">Call [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) to complete the search operation.</span></span>

<span data-ttu-id="62be4-132">**執行目錄搜尋**</span><span class="sxs-lookup"><span data-stu-id="62be4-132">**To perform a directory search**</span></span>

1.  <span data-ttu-id="62be4-133">系結至 LDAP 提供者。</span><span class="sxs-lookup"><span data-stu-id="62be4-133">Bind to an LDAP provider.</span></span> <span data-ttu-id="62be4-134">它可能是網域控制站或通用類別目錄提供者。</span><span class="sxs-lookup"><span data-stu-id="62be4-134">It may be a domain controller or a global catalog provider.</span></span>
2.  <span data-ttu-id="62be4-135">使用 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))呼叫來取出 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM 介面;這項作業在初始系結期間可能已在步驟1中完成。</span><span class="sxs-lookup"><span data-stu-id="62be4-135">Retrieve the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM Interface with a call to [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); this operation may have been done in Step 1 during the initial binding.</span></span>

    <span data-ttu-id="62be4-136">（選擇性）呼叫 [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 來選取用來處理搜尋結果的選項。</span><span class="sxs-lookup"><span data-stu-id="62be4-136">Optionally, call [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) to select options for handling the results of your search.</span></span>

3.  <span data-ttu-id="62be4-137">呼叫 [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)。</span><span class="sxs-lookup"><span data-stu-id="62be4-137">Call [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span></span> <span data-ttu-id="62be4-138">根據 [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 中設定的選項而定，這可能會開始執行查詢。</span><span class="sxs-lookup"><span data-stu-id="62be4-138">Depending on the options set in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) this may, or may not, begin query execution.</span></span>
4.  <span data-ttu-id="62be4-139">呼叫 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ，將資料列索引 (內部移至 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) 至第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="62be4-139">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to move the row index (internal to [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) to the first row.</span></span>
5.  <span data-ttu-id="62be4-140">使用 [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)讀取資料列中的資料，然後呼叫 [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) 釋放 **GetColumn** 所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="62be4-140">Read the data from the row using [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), then call [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) to release the memory allocated by **GetColumn**.</span></span>
6.  <span data-ttu-id="62be4-141">重複步驟5，直到從搜尋結果取出所有資料，或直到 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 傳回 S \_ ADS NOMORE 資料列為止 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="62be4-141">Repeat Step 5 until all data is retrieved from the search result, or until [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) returns S\_ADS\_NOMORE\_ROWS.</span></span>
7.  <span data-ttu-id="62be4-142">完成時呼叫 [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) 和 [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) 。</span><span class="sxs-lookup"><span data-stu-id="62be4-142">Call [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) and [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) when complete.</span></span>

<span data-ttu-id="62be4-143">下列程式碼範例顯示此案例。</span><span class="sxs-lookup"><span data-stu-id="62be4-143">The following code example shows this scenario.</span></span> <span data-ttu-id="62be4-144">若要開始系結至 ADSI，請呼叫 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數。</span><span class="sxs-lookup"><span data-stu-id="62be4-144">To start binding to ADSI, call the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



<span data-ttu-id="62be4-145">這會提供 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="62be4-145">This provides a pointer to the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="62be4-146">現在有一個 IDirectoryInterface 實例的 COM 介面，請呼叫 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)。</span><span class="sxs-lookup"><span data-stu-id="62be4-146">Now that there is a COM interface for an IDirectoryInterface instance, call [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span></span>

<span data-ttu-id="62be4-147">建立屬性名稱的陣列，以準備呼叫 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 函數。</span><span class="sxs-lookup"><span data-stu-id="62be4-147">Build an array of attribute names to prepare to call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="62be4-148">屬性名稱是在 Active Directory 的架構內定義。</span><span class="sxs-lookup"><span data-stu-id="62be4-148">The attribute names are defined within the schema of Active Directory.</span></span> <span data-ttu-id="62be4-149">如需架構定義的詳細資訊，請參閱 [ADSI 架構模型](adsi-schema-model.md)。</span><span class="sxs-lookup"><span data-stu-id="62be4-149">For more information about the schema definition, see [ADSI Schema Model](adsi-schema-model.md).</span></span> <span data-ttu-id="62be4-150">如果物件支援，則會傳回所列出的屬性名稱，做為搜尋的結果集。</span><span class="sxs-lookup"><span data-stu-id="62be4-150">The attribute names listed are returned, if supported by the object, as the result set of the search.</span></span>


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



<span data-ttu-id="62be4-151">現在，呼叫 [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 函數。</span><span class="sxs-lookup"><span data-stu-id="62be4-151">Now, call the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="62be4-152">除非您呼叫 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 方法，否則搜尋不會執行。</span><span class="sxs-lookup"><span data-stu-id="62be4-152">The search does not run until you call the [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) method.</span></span>


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



<span data-ttu-id="62be4-153">呼叫 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 以反覆運算結果中的資料列。</span><span class="sxs-lookup"><span data-stu-id="62be4-153">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to iterate rows in the result.</span></span> <span data-ttu-id="62be4-154">然後，會查詢每個資料列中的 "description" 屬性。</span><span class="sxs-lookup"><span data-stu-id="62be4-154">Each row is then queried for the "description" attribute.</span></span> <span data-ttu-id="62be4-155">如果找到此屬性，則會顯示該屬性。</span><span class="sxs-lookup"><span data-stu-id="62be4-155">If the attribute is found, it is displayed.</span></span>


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



<span data-ttu-id="62be4-156">若要結束搜尋，請呼叫 [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) 方法。</span><span class="sxs-lookup"><span data-stu-id="62be4-156">To end the search, call the [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) method.</span></span>

<span data-ttu-id="62be4-157">請注意，如果未設定頁面大小， [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 會封鎖，直到整個結果集傳回至用戶端為止。</span><span class="sxs-lookup"><span data-stu-id="62be4-157">Be aware that if a page size is not set, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blocks until the entire result set is returned to the client.</span></span> <span data-ttu-id="62be4-158">如果已設定頁面大小，則會 **GetNextRow** 封鎖，直到第一個頁面 (頁面大小 = 頁面中的資料列數目) 。</span><span class="sxs-lookup"><span data-stu-id="62be4-158">If page size is set, then **GetNextRow** blocks until the first page (page size = number of rows in a page) is returned.</span></span> <span data-ttu-id="62be4-159">如果已設定頁面大小，而且查詢要排序，且您未搜尋至少一個索引屬性，則會忽略 [頁面大小] 值，而且伺服器會在傳回資料之前計算整個結果集。</span><span class="sxs-lookup"><span data-stu-id="62be4-159">If page size is set and the query is to be sorted and you are not searching on at least one indexed attribute, then the page size value is ignored, and the server calculates the entire result set prior to returning the data.</span></span> <span data-ttu-id="62be4-160">這會造成 **GetNextRow** 封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="62be4-160">This has the effect of **GetNextRow** blocking until the query completes.</span></span>

> [!Note]  
> <span data-ttu-id="62be4-161">若要將此查詢從目錄搜尋變更為通用類別目錄搜尋， [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 呼叫會變更。</span><span class="sxs-lookup"><span data-stu-id="62be4-161">To change this query from a directory search to a global catalog search, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) call is changed.</span></span>

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 