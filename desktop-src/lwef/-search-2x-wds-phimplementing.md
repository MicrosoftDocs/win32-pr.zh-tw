---
title: 執行 WDS 的通訊協定處理常式
description: 建立通訊協定處理常式包括執行 ISearchProtocol 來管理 UrlAccessor 物件、IUrlAccessor 來產生的中繼資料，以及識別資料存放區中專案的適當篩選、IProtocolHandlerSite 來具現化 SearchProtocol 物件，並識別適當的篩選，以及 IFilterto 篩選專屬檔案，或列舉和篩選階層式儲存的檔案。
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092680"
---
# <a name="implementing-a-protocol-handler-for-wds"></a><span data-ttu-id="4649b-103">執行 WDS 的通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="4649b-103">Implementing a Protocol Handler for WDS</span></span>

> [!NOTE]
> <span data-ttu-id="4649b-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="4649b-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4649b-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="4649b-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="4649b-106">建立通訊協定處理常式包括執行 [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) 來管理 UrlAccessor 物件、 [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 來產生的中繼資料，以及識別資料存放區中專案的適當篩選、IProtocolHandlerSite 來具現化 SearchProtocol 物件，以及識別適當的篩選準則，以及使用 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)來篩選專屬檔案，或列舉和篩選階層式儲存的檔案。</span><span class="sxs-lookup"><span data-stu-id="4649b-106">Creating a protocol handler involves implementing [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) to generate metadata about and to identify appropriate filters for items in the data store, IProtocolHandlerSite to instantiate a SearchProtocol object and identify appropriate filters, and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span> <span data-ttu-id="4649b-107">通訊協定處理常式必須為多執行緒。</span><span class="sxs-lookup"><span data-stu-id="4649b-107">The protocol handler must be multithreaded.</span></span>

<span data-ttu-id="4649b-108">本章節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="4649b-108">This sections contains the following topics:</span></span>

