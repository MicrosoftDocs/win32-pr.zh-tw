---
title: 正在抓取刪除的物件
description: 刪除的物件會儲存在刪除的物件容器中。
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- 正在抓取刪除的物件 AD
- 物件廣告，正在抓取刪除的物件
- Active Directory，使用來抓取已刪除的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b2062c747e38bc0b3a9b1b793a102006c11512
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462833"
---
# <a name="retrieving-deleted-objects"></a><span data-ttu-id="86b44-106">正在抓取刪除的物件</span><span class="sxs-lookup"><span data-stu-id="86b44-106">Retrieving Deleted Objects</span></span>

<span data-ttu-id="86b44-107">刪除的物件會儲存在刪除的物件容器中。</span><span class="sxs-lookup"><span data-stu-id="86b44-107">Deleted objects are stored in the Deleted Objects container.</span></span> <span data-ttu-id="86b44-108">「刪除的物件」容器通常不可見，但是「刪除的物件」容器可由「系統管理員」群組的成員來系結。</span><span class="sxs-lookup"><span data-stu-id="86b44-108">The Deleted Objects container is not normally visible, but the Deleted Objects container can be bound to by a member of the administrators group.</span></span> <span data-ttu-id="86b44-109">您可以列舉已刪除物件容器的內容，而且可以使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 介面與 **ADS \_ SEARCHPREF \_** 標記搜尋喜好設定，來取得個別已刪除的物件屬性。</span><span class="sxs-lookup"><span data-stu-id="86b44-109">The contents of the Deleted Objects container can be enumerated and individual deleted object attributes can be obtained using the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface with the **ADS\_SEARCHPREF\_TOMBSTONE** search preference.</span></span>

<span data-ttu-id="86b44-110">您可以藉由系結至 Ntdsapi 中定義的已知 GUID **guid \_ Deleted \_ Objects \_ 容器** 來取得已刪除的物件容器。</span><span class="sxs-lookup"><span data-stu-id="86b44-110">The Deleted Objects container can be obtained by binding to the well-known GUID **GUID\_DELETED\_OBJECTS\_CONTAINER** defined in Ntdsapi.h.</span></span> <span data-ttu-id="86b44-111">如需有關系結至已知 Guid 的詳細資訊，請參閱 [使用 WKGUID 系結至 Well-Known 物件](binding-to-well-known-objects-using-wkguid.md)。</span><span class="sxs-lookup"><span data-stu-id="86b44-111">For more information about binding to well-known GUIDs, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>

<span data-ttu-id="86b44-112">系結至已刪除的物件容器時，指定 **ADS \_ FAST \_ BIND** 選項。</span><span class="sxs-lookup"><span data-stu-id="86b44-112">Specify the **ADS\_FAST\_BIND** option when binding to the Deleted Objects container.</span></span> <span data-ttu-id="86b44-113">這表示，用來處理 Active Directory Domain Services 中的物件（例如 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADSPROPERTYLIST**](/windows/desktop/api/iads/nn-iads-iadspropertylist)）的 ADSI 介面，不能用於已刪除的物件容器。</span><span class="sxs-lookup"><span data-stu-id="86b44-113">This means that the ADSI interfaces used to work with an object in Active Directory Domain Services, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on the Deleted Objects container.</span></span> <span data-ttu-id="86b44-114">如需詳細資訊和示範如何系結至 Deleted Objects 容器的程式碼範例，請參閱下面的 GetDeletedObjectsContainer 範例函式。</span><span class="sxs-lookup"><span data-stu-id="86b44-114">For more information and a code example that shows how to bind to the Deleted Objects container, see the GetDeletedObjectsContainer example function below.</span></span>

