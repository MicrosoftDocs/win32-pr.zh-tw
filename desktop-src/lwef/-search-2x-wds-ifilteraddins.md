---
title: 開發 IFilter 增益集
description: 您可以使用篩選增益集（可執行 IFilterinterface 的元件）擴充 Microsoft Windows 桌面搜尋 (WDS) ，以包含新的檔案類型。
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f846cf2101eefc17b1e92fbd7992529a06fb43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463100"
---
# <a name="developing-ifilter-add-ins"></a><span data-ttu-id="0b4c3-103">開發 IFilter 增益集</span><span class="sxs-lookup"><span data-stu-id="0b4c3-103">Developing IFilter Add-ins</span></span>

> [!NOTE]
> <span data-ttu-id="0b4c3-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0b4c3-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="0b4c3-106">您可以使用篩選增益集（可執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面的元件）擴充 Microsoft Windows 桌面搜尋 (WDS) ，以包含新的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-106">You can extend Microsoft Windows Desktop Search (WDS) with filter add-ins, components that implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface, to include new file types.</span></span> <span data-ttu-id="0b4c3-107">篩選準則負責存取和剖析檔案中的資料，以及傳回屬性和值的配對，以及用來編制索引的文字區塊。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-107">Filters are responsible for accessing and parsing data in files and for returning pairs of properties and values as well as chunks of text for indexing.</span></span> <span data-ttu-id="0b4c3-108">在編制索引過程中，WDS 會使用每個檔案或專案的 URL 來呼叫適當的篩選。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-108">During the indexing process, WDS calls the appropriate filter with the URL for each file or item.</span></span> <span data-ttu-id="0b4c3-109">篩選準則會先解壓縮對應至 WDS 架構中標示為可抓取之屬性的中繼資料，例如標題、檔案大小和上次修改日期。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-109">The filter first extracts metadata that corresponds to properties that are marked retrievable in the WDS schema, such as title, file size, and last modified date.</span></span> <span data-ttu-id="0b4c3-110">然後，它會將專案內容分割成文字區塊。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-110">Then it breaks the item content into chunks of text.</span></span> <span data-ttu-id="0b4c3-111">WDS 會將篩選所傳回的屬性和文字新增至目錄。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-111">WDS adds the properties and text returned by the filter to the catalog.</span></span> <span data-ttu-id="0b4c3-112">WDS 可以為具有已註冊篩選的任何檔案類型編制索引。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-112">WDS can index any file type for which it has a registered filter.</span></span>