-   [<span data-ttu-id="4649b-109">Url 上的注意事項</span><span class="sxs-lookup"><span data-stu-id="4649b-109">Note on URLs</span></span>](#note-on-urls)
-   [<span data-ttu-id="4649b-110">通訊協定處理常式介面</span><span class="sxs-lookup"><span data-stu-id="4649b-110">Protocol Handler Interfaces</span></span>](#protocol-handler-interfaces)
-   [<span data-ttu-id="4649b-111">適用于容器的 Ifilter</span><span class="sxs-lookup"><span data-stu-id="4649b-111">IFilters for Containers</span></span>](#ifilters-for-containers)
-   [<span data-ttu-id="4649b-112">新增通訊協定處理常式選項功能</span><span class="sxs-lookup"><span data-stu-id="4649b-112">Adding Protocol Handler Options Functionality</span></span>](#adding-protocol-handler-options-functionality)
    -   [<span data-ttu-id="4649b-113">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="4649b-113">ISearchProtocolOptions</span></span>](#isearchprotocoloptions)
-   [<span data-ttu-id="4649b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="4649b-114">Related topics</span></span>](#related-topics)

## <a name="note-on-urls"></a><span data-ttu-id="4649b-115">Url 上的注意事項</span><span class="sxs-lookup"><span data-stu-id="4649b-115">Note on URLs</span></span>

<span data-ttu-id="4649b-116">Windows 桌面搜尋 (WDS) 使用 Url 來唯一識別檔案系統中的專案、類似資料庫的存放區，或在網路上。</span><span class="sxs-lookup"><span data-stu-id="4649b-116">Microsoft Windows Desktop Search (WDS) uses URLs to uniquely identify items in a file system, inside a database-like store, or on the Web.</span></span> <span data-ttu-id="4649b-117">定義專案節點的 URL 稱為起始頁;WDS 開始于該起始頁面，並遞迴地編目資料存放區。</span><span class="sxs-lookup"><span data-stu-id="4649b-117">A URL that defines an entry node is called a start page; WDS begins at that start page and recursively crawls the data store.</span></span> <span data-ttu-id="4649b-118">一般的 URL 結構如下：</span><span class="sxs-lookup"><span data-stu-id="4649b-118">The typical URL structure is:</span></span>

`protocol://host/path/name.extension`

> [!Note]
>
> <span data-ttu-id="4649b-119">當您想要加入新的資料存放區時，必須選取名稱以識別與目前不衝突的名稱。</span><span class="sxs-lookup"><span data-stu-id="4649b-119">When you want to add a new data store, you'll need to select a name to identify it that does not conflict with current ones.</span></span> <span data-ttu-id="4649b-120">我們建議採用此命名慣例：公司名稱配置。</span><span class="sxs-lookup"><span data-stu-id="4649b-120">We recommend this naming convention: companyName.scheme.</span></span>

 

## <a name="protocol-handler-interfaces"></a><span data-ttu-id="4649b-121">通訊協定處理常式介面</span><span class="sxs-lookup"><span data-stu-id="4649b-121">Protocol Handler Interfaces</span></span>

<span data-ttu-id="4649b-122">**ISearchProtocol**</span><span class="sxs-lookup"><span data-stu-id="4649b-122">**ISearchProtocol**</span></span>

<span data-ttu-id="4649b-123">[**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol)介面會叫用、初始化和管理 UrlAccessor 物件。</span><span class="sxs-lookup"><span data-stu-id="4649b-123">The [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) interface invokes, initializes, and manages UrlAccessor objects.</span></span> <span data-ttu-id="4649b-124">如需有關如何執行 ISearchProtocol 介面的詳細資訊，請參閱 **ISearchProtocol 介面參考**。</span><span class="sxs-lookup"><span data-stu-id="4649b-124">For more information on implementing the ISearchProtocol interface, see **ISearchProtocol Interface reference**.</span></span>

<span data-ttu-id="4649b-125">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="4649b-125">**IUrlAccessor**</span></span>

<span data-ttu-id="4649b-126">針對指定的 URL， [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 介面會產生位置結構和包含專案的相關中繼資料，並將這些專案系結至篩選。</span><span class="sxs-lookup"><span data-stu-id="4649b-126">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface generates metadata about the location structure as well as contained items, and it binds those items to an filter.</span></span> <span data-ttu-id="4649b-127">**IUrlAccessor** 物件是由 SearchProtocol 物件具現化並初始化;不過，您也可以執行內部初始化方法，讓您的 **IUrlAccessor** 物件可以執行您的通訊協定處理常式專屬的初始化工作，例如驗證要存取之專案的 URL，或檢查上次修改的時間，以判斷是否必須在目前的編目中處理檔案。</span><span class="sxs-lookup"><span data-stu-id="4649b-127">The **IUrlAccessor** object is instantiated and initialized by an SearchProtocol object; however, you can also implement an internal initialization method so your **IUrlAccessor** object can perform initialization tasks specific to your protocol handler, such as validating the URL for an item being accessed or checking the last modified time to determine if a file must be processed in the current crawl.</span></span>

> [!Note]
>
> <span data-ttu-id="4649b-128">系統會忽略目錄的修改時間。</span><span class="sxs-lookup"><span data-stu-id="4649b-128">Modified times for directories are ignored.</span></span> <span data-ttu-id="4649b-129">[**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor)物件必須列舉子物件，以判斷是否有任何修改或刪除。</span><span class="sxs-lookup"><span data-stu-id="4649b-129">The [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) object must enumerate the child objects to determine whether there have been any modifications or deletions.</span></span>

 

<span data-ttu-id="4649b-130">**UrlAccessor** 物件的大部分設計都取決於結構是階層式或以連結為基礎。</span><span class="sxs-lookup"><span data-stu-id="4649b-130">Much of the design of the **UrlAccessor** object is dependent on whether the structure is hierarchical or link-based.</span></span> <span data-ttu-id="4649b-131">針對階層式資料存放區， **UrlAccessor** 物件必須找到可以列舉其內容的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="4649b-131">For hierarchical data stores, the **UrlAccessor** object must find an filter that can enumerate their contents.</span></span> <span data-ttu-id="4649b-132">階層式和連結式通訊協定處理常式之間的另一項差異，是使用 IsDirectory 方法。</span><span class="sxs-lookup"><span data-stu-id="4649b-132">Another distinction between hierarchical and link-based protocol handlers is the use of the IsDirectory method.</span></span> <span data-ttu-id="4649b-133">在以連結為基礎的通訊協定處理常式中，此方法應該會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="4649b-133">In link-based protocol handlers, this method should return S\_FALSE.</span></span> <span data-ttu-id="4649b-134">階層式通訊協定處理常式必須傳回 \_ 容器的 [確定]。</span><span class="sxs-lookup"><span data-stu-id="4649b-134">Hierarchical protocol handlers must return S\_OK for containers.</span></span>

<span data-ttu-id="4649b-135">如需有關如何執行 [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 介面的進一步指示，請參閱 [**IUrlAccessor 介面**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) 參考。</span><span class="sxs-lookup"><span data-stu-id="4649b-135">For further instructions on implementing an [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface, see the [**IUrlAccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) reference.</span></span>

<span data-ttu-id="4649b-136">**IProtocolHandlerSite**</span><span class="sxs-lookup"><span data-stu-id="4649b-136">**IProtocolHandlerSite**</span></span>

<span data-ttu-id="4649b-137">這個介面是用來具現化 **SearchProtocol** 物件，也會為 **UrlAccessor** 物件提供指定類別識別碼 (CLSID) 的適當篩選。</span><span class="sxs-lookup"><span data-stu-id="4649b-137">This interface is used to instantiate a **SearchProtocol** object and also provides the **UrlAccessor** object with an appropriate filter for a specified class ID (CLSID).</span></span>

## <a name="ifilters-for-containers"></a><span data-ttu-id="4649b-138">適用于容器的 Ifilter</span><span class="sxs-lookup"><span data-stu-id="4649b-138">IFilters for Containers</span></span>

<span data-ttu-id="4649b-139">如果您要執行階層式通訊協定處理常式，您必須執行容器 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)元件，以列舉代表容器或資料夾的 url。</span><span class="sxs-lookup"><span data-stu-id="4649b-139">If you are implementing a hierarchical protocol handler, you must implement a container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component that enumerates URLs representing containers or folders.</span></span> <span data-ttu-id="4649b-140">列舉程式是透過 IFilter 介面的 **GetChunk** 和 **GetValue** 方法進行迴圈，此方法會傳回代表容器中每個專案的 url 清單。</span><span class="sxs-lookup"><span data-stu-id="4649b-140">The enumeration process is a loop through the **GetChunk** and **GetValue** methods of the IFilter interface that return a list of URLs that represent each item in the container.</span></span>

<span data-ttu-id="4649b-141">首先， **GetChunk** 會傳回具有屬性 set 收集 PROPSET 的 FULLPROSPEC \_ ，以及下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="4649b-141">First, **GetChunk** returns a FULLPROSPEC with the property set GATHER\_PROPSET and either:</span></span>

-   <span data-ttu-id="4649b-142">PID \_ GTHR \_ DIRLINK、不含上次修改時間之專案的 URL，或</span><span class="sxs-lookup"><span data-stu-id="4649b-142">PID\_GTHR\_DIRLINK, the URL to the item without the last modified time, or</span></span>
-   <span data-ttu-id="4649b-143">PID \_ GTHR \_ DIRLINK \_ WITH \_ TIME、URL 以及上次修改時間</span><span class="sxs-lookup"><span data-stu-id="4649b-143">PID\_GTHR\_DIRLINK\_WITH\_TIME, the URL along with the last modified time</span></span>

<span data-ttu-id="4649b-144">收集 PROPSET 的屬性集 GUID \_ 是0B63E343-9CCC-11D0-BCDB-00805FCCCE04。</span><span class="sxs-lookup"><span data-stu-id="4649b-144">The property set GUID for GATHER\_PROPSET is 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span></span> <span data-ttu-id="4649b-145">PROPSPEC 屬性可以是 PID \_ GTHR \_ DIRLINK = 2 或 pid \_ GTHR \_ DIRLINK \_ ， \_ 時間 = 12 decimal。</span><span class="sxs-lookup"><span data-stu-id="4649b-145">The PROPSPEC Property is either PID\_GTHR\_DIRLINK=2 or PID\_GTHR\_DIRLINK\_WITH\_TIME = 12 decimal.</span></span>

<span data-ttu-id="4649b-146">\_以時間傳回 PID GTHR \_ DIRLINK \_ \_ 會更有效率，因為索引子可以立即判斷是否需要為專案編制索引，而不需要呼叫 ISearchProtocol->CreateUrlAccessor () 和 IUrlAccessor >GetLastModified () 方法。</span><span class="sxs-lookup"><span data-stu-id="4649b-146">Returning PID\_GTHR\_DIRLINK\_WITH\_TIME is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the ISearchProtocol->CreateUrlAccessor() and IUrlAccessor->GetLastModified() methods.</span></span>

<span data-ttu-id="4649b-147">然後，如果使用) ，則 **GetValue** 會傳回 URL (和上次修改時間的 PROPVARIANT，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4649b-147">Then **GetValue** returns a PROPVARIANT for the URL (and last modified time if used), as either:</span></span>

-   <span data-ttu-id="4649b-148">VT \_ LPWSTR、子專案的 URL，或</span><span class="sxs-lookup"><span data-stu-id="4649b-148">VT\_LPWSTR, the URL of the child item, or</span></span>
-   <span data-ttu-id="4649b-149">URL 的向量，後面接著 FILETIME</span><span class="sxs-lookup"><span data-stu-id="4649b-149">Vector of the URL followed by a FILETIME</span></span>

<span data-ttu-id="4649b-150">下列範例程式碼示範如何使用時間來建立適當的 PID \_ GTHR \_ DIRLINK \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4649b-150">The following sample code demonstrates how to build the proper PID\_GTHR\_DIRLINK\_WITH\_TIME.</span></span>

> [!Note]
>
> <span data-ttu-id="4649b-151">**此程式碼和資訊是以「原樣」提供，不含任何明示或默示擔保，包括但不限於特定用途的適售性及/或適用性默示擔保。**</span><span class="sxs-lookup"><span data-stu-id="4649b-151">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="4649b-152">著作權 (C) Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4649b-152">Copyright (C) Microsoft.</span></span> <span data-ttu-id="4649b-153">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="4649b-153">All rights reserved.</span></span>

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]
>
> <span data-ttu-id="4649b-154">容器 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)元件應該一律列舉所有的子 url，即使子 url 未變更，因為索引子會透過列舉進程偵測刪除。</span><span class="sxs-lookup"><span data-stu-id="4649b-154">A container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component should always enumerate all child URLs even if the child URLs have not changed, because the Indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="4649b-155">如果 DIR 連結中的日期輸出 \_ \_ \_ 指出資料尚未變更，則索引子不會更新該 URL 的資料。</span><span class="sxs-lookup"><span data-stu-id="4649b-155">If the date output in a DIR\_LINKS\_WITH\_TIME indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

<span data-ttu-id="4649b-156">實體 URL 是 **UrlAccessor** 物件處理的 url。</span><span class="sxs-lookup"><span data-stu-id="4649b-156">The physical URL is the URL that the **UrlAccessor** object processes.</span></span> <span data-ttu-id="4649b-157">如果篩選不會發出方便使用的 DisplayUrl，WDS 會在搜尋結果中顯示使用者的實體 URL。</span><span class="sxs-lookup"><span data-stu-id="4649b-157">If the filter does not emit a user-friendly DisplayUrl, WDS displays the physical URL to the user as part of the search results.</span></span> <span data-ttu-id="4649b-158">WDS 架構包含兩個屬性，可控制要對終端使用者顯示的內容，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="4649b-158">The WDS schema contains two properties to control what is displayed to the end user, as shown in the table below.</span></span>



| <span data-ttu-id="4649b-159">GUID</span><span class="sxs-lookup"><span data-stu-id="4649b-159">GUID</span></span>                                 | <span data-ttu-id="4649b-160">PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="4649b-160">PROPSPEC</span></span>      | <span data-ttu-id="4649b-161">Description</span><span class="sxs-lookup"><span data-stu-id="4649b-161">Description</span></span>                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| <span data-ttu-id="4649b-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="4649b-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="4649b-163">DisplayFolder</span><span class="sxs-lookup"><span data-stu-id="4649b-163">DisplayFolder</span></span> | <span data-ttu-id="4649b-164">在搜尋結果中顯示給使用者的資料夾路徑</span><span class="sxs-lookup"><span data-stu-id="4649b-164">Folder Path displayed to the user in search results</span></span> |
| <span data-ttu-id="4649b-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="4649b-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="4649b-166">FolderName</span><span class="sxs-lookup"><span data-stu-id="4649b-166">FolderName</span></span>    | <span data-ttu-id="4649b-167">父資料夾的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4649b-167">Display name of the parent folder</span></span>                   |



 

<span data-ttu-id="4649b-168">如果您的程式碼未發出 DisplayFolder 或資料夾資料夾，則會從 DisplayUrl 計算這些值。</span><span class="sxs-lookup"><span data-stu-id="4649b-168">If your code does not emit a DisplayFolder or FolderName, these values are computed from the DisplayUrl.</span></span> <span data-ttu-id="4649b-169">URL 中的正斜線代表存放區或檔案系統內的容器。</span><span class="sxs-lookup"><span data-stu-id="4649b-169">Forward slashes in the URL denote containers within the store or file system.</span></span>

## <a name="adding-protocol-handler-options-functionality"></a><span data-ttu-id="4649b-170">新增通訊協定處理常式選項功能</span><span class="sxs-lookup"><span data-stu-id="4649b-170">Adding Protocol Handler Options Functionality</span></span>

<span data-ttu-id="4649b-171">若要讓您的通訊協定處理常式具有預設起始頁 (和專案節點 URL) ，您必須執行 **ISearchProtocolOptions** 介面。</span><span class="sxs-lookup"><span data-stu-id="4649b-171">For your protocol handler to have a default start page (and entry node URL), you must implement the **ISearchProtocolOptions** interface.</span></span> <span data-ttu-id="4649b-172">在未來的 WDS 版本中，這個介面會提供 [選項] 對話方塊的勾點，以提供增強的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="4649b-172">In future versions of WDS, this interface will provide hooks to the Options dialog for an enhanced user experience.</span></span> <span data-ttu-id="4649b-173">此介面提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="4649b-173">This interface provides the following functionality:</span></span>

-   <span data-ttu-id="4649b-174">判斷是否符合通訊協定處理常式的需求。</span><span class="sxs-lookup"><span data-stu-id="4649b-174">Determines whether the requirements for your protocol handler are met.</span></span> <span data-ttu-id="4649b-175">例如，您的通訊協定處理常式存放區可能需要存取指定的應用程式，才能正確地為應用程式的資料編制索引，但應用程式無法使用。</span><span class="sxs-lookup"><span data-stu-id="4649b-175">For example, your protocol handler's store may require access to a given application to properly index the application's data but that application is unavailable.</span></span>
-   <span data-ttu-id="4649b-176">識別您的通訊協定處理常式處理專案所需的最低需求。</span><span class="sxs-lookup"><span data-stu-id="4649b-176">Identifies the minimum requirements your protocol handler needs to process an item.</span></span> <span data-ttu-id="4649b-177">您可以使用易記的當地語系化描述來表示需求，例如「Microsoft Outlook 2000 或更高版本」。</span><span class="sxs-lookup"><span data-stu-id="4649b-177">Requirements can be expressed in a user-friendly, localized description, such as "Microsoft Outlook 2000 or greater."</span></span>
-   <span data-ttu-id="4649b-178">定義通訊協定處理常式預設應處理的 Url。</span><span class="sxs-lookup"><span data-stu-id="4649b-178">Defines the URLs your protocol handler should process by default.</span></span>

### <a name="isearchprotocoloptions"></a><span data-ttu-id="4649b-179">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="4649b-179">ISearchProtocolOptions</span></span>

<span data-ttu-id="4649b-180">下表說明您需要針對 **ISearchProtocolOptions** 介面執行的方法。</span><span class="sxs-lookup"><span data-stu-id="4649b-180">The following table describes the methods you need to implement for the **ISearchProtocolOptions** interface.</span></span>



| <span data-ttu-id="4649b-181">方法</span><span class="sxs-lookup"><span data-stu-id="4649b-181">Method</span></span>               | <span data-ttu-id="4649b-182">描述</span><span class="sxs-lookup"><span data-stu-id="4649b-182">Description</span></span>                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4649b-183">CheckRequirements</span><span class="sxs-lookup"><span data-stu-id="4649b-183">CheckRequirements</span></span>    | <span data-ttu-id="4649b-184">判斷是否符合自訂通訊協定處理常式的最低需求</span><span class="sxs-lookup"><span data-stu-id="4649b-184">Determines whether a custom protocol handler's minimum requirements are met</span></span>                             |
| <span data-ttu-id="4649b-185">GetDefaultCrawlScope</span><span class="sxs-lookup"><span data-stu-id="4649b-185">GetDefaultCrawlScope</span></span> | <span data-ttu-id="4649b-186">針對自訂通訊協定處理常式，傳回指定存放區內的預設 Url 清單</span><span class="sxs-lookup"><span data-stu-id="4649b-186">Returns a list of default URLs within a specified store for a custom protocol handler</span></span>                   |
| <span data-ttu-id="4649b-187">GetRequirements</span><span class="sxs-lookup"><span data-stu-id="4649b-187">GetRequirements</span></span>      | <span data-ttu-id="4649b-188">識別自訂通訊協定處理常式之最低需求的使用者易記當地語系化描述</span><span class="sxs-lookup"><span data-stu-id="4649b-188">Identifies a user-friendly, localized description of minimum requirements for a custom protocol handler</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4649b-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="4649b-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4649b-190">**參考**</span><span class="sxs-lookup"><span data-stu-id="4649b-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4649b-191">通知索引變更</span><span class="sxs-lookup"><span data-stu-id="4649b-191">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="4649b-192">使用 Shell 擴充功能新增圖示、預覽和內容功能表</span><span class="sxs-lookup"><span data-stu-id="4649b-192">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="4649b-193">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="4649b-193">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 