-   [<span data-ttu-id="86b44-115">列舉已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="86b44-115">Enumerating Deleted Objects</span></span>](#enumerating-deleted-objects)
-   [<span data-ttu-id="86b44-116">尋找特定已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="86b44-116">Finding a Specific Deleted Object</span></span>](#finding-a-specific-deleted-object)
    -   [<span data-ttu-id="86b44-117">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="86b44-117">GetDeletedObjectsContainer</span></span>](#getdeletedobjectscontainer)
    -   [<span data-ttu-id="86b44-118">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="86b44-118">EnumDeletedObjects</span></span>](#enumdeletedobjects)
    -   [<span data-ttu-id="86b44-119">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="86b44-119">FindDeletedObjectByGUID</span></span>](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a><span data-ttu-id="86b44-120">列舉已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="86b44-120">Enumerating Deleted Objects</span></span>

<span data-ttu-id="86b44-121">[**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)介面是用來搜尋已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-121">The [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface is used to search for deleted objects.</span></span>

<span data-ttu-id="86b44-122">**列舉已刪除的物件**</span><span class="sxs-lookup"><span data-stu-id="86b44-122">**To enumerate deleted objects**</span></span>

1.  <span data-ttu-id="86b44-123">取得已刪除物件容器的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 介面。</span><span class="sxs-lookup"><span data-stu-id="86b44-123">Obtain the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface for the Deleted Objects container.</span></span> <span data-ttu-id="86b44-124">這是藉由系結至已刪除的物件容器來完成，並要求 **>idirectorysearch** 介面。</span><span class="sxs-lookup"><span data-stu-id="86b44-124">This is accomplished by binding to the Deleted Objects container and requesting the **IDirectorySearch** interface.</span></span> <span data-ttu-id="86b44-125">如需詳細資訊和示範如何系結至 Deleted Objects 容器的程式碼範例，請參閱下列 **GetDeletedObjectsContainer** 函數範例。</span><span class="sxs-lookup"><span data-stu-id="86b44-125">For more information and a code example that shows how to bind to the Deleted Objects container, see the following **GetDeletedObjectsContainer** function example.</span></span>
2.  <span data-ttu-id="86b44-126">使用 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference)方法，將 **ads \_ SEARCHPREF \_ 搜尋 \_ 範圍** 搜尋喜好設定設為 **ads \_ 範圍 \_ ONELEVEL** 。</span><span class="sxs-lookup"><span data-stu-id="86b44-126">Set the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** search preference to **ADS\_SCOPE\_ONELEVEL** using the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="86b44-127">您也可以使用 **ads \_ 範圍 \_ 子樹** 喜好設定，但刪除的物件容器只是一個層級，因此使用 **ADS \_ 範圍 \_ 子樹** 是多餘的。</span><span class="sxs-lookup"><span data-stu-id="86b44-127">The **ADS\_SCOPE\_SUBTREE** preference can also be used, but the Deleted Objects container is only one level, so using **ADS\_SCOPE\_SUBTREE** is redundant.</span></span>
3.  <span data-ttu-id="86b44-128">將 **ADS \_ SEARCHPREF \_** 標記搜尋喜好設定設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="86b44-128">Set the **ADS\_SEARCHPREF\_TOMBSTONE** search preference to **TRUE**.</span></span> <span data-ttu-id="86b44-129">這會導致搜尋包含已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-129">This causes the search to include deleted objects.</span></span>
4.  <span data-ttu-id="86b44-130">將 **ADS \_ SEARCHPREF \_ PAGESIZE** 搜尋喜好設定設定為小於或等於1000的值。</span><span class="sxs-lookup"><span data-stu-id="86b44-130">Set the **ADS\_SEARCHPREF\_PAGESIZE** search preference to a value less than, or equal to, 1000.</span></span> <span data-ttu-id="86b44-131">這是選擇性的，但如果沒有這麼做，就無法抓取超過1000的已刪除物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-131">This is optional, but if this is not done, no more than 1000 deleted objects can be retrieved.</span></span>
5.  <span data-ttu-id="86b44-132">將 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) 呼叫中的搜尋篩選設定為 " (IsDeleted =**TRUE**) "。</span><span class="sxs-lookup"><span data-stu-id="86b44-132">Set the search filter in the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) call to "(isDeleted=**TRUE**)".</span></span> <span data-ttu-id="86b44-133">這會導致搜尋只取出 **isDeleted** 屬性設定為 **TRUE** 的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-133">This causes the search to only retrieve objects with the **isDeleted** attribute set to **TRUE**.</span></span>

<span data-ttu-id="86b44-134">如需示範如何列舉已刪除之物件的程式碼範例程式碼，請參閱下列 **EnumDeletedObjects** 函數範例。</span><span class="sxs-lookup"><span data-stu-id="86b44-134">For a code example code that shows how to enumerate deleted objects, see the following **EnumDeletedObjects** function example.</span></span>

<span data-ttu-id="86b44-135">您可以新增至搜尋篩選，以進一步調整搜尋，如 [LDAP 方言](/windows/desktop/ADSI/ldap-dialect)所示。</span><span class="sxs-lookup"><span data-stu-id="86b44-135">The search can be refined further by adding to the search filter as shown in [LDAP Dialect](/windows/desktop/ADSI/ldap-dialect).</span></span> <span data-ttu-id="86b44-136">例如，若要搜尋名稱開頭為 "Jeff" 的所有已刪除物件，搜尋篩選準則會設定為 " (& (isDeleted =**TRUE**)  (Cn = Jeff \*) ) "。</span><span class="sxs-lookup"><span data-stu-id="86b44-136">For example, to search for all of the deleted objects with a name that begins with "Jeff", the search filter would be set to "(&(isDeleted=**TRUE**)(cn=Jeff\*))".</span></span>

<span data-ttu-id="86b44-137">因為刪除的物件在刪除時已移除大部分的屬性，所以無法直接系結至已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-137">Because deleted objects have most of their attributes removed when they are deleted, it is not possible to bind directly to a deleted object.</span></span> <span data-ttu-id="86b44-138">系結至已刪除的物件時，必須指定 **ADS \_ FAST \_ BIND** 選項。</span><span class="sxs-lookup"><span data-stu-id="86b44-138">The **ADS\_FAST\_BIND** option must be specified when binding to a deleted object.</span></span> <span data-ttu-id="86b44-139">這表示，用來處理 Active Directory Domain Services 物件（例如 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADSPROPERTYLIST**](/windows/desktop/api/iads/nn-iads-iadspropertylist)）的 ADSI 介面不能用於已刪除的物件容器。</span><span class="sxs-lookup"><span data-stu-id="86b44-139">This means that the ADSI interfaces used to work with an Active Directory Domain Services object, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on a deleted object container.</span></span>

## <a name="finding-a-specific-deleted-object"></a><span data-ttu-id="86b44-140">尋找特定已刪除的物件</span><span class="sxs-lookup"><span data-stu-id="86b44-140">Finding a Specific Deleted Object</span></span>

<span data-ttu-id="86b44-141">您也可以找到特定已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-141">It is also possible to find a specific deleted object.</span></span> <span data-ttu-id="86b44-142">如果已知物件的 **objectGUID** ，它可以用來搜尋具有該特定 **objectGUID** 的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-142">If the **objectGUID** of the object is known, it can be used to search for the object with that specific **objectGUID**.</span></span> <span data-ttu-id="86b44-143">如需詳細資訊和示範如何尋找特定已刪除物件的程式碼範例，請參閱下面的 **FindDeletedObjectByGUID** 。</span><span class="sxs-lookup"><span data-stu-id="86b44-143">For more information and a code example that shows how to find a specific deleted object, see **FindDeletedObjectByGUID** below.</span></span>

### <a name="getdeletedobjectscontainer"></a><span data-ttu-id="86b44-144">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="86b44-144">GetDeletedObjectsContainer</span></span>

<span data-ttu-id="86b44-145">下列 c + + 程式碼範例示範如何系結至已刪除的物件容器。</span><span class="sxs-lookup"><span data-stu-id="86b44-145">The following C++ code example shows how to bind to the Deleted Objects container.</span></span>


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}

```



### <a name="enumdeletedobjects"></a><span data-ttu-id="86b44-146">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="86b44-146">EnumDeletedObjects</span></span>

<span data-ttu-id="86b44-147">下列 c + + 程式碼範例顯示如何列舉 Deleted Objects 容器中的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-147">The following C++ code example shows how to enumerate the objects in the Deleted Objects container.</span></span>


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a><span data-ttu-id="86b44-148">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="86b44-148">FindDeletedObjectByGUID</span></span>

<span data-ttu-id="86b44-149">下列 c + + 程式碼範例示範如何從物件的 **objectGUID** 屬性尋找特定已刪除的物件。</span><span class="sxs-lookup"><span data-stu-id="86b44-149">The following C++ code example shows how to find a specific deleted object from the object's **objectGUID** property.</span></span>


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 