<span data-ttu-id="0b4c3-113">在某些情況下，您不需要撰寫新的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-113">In some circumstances, you do not need to write a new filter.</span></span> <span data-ttu-id="0b4c3-114">WDS 2.x 包含超過200種專案類型的篩選 (包括 HTML、XML 和原始程式碼檔案等純文字專案) ，並使用與 SharePoint 服務相同的 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)技術。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-114">WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)technology as SharePoint Services.</span></span> <span data-ttu-id="0b4c3-115">如果您已針對檔案類型安裝篩選器，WDS 可以使用這些現有的篩選來編制此資料的索引。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-115">If you already have filters installed for your file types, WDS can use those existing filters to index this data.</span></span> <span data-ttu-id="0b4c3-116">此外，WDS 也包含純文字格式之檔案類型的一般篩選。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-116">Furthermore, WDS includes a general filter for file types that are plaintext-based.</span></span> <span data-ttu-id="0b4c3-117">如果您的檔案類型可以由現有的 SharePoint Services 篩選或純文字篩選器處理，您可以將副檔名和篩選 GUID 新增至登錄，讓 WDS 可以找到並使用它 (如需詳細資訊，請參閱 [註冊篩選增益集](#to-register-a-filter-add-in)) 。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-117">If you have a file type that can be processed by either an existing SharePoint Services filter or the plaintext filter, you can add the file name extension and filter GUID to the Registry so WDS can locate and use it (see [To Register a Filter Add-in](#to-register-a-filter-add-in) for more information).</span></span>

<span data-ttu-id="0b4c3-118">但是，如果您有非純文字和專屬的資料或檔案格式，則撰寫自訂篩選器會是確保 WDS 可以在目錄中編制檔案格式的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-118">If, however, you have a non-plaintext and proprietary data or file format, writing a custom filter implementation is the only way to ensure WDS can index the file format in the catalog.</span></span> <span data-ttu-id="0b4c3-119">檔案類型只能有一個篩選增益集，因此可以覆寫現有的篩選，或針對特定檔案類型覆寫其他篩選器。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-119">You can have only one filter add-in for a file type, so it is possible to override an existing filter or to have another filter override yours for a specific file type.</span></span>

<span data-ttu-id="0b4c3-120">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="0b4c3-121">必要的篩選介面</span><span class="sxs-lookup"><span data-stu-id="0b4c3-121">Required Filter Interfaces</span></span>](#required-filter-interfaces)
    -   [<span data-ttu-id="0b4c3-122">IFilter 介面</span><span class="sxs-lookup"><span data-stu-id="0b4c3-122">IFilter Interface</span></span>](#ifilter-interface)
    -   [<span data-ttu-id="0b4c3-123">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="0b4c3-123">IPersistStream</span></span>](#ipersiststream)
    -   [<span data-ttu-id="0b4c3-124">IPersistFile</span><span class="sxs-lookup"><span data-stu-id="0b4c3-124">IPersistFile</span></span>](#ipersistfile)
    -   [<span data-ttu-id="0b4c3-125">IPersistStorage</span><span class="sxs-lookup"><span data-stu-id="0b4c3-125">IPersistStorage</span></span>](#ipersiststorage)
-   [<span data-ttu-id="0b4c3-126">使用篩選器輸出屬性</span><span class="sxs-lookup"><span data-stu-id="0b4c3-126">Outputting Properties with Filters</span></span>](#outputting-properties-with-filters)
    -   [<span data-ttu-id="0b4c3-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="0b4c3-127">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="0b4c3-128">篩選增益集安裝</span><span class="sxs-lookup"><span data-stu-id="0b4c3-128">Filter Add-in Installation</span></span>](#filter-add-in-installation)
    -   [<span data-ttu-id="0b4c3-129">註冊所需的 Clsid</span><span class="sxs-lookup"><span data-stu-id="0b4c3-129">CLSIDs Required for Registration</span></span>](#clsids-required-for-registration)
    -   [<span data-ttu-id="0b4c3-130">註冊模型</span><span class="sxs-lookup"><span data-stu-id="0b4c3-130">Registration Model</span></span>](#registration-model)
    -   [<span data-ttu-id="0b4c3-131">註冊篩選增益集</span><span class="sxs-lookup"><span data-stu-id="0b4c3-131">To Register a Filter Add-in</span></span>](#to-register-a-filter-add-in)
-   [<span data-ttu-id="0b4c3-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b4c3-132">Related topics</span></span>](#related-topics)

## <a name="required-filter-interfaces"></a><span data-ttu-id="0b4c3-133">必要的篩選介面</span><span class="sxs-lookup"><span data-stu-id="0b4c3-133">Required Filter Interfaces</span></span>

<span data-ttu-id="0b4c3-134">篩選增益集必須執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面和下列其中一個介面：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-134">A filter add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface and one of the following interfaces:</span></span>

-   <span data-ttu-id="0b4c3-135">[IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -從資料流程載入資料。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-135">[IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) - To load data from a stream.</span></span> <span data-ttu-id="0b4c3-136">這比使用檔案更安全，因為沒有寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-136">This is more secure than using files because nothing is written to disk.</span></span> <span data-ttu-id="0b4c3-137">IPersistStream 介面是向前相容于 Windows Vista 的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-137">The IPersistStream interface is the preferred method for forward compatibility with Windows Vista.</span></span>
-   <span data-ttu-id="0b4c3-138">[IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile) -從檔案載入資料。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-138">[IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) - To load data from a file.</span></span> <span data-ttu-id="0b4c3-139">Windows Vista 不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-139">This interface is not supported in Windows Vista.</span></span>
-   <span data-ttu-id="0b4c3-140">[IPersistStorage 介面](/windows/win32/api/objidl/nn-objidl-ipersiststorage) -從 OLE COM 結構化儲存體載入資料。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-140">[IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) - To load data from an OLE COM Structured Storage.</span></span>

<span data-ttu-id="0b4c3-141">篩選增益集會使用這些介面來取得專案的內容，並以反復方式將它們傳回至索引，直到到達檔案結尾為止。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-141">A filter add-in uses these interfaces to get the contents of the item and return them iteratively to the index until the end of the file is reached.</span></span> <span data-ttu-id="0b4c3-142">篩選增益集應該盡可能健全，以處理損毀的檔案，以及不符合預期輸入格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-142">A filter add-in should be as robust as possible to handle corrupt files and those that do not meet expected input formats.</span></span>

### <a name="ifilter-interface"></a><span data-ttu-id="0b4c3-143">IFilter 介面</span><span class="sxs-lookup"><span data-stu-id="0b4c3-143">IFilter Interface</span></span>

<span data-ttu-id="0b4c3-144">這是篩選器執行所需的介面。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-144">This is a required interface for a filter implementation.</span></span> <span data-ttu-id="0b4c3-145">如需詳細資訊，請參閱 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面參考。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-145">For more information, see the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface reference.</span></span>



| <span data-ttu-id="0b4c3-146">方法</span><span class="sxs-lookup"><span data-stu-id="0b4c3-146">Method</span></span>       | <span data-ttu-id="0b4c3-147">描述</span><span class="sxs-lookup"><span data-stu-id="0b4c3-147">Description</span></span>                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4c3-148">Init () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-148">Init()</span></span>       | <span data-ttu-id="0b4c3-149">初始化篩選會話。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-149">Initializes a filtering session.</span></span>                                                       |
| <span data-ttu-id="0b4c3-150">GetChunk () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-150">GetChunk()</span></span>   | <span data-ttu-id="0b4c3-151">將篩選置於第一個或下一個區塊的開頭，並傳回描述項。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-151">Positions the filter at the beginning of first or next chunk and returns a descriptor.</span></span> |
| <span data-ttu-id="0b4c3-152">GetText () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-152">GetText()</span></span>    | <span data-ttu-id="0b4c3-153">抓取目前區塊中的文字。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-153">Retrieves text from the current chunk.</span></span>                                                 |
| <span data-ttu-id="0b4c3-154">GetValue()</span><span class="sxs-lookup"><span data-stu-id="0b4c3-154">GetValue()</span></span>   | <span data-ttu-id="0b4c3-155">從目前的區塊抓取屬性值。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-155">Retrieves property values from the current chunk.</span></span>                                      |
| <span data-ttu-id="0b4c3-156">BindRegion () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-156">BindRegion()</span></span> | <span data-ttu-id="0b4c3-157">目前保留供內部使用;請勿實行。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-157">Currently reserved for internal use; do not implement.</span></span> <span data-ttu-id="0b4c3-158">這個方法會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-158">This method returns E\_NOTIMPL.</span></span> |



 

### <a name="ipersiststream"></a><span data-ttu-id="0b4c3-159">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="0b4c3-159">IPersistStream</span></span>

<span data-ttu-id="0b4c3-160">這個介面會從資料流程載入檔案，以比 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile) 更安全處理，因為執行 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 篩選器的內容不需要在磁片上或透過網路開啟任何檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-160">This interface loads a file from a stream for more secure processing than [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) because the context in which a [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) filter runs does not need the rights to open any files on the disk or over the network.</span></span> <span data-ttu-id="0b4c3-161">在存取單一檔案的兩個方法中，這是與 Windows 向前相容的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-161">Of the two methods for accessing a single file, this is the preferred method for forward compatibility with Windows.</span></span>



| <span data-ttu-id="0b4c3-162">方法</span><span class="sxs-lookup"><span data-stu-id="0b4c3-162">Method</span></span>       | <span data-ttu-id="0b4c3-163">描述</span><span class="sxs-lookup"><span data-stu-id="0b4c3-163">Description</span></span>                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4c3-164">IsDirty () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-164">IsDirty()</span></span>    | <span data-ttu-id="0b4c3-165">檢查是否有變更。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-165">Checks if there has been a change.</span></span> <span data-ttu-id="0b4c3-166">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-166">This method returns E\_NOTIMPL in filters.</span></span>                                                                      |
| <span data-ttu-id="0b4c3-167">InitNew () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-167">InitNew()</span></span>    | <span data-ttu-id="0b4c3-168">建立新的存放裝置。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-168">Creates a new storage.</span></span> <span data-ttu-id="0b4c3-169">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-169">This method returns E\_NOTIMPL in filters.</span></span>                                                                                  |
| <span data-ttu-id="0b4c3-170">載入 () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-170">Load()</span></span>       | <span data-ttu-id="0b4c3-171">從先前儲存物件的資料流來初始化它。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-171">Initializes an object from the stream where it was previously saved.</span></span>                                                                               |
| <span data-ttu-id="0b4c3-172">儲存 () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-172">Save()</span></span>       | <span data-ttu-id="0b4c3-173">將物件儲存至指定的資料流程，並指出物件是否應該重設其中途旗標。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-173">Saves an object into the specified stream and indicates whether the object should reset its dirty flag.</span></span> <span data-ttu-id="0b4c3-174">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-174">This method returns E\_NOTIMPL in filters.</span></span> |
| <span data-ttu-id="0b4c3-175">GetSizeMax () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-175">GetSizeMax()</span></span> | <span data-ttu-id="0b4c3-176">傳回儲存物件所需資料流的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-176">Returns the size in bytes of the stream needed to save the object.</span></span> <span data-ttu-id="0b4c3-177">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-177">This method returns E\_NOTIMPL in filters.</span></span>                                      |



 

### <a name="ipersistfile"></a><span data-ttu-id="0b4c3-178">IPersistFile</span><span class="sxs-lookup"><span data-stu-id="0b4c3-178">IPersistFile</span></span>

<span data-ttu-id="0b4c3-179">此介面會依絕對路徑載入檔案，而且在 Windows Vista 中不支援。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-179">This interface loads a file by absolute path and is not supported in Windows Vista.</span></span>



| <span data-ttu-id="0b4c3-180">方法</span><span class="sxs-lookup"><span data-stu-id="0b4c3-180">Method</span></span>          | <span data-ttu-id="0b4c3-181">描述</span><span class="sxs-lookup"><span data-stu-id="0b4c3-181">Description</span></span>                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4c3-182">GetCurFile () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-182">GetCurFile()</span></span>    | <span data-ttu-id="0b4c3-183">取得與物件相關聯之檔案的目前名稱。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-183">Gets the current name of the file associated with the object.</span></span> <span data-ttu-id="0b4c3-184">傳回 Load () 中指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-184">Returns the path specified in Load().</span></span>                          |
| <span data-ttu-id="0b4c3-185">載入 () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-185">Load()</span></span>          | <span data-ttu-id="0b4c3-186">開啟指定的檔案，並從檔案連接初始化物件。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-186">Opens the specified file and initializes an object from the file contents.</span></span> <span data-ttu-id="0b4c3-187">您可以延遲開啟檔案，直到需要為止。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-187">You can delay opening the file until you need it.</span></span> |
| <span data-ttu-id="0b4c3-188">GetClassID () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-188">GetClassID()</span></span>    | <span data-ttu-id="0b4c3-189">針對新的檔案類型，傳回 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-189">Returns the class identifier (CLSID) for the new file type.</span></span> <span data-ttu-id="0b4c3-190">您應該使用 uuidgen.exe 來產生唯一的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-190">You should use uuidgen.exe to generate a unique CLSID.</span></span>           |
| <span data-ttu-id="0b4c3-191">IsDirty () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-191">IsDirty()</span></span>       | <span data-ttu-id="0b4c3-192">只需要 \_ 在篩選器中傳回 E >notimpl</span><span class="sxs-lookup"><span data-stu-id="0b4c3-192">Need only return E\_NOTIMPL in filters</span></span>                                                                                       |
| <span data-ttu-id="0b4c3-193">儲存 () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-193">Save()</span></span>          | <span data-ttu-id="0b4c3-194">只需要 \_ 在篩選器中傳回 E >notimpl</span><span class="sxs-lookup"><span data-stu-id="0b4c3-194">Need only return E\_NOTIMPL in filters</span></span>                                                                                       |
| <span data-ttu-id="0b4c3-195">SaveCompleted () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-195">SaveCompleted()</span></span> | <span data-ttu-id="0b4c3-196">只需要 \_ 在篩選器中傳回 E >notimpl</span><span class="sxs-lookup"><span data-stu-id="0b4c3-196">Need only return E\_NOTIMPL in filters</span></span>                                                                                       |



 

### <a name="ipersiststorage"></a><span data-ttu-id="0b4c3-197">IPersistStorage</span><span class="sxs-lookup"><span data-stu-id="0b4c3-197">IPersistStorage</span></span>

<span data-ttu-id="0b4c3-198">此介面支援結構化儲存體模型，其中每個包含的物件都有它自己的儲存區，它會嵌套在容器的儲存體中。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-198">This interface supports the structured storage model, in which each contained object has its own storage that is nested within the container's storage.</span></span> <span data-ttu-id="0b4c3-199">如同 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile)，這個介面會依絕對路徑載入，而且在 Windows Vista 中不受支援。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-199">Like [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile), this interface loads by absolute path and is not supported in Windows Vista.</span></span>



| <span data-ttu-id="0b4c3-200">方法</span><span class="sxs-lookup"><span data-stu-id="0b4c3-200">Method</span></span>            | <span data-ttu-id="0b4c3-201">描述</span><span class="sxs-lookup"><span data-stu-id="0b4c3-201">Description</span></span>                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4c3-202">IsDirty () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-202">IsDirty()</span></span>         | <span data-ttu-id="0b4c3-203">檢查是否有變更。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-203">Checks if there has been a change.</span></span> <span data-ttu-id="0b4c3-204">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-204">This method returns E\_NOTIMPL in filters.</span></span>                                 |
| <span data-ttu-id="0b4c3-205">InitNew () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-205">InitNew()</span></span>         | <span data-ttu-id="0b4c3-206">建立新的存放裝置。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-206">Creates a new storage.</span></span> <span data-ttu-id="0b4c3-207">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-207">This method returns E\_NOTIMPL in filters.</span></span>                                             |
| <span data-ttu-id="0b4c3-208">載入 () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-208">Load()</span></span>            | <span data-ttu-id="0b4c3-209">儲存儲存體。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-209">Saves the storage.</span></span> <span data-ttu-id="0b4c3-210">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-210">This method returns E\_NOTIMPL in filters.</span></span>                                                 |
| <span data-ttu-id="0b4c3-211">儲存 () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-211">Save()</span></span>            | <span data-ttu-id="0b4c3-212">傳回儲存物件所需資料流的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-212">Returns the size in bytes of the stream needed to save the object.</span></span> <span data-ttu-id="0b4c3-213">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-213">This method returns E\_NOTIMPL in filters.</span></span> |
| <span data-ttu-id="0b4c3-214">SaveCompleted () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-214">SaveCompleted()</span></span>   | <span data-ttu-id="0b4c3-215">保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-215">Reserved for internal use.</span></span> <span data-ttu-id="0b4c3-216">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-216">This method returns E\_NOTIMPL in filters.</span></span>                                         |
| <span data-ttu-id="0b4c3-217">HandsOffStorage () </span><span class="sxs-lookup"><span data-stu-id="0b4c3-217">HandsOffStorage()</span></span> | <span data-ttu-id="0b4c3-218">保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-218">Reserved for internal use.</span></span> <span data-ttu-id="0b4c3-219">這個方法會傳回 \_ 篩選中的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-219">This method returns E\_NOTIMPL in filters.</span></span>                                         |



 

## <a name="outputting-properties-with-filters"></a><span data-ttu-id="0b4c3-220">使用篩選器輸出屬性</span><span class="sxs-lookup"><span data-stu-id="0b4c3-220">Outputting Properties with Filters</span></span>

<span data-ttu-id="0b4c3-221">篩選準則的目的是要將檔案的內容和屬性解壓縮，以包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-221">The purpose of a filter is to extract the content and properties of files for inclusion in the full-text index.</span></span> <span data-ttu-id="0b4c3-222">WDS 會先呼叫 IPersistFile、IPersistStream 或 IPersistStorage 執行的 Load 方法，然後再叫用 IFilter 執行的 Init 方法。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-222">WDS first calls the Load method on either the IPersistFile, IPersistStream, or IPersistStorage implementations and then invokes the Init method of the IFilter implementation.</span></span> <span data-ttu-id="0b4c3-223">**GetChunk** 被呼叫來取出文字或屬性值資料的區塊，然後視需要呼叫 **GetText** 或 **GetValue** ，以抓取與區塊相關聯的所有文字或屬性值。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-223">**GetChunk** is called to retrieve chunks of text or property value data, and then either **GetText** or **GetValue** is called as many times as needed to retrieve all of the text or property values associated with the chunk.</span></span> <span data-ttu-id="0b4c3-224">此程式會重複，直到 **GetChunk** 回報檔中沒有其他區塊為止。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-224">This process repeats until **GetChunk** reports that there are no more chunks in the document.</span></span>

<span data-ttu-id="0b4c3-225">**GetChunk** 方法會從要篩選的檔案抓取第一個或下一個邏輯區塊資訊的相關資訊，並將該資訊傳回 \_ 至 STAT 區塊結構，包括單純遞增的區塊識別碼、目前區塊與先前區塊之間的關聯狀態資訊、旗標，指出區塊是否包含文字或值、區塊的地區設定，以及區塊的屬性規格。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-225">The **GetChunk** method retrieves information about the first or next logical block of information from the file being filtered and returns that information in a STAT\_CHUNK structure, including a monotonically increasing chunk ID, status information about how the current chunk relates to the previous chunk, a flag indicating whether the chunk contains text or a value, the chunk's locale, and the chunk's property specification.</span></span> <span data-ttu-id="0b4c3-226">屬性規格是由 CLSID 和整數或字串屬性 (識別碼所組成的 [**FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) ，例如 D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType) 。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-226">The property specification is a [**FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) consisting of a CLSID and either an integer or string property identifier (for example, D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType).</span></span> <span data-ttu-id="0b4c3-227">它會識別屬性的類型，而不是屬性值本身。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-227">It identifies the type of property rather than the property value itself.</span></span>

<span data-ttu-id="0b4c3-228">區塊地區設定識別碼是用來選擇適當的斷詞工具，您必須正確地加以識別。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-228">The chunk locale identifier is used to choose an appropriate word breaker, and it is very important that you correctly identify it.</span></span> <span data-ttu-id="0b4c3-229">如果篩選準則無法判斷文字的地區設定，則應該假設預設的系統地區設定，可使用 **GetSystemDefaultLCID** 取得。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-229">If the filter cannot determine the locale of the text, it should assume the default system locale, available by using **GetSystemDefaultLCID**.</span></span> <span data-ttu-id="0b4c3-230">如果您控制檔案格式，但目前不包含地區設定資訊，您應該新增使用者功能，以啟用適當的地區設定識別。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-230">If you control the file format and it currently does not contain locale information, you should add a user feature to enable proper locale identification.</span></span> <span data-ttu-id="0b4c3-231">使用不相符的斷詞工具可能會導致使用者的查詢體驗不良。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-231">Using a mismatched word breaker can lead to a bad query experience for the user.</span></span>

<span data-ttu-id="0b4c3-232">**GetChunk** 只會管理存取區塊，且不會傳回文字或屬性值本身。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-232">**GetChunk** only manages accessing chunks and does not return the text or property value itself.</span></span> <span data-ttu-id="0b4c3-233">相反地，後續呼叫 **GetText** 和 **GetValue** 會取出區塊的主體。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-233">Rather, subsequent calls to **GetText** and **GetValue** retrieve the body of the chunk.</span></span> <span data-ttu-id="0b4c3-234">**GetText** 會從目前的區塊文字區塊傳回文字區塊，也就是 Unicode 字串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-234">**GetText** returns text chunks, which are Unicode strings, from the current CHUNK\_TEXT chunk.</span></span> <span data-ttu-id="0b4c3-235">如果目前的區塊太大，則可能需要一個以上的 **GetText** 方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-235">If the current chunk is too large, more than one call to the **GetText** method can be required.</span></span> <span data-ttu-id="0b4c3-236">每次呼叫 **GetText** 方法時，都會抓取緊接在最後一次呼叫 **GetText** 方法的文字後面的文字。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-236">Each call to the **GetText** method retrieves text that immediately follows the text from the last call to the **GetText** method.</span></span> <span data-ttu-id="0b4c3-237">例如，一個呼叫中的最後一個字元可以位於單字的中間，而下一個呼叫中的第一個字元會繼續該字。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-237">For example, the last character from one call can be in the middle of a word, and the first character in the next call would continue that word.</span></span> <span data-ttu-id="0b4c3-238">搜尋引擎必須處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-238">Search engines must handle this situation.</span></span>

<span data-ttu-id="0b4c3-239">**GetValue** \_ 會傳回 PROPVARIANT 結構中目前區塊值區塊的屬性值，其可保存各種不同的資料類型。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-239">**GetValue** returns property values for the current CHUNK\_VALUE chunk in PROPVARIANT structures, which can hold a wide variety of data types.</span></span> <span data-ttu-id="0b4c3-240">**GetValue** 必須使用 CoTaskMemAlloc 來配置 PROPVARIANT 結構本身。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-240">**GetValue** must allocate the PROPVARIANT structure itself using CoTaskMemAlloc.</span></span> <span data-ttu-id="0b4c3-241">**GetValue** 的呼叫端負責釋放 PROPVARIANT 使用 PropVariantClear 所指向的記憶體，以及使用 CoTaskMemFree 釋放結構本身。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-241">The caller of **GetValue** is responsible for freeing memory pointed to by the PROPVARIANT using PropVariantClear, and for freeing the structure itself with CoTaskMemFree.</span></span> <span data-ttu-id="0b4c3-242">如需 PROPVARIANTs 的詳細資訊，請參閱 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 參考。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-242">For more information on PROPVARIANTs, see the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) reference.</span></span>

### <a name="property-values"></a><span data-ttu-id="0b4c3-243">屬性值</span><span class="sxs-lookup"><span data-stu-id="0b4c3-243">Property Values</span></span>

<span data-ttu-id="0b4c3-244">篩選器最少應輸出下列屬性，這些屬性是 WDS 結果檢視器中的預設資料行。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-244">Filters should output at a minimum the following properties which are the default columns in the WDS results view.</span></span>



| <span data-ttu-id="0b4c3-245">GUID</span><span class="sxs-lookup"><span data-stu-id="0b4c3-245">GUID</span></span>                                 | <span data-ttu-id="0b4c3-246">PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="0b4c3-246">PROPSPEC</span></span>      | <span data-ttu-id="0b4c3-247">易記名稱</span><span class="sxs-lookup"><span data-stu-id="0b4c3-247">Friendly Name</span></span>  | <span data-ttu-id="0b4c3-248">Description</span><span class="sxs-lookup"><span data-stu-id="0b4c3-248">Description</span></span>                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4c3-249">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="0b4c3-249">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span> | <span data-ttu-id="0b4c3-250">2</span><span class="sxs-lookup"><span data-stu-id="0b4c3-250">2</span></span>             | <span data-ttu-id="0b4c3-251">PrimaryTitle</span><span class="sxs-lookup"><span data-stu-id="0b4c3-251">PrimaryTitle</span></span>   | <span data-ttu-id="0b4c3-252">針對此專案顯示的標題。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-252">Title that displays for this item.</span></span>                                                                                                              |
| <span data-ttu-id="0b4c3-253">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="0b4c3-253">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span> | <span data-ttu-id="0b4c3-254">4</span><span class="sxs-lookup"><span data-stu-id="0b4c3-254">4</span></span>             | <span data-ttu-id="0b4c3-255">PrimaryAuthors</span><span class="sxs-lookup"><span data-stu-id="0b4c3-255">PrimaryAuthors</span></span> | <span data-ttu-id="0b4c3-256">與此專案最相關聯的人員。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-256">Person most associated with this item.</span></span>                                                                                                          |
| <span data-ttu-id="0b4c3-257">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="0b4c3-257">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="0b4c3-258">PrimaryDate</span><span class="sxs-lookup"><span data-stu-id="0b4c3-258">PrimaryDate</span></span>   | <span data-ttu-id="0b4c3-259">PrimaryDate</span><span class="sxs-lookup"><span data-stu-id="0b4c3-259">PrimaryDate</span></span>    | <span data-ttu-id="0b4c3-260">專案的最重要日期，例如收到的電子郵件或修改檔案的日期。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-260">Most important date for item, like date received for email or modified for files.</span></span>                                                               |
| <span data-ttu-id="0b4c3-261">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="0b4c3-261">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="0b4c3-262">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="0b4c3-262">PerceivedType</span></span> | <span data-ttu-id="0b4c3-263">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="0b4c3-263">PerceivedType</span></span>  | <span data-ttu-id="0b4c3-264">正在剖析的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-264">Type of file being parsed.</span></span> <span data-ttu-id="0b4c3-265">必須符合 WDS [感知類型](-search-2x-wds-perceivedtype.md)中所列的其中一個 Windows 桌面搜尋類型。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-265">Must match one of the Windows Desktop Search types listed in WDS [Perceived Type](-search-2x-wds-perceivedtype.md).</span></span> |



 

<span data-ttu-id="0b4c3-266">若是純文字專案，WDS 會將所有文字和系統定義的屬性（例如檔案大小或副檔名）解壓縮到索引) 的新純文字檔案類型。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-266">For plaintext items, WDS extracts all text and system-defined properties such as file size or extension on including new plaintext file types to the index).</span></span> <span data-ttu-id="0b4c3-267">其他可傳回至索引的屬性類型包括：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-267">Other types of properties that can be returned to the index include:</span></span>

-   <span data-ttu-id="0b4c3-268">針對檔案： author、title、status、關鍵字</span><span class="sxs-lookup"><span data-stu-id="0b4c3-268">For files: author, title, status, keywords</span></span>
-   <span data-ttu-id="0b4c3-269">針對媒體：專輯、內容類型、相機製作、拍攝日期</span><span class="sxs-lookup"><span data-stu-id="0b4c3-269">For media: album, genre, camera make, date taken</span></span>
-   <span data-ttu-id="0b4c3-270">針對通訊：寄件者、收件者、副本、重要性</span><span class="sxs-lookup"><span data-stu-id="0b4c3-270">For communications: from, to, cc, importance</span></span>
-   <span data-ttu-id="0b4c3-271">連絡人：職稱、公司電話、公司</span><span class="sxs-lookup"><span data-stu-id="0b4c3-271">For contacts: job title, business phone, company</span></span>

<span data-ttu-id="0b4c3-272">上述清單會將所指定之感知類型通用的屬性分組;但是，不論類型為何，都可以使用任何屬性。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-272">The list above groups properties common to a specified Perceived Type; however, any property can be used regardless of the type.</span></span> <span data-ttu-id="0b4c3-273">例如，公司可以用來做為連絡人的雇主名稱，也可以用來參考與該檔案相關之用戶端的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-273">For example, company could be used for a contact's employer name and could also be used to refer to the name of a client the file relates to.</span></span> <span data-ttu-id="0b4c3-274">其中許多屬性都是用來在 WDS 結果查看中顯示搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-274">Many of these properties are used to display search results in the WDS results view.</span></span> <span data-ttu-id="0b4c3-275">例如，檔案的 Title 屬性會顯示為預設結果檢視中的主要資料行。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-275">For example, a file's Title property is shown as the main column in the default results view.</span></span> <span data-ttu-id="0b4c3-276">IFilter 物件應該會輸出與所剖析之專案類型相關的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-276">IFilter objects should output all the properties related to the item type they are parsing.</span></span> <span data-ttu-id="0b4c3-277">無法在 WDS 2.x 中新增自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-277">Custom properties cannot be added in WDS 2.x.</span></span> <span data-ttu-id="0b4c3-278">如需可用屬性的完整清單，請參閱 [WDS 架構](-search-2x-wds-schematable.md)。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-278">For a full list of properties available, see the [WDS Schema](-search-2x-wds-schematable.md).</span></span>

## <a name="filter-add-in-installation"></a><span data-ttu-id="0b4c3-279">篩選增益集安裝</span><span class="sxs-lookup"><span data-stu-id="0b4c3-279">Filter Add-in Installation</span></span>

<span data-ttu-id="0b4c3-280">安裝篩選牽涉到將 DLL 複製到 Program Files 目錄中的適當位置並加以註冊。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-280">Installing the filter involves copying the DLL to an appropriate location in the Program Files directory and registering it.</span></span> <span data-ttu-id="0b4c3-281">篩選器應執行自我註冊以進行安裝，且應遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-281">Filters should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="0b4c3-282">安裝程式必須使用 EXE 或 MSI 安裝程式。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-282">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="0b4c3-283">必須提供版本資訊。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-283">Release notes must be provided.</span></span>
-   <span data-ttu-id="0b4c3-284">每個安裝的增益集都必須建立 [ **新增/移除程式** ] 專案。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-284">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="0b4c3-285">安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-285">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="0b4c3-286">如果先前的增益集遭到覆寫，安裝程式應通知使用者。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-286">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="0b4c3-287">如果較新的增益集已覆寫先前的增益集，應該可以還原先前增益集的功能，並將它設為該檔案類型的預設增益集，或重新儲存。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-287">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

### <a name="clsids-required-for-registration"></a><span data-ttu-id="0b4c3-288">註冊所需的 Clsid</span><span class="sxs-lookup"><span data-stu-id="0b4c3-288">CLSIDs Required for Registration</span></span>

<span data-ttu-id="0b4c3-289">每個篩選器都有三個相關聯的類別識別碼或 Clsid。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-289">There are three class identifiers, or CLSIDs, associated with every filter.</span></span> <span data-ttu-id="0b4c3-290">您必須產生一或多個這些 (使用 uuidgen.exe) 註冊篩選增益集。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-290">You'll need to generate one or more of these (use uuidgen.exe) to register your filter add-in.</span></span>

-   <span data-ttu-id="0b4c3-291">第一個會識別所有篩選準則的持續性處理常式 IID \_ IFilter，也就是 {89BCB740-6119-101A-BCB7-00DD010655AF}。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-291">The first identifies all filters' persistent handler, IID\_IFilter, which is {89BCB740-6119-101A-BCB7-00DD010655AF}.</span></span> <span data-ttu-id="0b4c3-292">此 CLSID 對於所有執行 IFilter 的篩選都是常數。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-292">This CLSID is constant for all filters that implement IFilter.</span></span>
-   <span data-ttu-id="0b4c3-293">第二個 (IID \_ IFilter 金鑰的值) 識別檔案類型的 IFilter 執行。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-293">The second (the value of the IID\_IFilter key) identifies the IFilter implementation for your file type.</span></span> <span data-ttu-id="0b4c3-294">此索引鍵包含 InprocServer32 值，指定依路徑和執行緒模型的 DLL 名稱。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-294">This key contains an InprocServer32 value that specifies the DLL name by path and the threading model.</span></span> <span data-ttu-id="0b4c3-295">如果篩選準則位於系統路徑中（例如 system32 目錄），則檔案名即已足夠。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-295">If the filter is in the system path, like the system32 directory, a file name is sufficient.</span></span> <span data-ttu-id="0b4c3-296">否則，此值應該有完整路徑規格。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-296">Otherwise, this value should have a full path specification.</span></span>
-   <span data-ttu-id="0b4c3-297">第三個會識別篩選所處理的檔案類型，並由您的 IPersist 介面上的 GetClassID 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-297">The third identifies the file type the filter processes and is returned by the GetClassID method on your IPersist interface.</span></span>

> [!Note]
>
> <span data-ttu-id="0b4c3-298">在未來的 Microsoft 作業系統版本中，在 system32 目錄中安裝檔案可能會變得更困難，因此建議您將它們安裝在 [Program Files] 底下，並在登錄中包含篩選的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-298">In future versions of Microsoft operating systems, installing files in the system32 directory may get more difficult, so we recommend you install them under Program Files and include a full path to the filter in the registry.</span></span> <span data-ttu-id="0b4c3-299">基於安全性理由，在登錄中指定 DLL 的完整路徑也是很謹慎的。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-299">For security reasons, it is also prudent to specify a full path to your DLL in the registry.</span></span> <span data-ttu-id="0b4c3-300">否則，如果您的版本是在版本之前的進程路徑中，則可以載入 DLL 的「特洛伊木馬程式」版本。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-300">Otherwise, a "Trojan horse" version of your DLL could be loaded if it happens to be in the process path before your version.</span></span>

 

### <a name="registration-model"></a><span data-ttu-id="0b4c3-301">註冊模型</span><span class="sxs-lookup"><span data-stu-id="0b4c3-301">Registration Model</span></span>

<span data-ttu-id="0b4c3-302">當 WDS 可以篩選檔案時，它會在登錄的副檔名下尋找，以決定要載入的篩選。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-302">When WDS is ready to filter a file, it looks in the registry under the file's extension to determine which filter to load.</span></span> <span data-ttu-id="0b4c3-303">接著，它會遵循一系列的登錄連結，以下列順序找出篩選 DLL 的名稱：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-303">It then follows a series of registry links to find the name of the filter DLL, in this order:</span></span>

1.  <span data-ttu-id="0b4c3-304">從位於下列位置的 Clsid：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-304">From CLSIDs located at:</span></span>

    <span data-ttu-id="0b4c3-305">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器覆 \\ 寫 \\ RSApp**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-305">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\RSSearch\\ContentIndexCommon\\Filters\\Override\\RSApp**</span></span>

    <span data-ttu-id="0b4c3-306">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-306">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\RSSearch\\ContentIndexCommon\\Filters**</span></span>

2.  <span data-ttu-id="0b4c3-307">從檔案內容類型：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-307">From the file content type at:</span></span>

    <span data-ttu-id="0b4c3-308">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ MIME \\ 資料庫 \\ 內容類型**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-308">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\MIME\\Database\\Content Type**</span></span>

3.  <span data-ttu-id="0b4c3-309">從副檔名 (與 Win32 LoadIFilter API) 相同：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-309">From the file name extension (same as Win32 LoadIFilter API) at:</span></span>

    <span data-ttu-id="0b4c3-310">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器覆 \\ 寫 \\ RSApp**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-310">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\RSSearch\\ContentIndexCommon\\Filters\\Override\\RSApp**</span></span>

    <span data-ttu-id="0b4c3-311">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-311">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\RSSearch\\ContentIndexCommon\\Filters**</span></span>

    <span data-ttu-id="0b4c3-312">**HKEY \_ 類別 \_ 根 \\ EXTPERSISTENTHANDLER->CLSID->IID \_ IFilter->clsid**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-312">**HKEY\_CLASSES\_ROOT\\extpersistentHandler->CLSID->IID\_IFilter->CLSID**</span></span>

4.  <span data-ttu-id="0b4c3-313">預設位置：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-313">From Default at:</span></span>

    <span data-ttu-id="0b4c3-314">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ 篩選器**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-314">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\RSSearch\\ContentIndexCommon\\Filters**</span></span>

### <a name="to-register-a-filter-add-in"></a><span data-ttu-id="0b4c3-315">註冊篩選增益集</span><span class="sxs-lookup"><span data-stu-id="0b4c3-315">To Register a Filter Add-in</span></span>

<span data-ttu-id="0b4c3-316">您必須在登錄中總共建立八個專案，以註冊您的篩選增益集，其中：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-316">You need to make a total of eight entries in the registry to register your filter add-in, where:</span></span>

-   <span data-ttu-id="0b4c3-317">**ext** 是新的檔案名副檔名</span><span class="sxs-lookup"><span data-stu-id="0b4c3-317">**.ext** is the new file name extension</span></span>
-   <span data-ttu-id="0b4c3-318">**Guid \_ 1** 可以是針對此延伸模組產生的任何新 guid</span><span class="sxs-lookup"><span data-stu-id="0b4c3-318">**GUID\_1** can be any new GUID generated for this extension</span></span>
-   <span data-ttu-id="0b4c3-319">**89BCB740-6119-101A-BCB7-00DD010655AF** 是 IFILTER 介面 GUID，也就是所有 IFilter 執行的常數。</span><span class="sxs-lookup"><span data-stu-id="0b4c3-319">**89BCB740-6119-101A-BCB7-00DD010655AF** is the IFilter interface GUID, which is a constant for all IFilter implementations.</span></span>

1.  <span data-ttu-id="0b4c3-320">使用下列索引鍵和值註冊副檔名的持續性處理常式：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-320">Register the persistent handler for the file name extension with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<.ext>\PersistentHandler
       (Default) = {GUID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}
       (Default) = <Persistent Handler Description>
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered
       (Default) = (Value Not Set)
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered\{89BCB740-6119-101A-BCB7-00DD010655AF}
       (Default) = {CLSID of IFilter implementation}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentHandler
       (Default) = {GUID_1}
    ```

2.  <span data-ttu-id="0b4c3-321">使用下列索引鍵和值註冊 IFilter 執行：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-321">Register the IFilter implementation with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  <span data-ttu-id="0b4c3-322">使用下列機碼和值，向 Windows 桌面搜尋登錄 IFilter 執行：</span><span class="sxs-lookup"><span data-stu-id="0b4c3-322">Register the IFilter implementation with Windows Desktop Search with the following key and value:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a><span data-ttu-id="0b4c3-323">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b4c3-323">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0b4c3-324">**參考**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-324">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b4c3-325">SchemaTable</span><span class="sxs-lookup"><span data-stu-id="0b4c3-325">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> <dt>

[<span data-ttu-id="0b4c3-326">認知類型</span><span class="sxs-lookup"><span data-stu-id="0b4c3-326">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="0b4c3-327">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="0b4c3-327">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="0b4c3-328">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-328">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0b4c3-329">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-329">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 