---
description: Microsoft 提供數個具有 Windows Search 的標準篩選。 用戶端會呼叫這些篩選器處理常式 (這些是 IFilter 介面的執行，) 從檔中解壓縮文字和屬性。
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Windows 隨附的篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112452"
---
# <a name="filter-handlers-that-ship-with-windows"></a><span data-ttu-id="fd4e5-104">Windows 隨附的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-104">Filter Handlers that Ship with Windows</span></span>

<span data-ttu-id="fd4e5-105">Microsoft 提供數個具有 Windows Search 的標準篩選。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-105">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="fd4e5-106">用戶端會呼叫這些篩選器處理常式 (這些是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行，) 從檔中解壓縮文字和屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-106">Clients call these filter handlers (which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) to extract text and properties from a document.</span></span>

<span data-ttu-id="fd4e5-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="fd4e5-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="fd4e5-108">Windows Search 的執行注意事項</span><span class="sxs-lookup"><span data-stu-id="fd4e5-108">Windows Search Implementation Notes</span></span>](#windows-search-implementation-notes)
  - [<span data-ttu-id="fd4e5-109">Windows 7 和10實行</span><span class="sxs-lookup"><span data-stu-id="fd4e5-109">Windows 7 and 10 Implementation</span></span>](#windows-7-and-10-implementation)
  - [<span data-ttu-id="fd4e5-110">Windows Vista 的執行</span><span class="sxs-lookup"><span data-stu-id="fd4e5-110">Windows Vista Implementation</span></span>](#windows-vista-implementation)
  - [<span data-ttu-id="fd4e5-111">舊版的執行</span><span class="sxs-lookup"><span data-stu-id="fd4e5-111">Legacy Implementation</span></span>](#legacy-implementation)
- [<span data-ttu-id="fd4e5-112">Windows Search 篩選</span><span class="sxs-lookup"><span data-stu-id="fd4e5-112">Windows Search Filters</span></span>](#filter-handlers-that-ship-with-windows)
  - [<span data-ttu-id="fd4e5-113">MIME 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-113">MIME Filter Handler</span></span>](#mime-filter-handler)
  - [<span data-ttu-id="fd4e5-114">HTML 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-114">HTML Filter Handler</span></span>](#html-filter-handler)
  - [<span data-ttu-id="fd4e5-115">檔篩選器處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-115">Document Filter Handler</span></span>](#document-filter-handler)
  - [<span data-ttu-id="fd4e5-116">純文字篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-116">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)
  - [<span data-ttu-id="fd4e5-117">Binary 或 Null 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-117">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler)
- [<span data-ttu-id="fd4e5-118">其他資源</span><span class="sxs-lookup"><span data-stu-id="fd4e5-118">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="fd4e5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd4e5-119">Related topics</span></span>](#related-topics)

## <a name="windows-search-implementation-notes"></a><span data-ttu-id="fd4e5-120">Windows Search 的執行注意事項</span><span class="sxs-lookup"><span data-stu-id="fd4e5-120">Windows Search Implementation Notes</span></span>

<span data-ttu-id="fd4e5-121">在 Windows 7 和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-121">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="fd4e5-122">篩選準則必須以機器碼撰寫，因為有多個增益集在中執行的進程可能發生 CLR 版本控制問題。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-122">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="windows-7-and-10-implementation"></a><span data-ttu-id="fd4e5-123">Windows 7 和10實行</span><span class="sxs-lookup"><span data-stu-id="fd4e5-123">Windows 7 and 10 Implementation</span></span>

<span data-ttu-id="fd4e5-124">在 Windows 7 和更新版本中，註冊篩選處理常式、屬性處理常式或新的延伸模組時，會發生新的行為。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-124">In Windows 7 and later, there is new behavior that occurs when registering a filter handler, property handler, or new extension.</span></span> <span data-ttu-id="fd4e5-125">當安裝新的屬性處理常式和（或）篩選器處理常式時，會自動重新編制具有對應副檔名的檔案的索引。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-125">When a new property handler and/or filter handler is installed, files with the corresponding extensions are automatically re-indexed.</span></span>

<span data-ttu-id="fd4e5-126">在 Windows 7 和更新版本中，我們建議您將篩選器處理常式與對應的屬性處理常式一起安裝，並在屬性處理常式之前註冊篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-126">In Windows 7 and later, we recommend that you install a filter handler in conjunction with its corresponding property handlers, and that you register the filter handler before the property handler.</span></span> <span data-ttu-id="fd4e5-127">註冊屬性處理常式時，會立即開始重新編制先前索引檔案的索引，而不需要重新開機，而且會利用任何先前註冊的篩選處理常式來進行內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-127">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a restart, and takes advantage of any previously registered filter handlers for the purpose of content indexing.</span></span>

<span data-ttu-id="fd4e5-128">如果未在沒有對應的屬性處理常式的情況下安裝篩選處理常式，則會在重新開機索引服務或重新開機系統之後，自動重新建立索引。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-128">If only a filter handler is installed without a corresponding property handler, then automatic re-indexing occurs either after a restart of the indexing service, or a restart of the system.</span></span>

<span data-ttu-id="fd4e5-129">如需 Windows 7 特有的屬性描述旗標，請參閱下列參考主題： [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)、 [PROPDESC \_ COLUMNINDEX \_ TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) 和 [PROPDESC \_ SEARCHINFO \_ flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-129">For property description flags specific to Windows 7, see the following reference topics: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC\_COLUMNINDEX\_TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) and [PROPDESC\_SEARCHINFO\_FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span></span>

### <a name="windows-vista-implementation"></a><span data-ttu-id="fd4e5-130">Windows Vista 的執行</span><span class="sxs-lookup"><span data-stu-id="fd4e5-130">Windows Vista Implementation</span></span>

<span data-ttu-id="fd4e5-131">在 Windows Vista 及更早版本中，除非獨立軟體廠商 (ISV) 明確地呼叫相符 Url 的重建或重新編制索引，否則安裝 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 或屬性處理常式並不會起始現有專案的重新編制索引。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-131">In Windows Vista and earlier, installing an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or property handler does not initiate a re-indexing of existing items unless an independent software vendor (ISV) explicitly calls a rebuild or re-indexing of matching URLs.</span></span>

<span data-ttu-id="fd4e5-132">繼承應用程式之間有兩個主要的差異，例如索引服務和較新的應用程式，例如在執行篩選時應注意的 Windows Search：</span><span class="sxs-lookup"><span data-stu-id="fd4e5-132">There are two major differences between legacy applications like Indexing Service and newer applications like Windows Search that you should be aware of when implementing filters:</span></span>

- <span data-ttu-id="fd4e5-133">使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-133">Use of the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface.</span></span>
- <span data-ttu-id="fd4e5-134">使用屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-134">Use of property handlers.</span></span>

<span data-ttu-id="fd4e5-135">首先，Windows Vista 和 Windows Search 3.0 和更新版本會要求您使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) ，原因如下：</span><span class="sxs-lookup"><span data-stu-id="fd4e5-135">First, Windows Vista and Windows Search 3.0 and later require you use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) for the following reasons:</span></span>

- <span data-ttu-id="fd4e5-136">以確保效能和未來的相容性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-136">To ensure performance and future compatibility.</span></span>
- <span data-ttu-id="fd4e5-137">有助於提高安全性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-137">To help increase security.</span></span> <span data-ttu-id="fd4e5-138">使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 來執行的篩選更為安全，因為篩選執行所在的內容不需要在磁片上或透過網路開啟檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-138">Filters implemented with [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) are more secure because the context in which the filter runs does not need the rights to open files on the disk or over the network.</span></span>

<span data-ttu-id="fd4e5-139">雖然 Windows Search 只使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)，您也可以在篩選中包含 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和/或 [IPersistStorage 介面](/windows/win32/api/objidl/nn-objidl-ipersiststorage) ，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-139">While Windows Search uses only [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), you can also include [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and/or [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) implementations in your filters for backward compatibility.</span></span>

<span data-ttu-id="fd4e5-140">第二個主要差異是 Windows Vista 和 Windows Search 3.0 和更新版本都有新的 [屬性系統](../properties/building-property-handlers.md) ，使用屬性處理常式來列舉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-140">The second major difference is that Windows Vista and Windows Search 3.0 and later have a new [Property System](../properties/building-property-handlers.md) that uses property handlers to enumerate properties of items.</span></span>

<span data-ttu-id="fd4e5-141">不過，有時候您需要執行可處理內容和屬性的篩選準則，以便：</span><span class="sxs-lookup"><span data-stu-id="fd4e5-141">However, there are times when you need to implement a filter that handles both content and properties in order to:</span></span>

- <span data-ttu-id="fd4e5-142">支援舊版 MSSearch 實作為。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-142">Support legacy MSSearch implementations.</span></span>
- <span data-ttu-id="fd4e5-143">跨越連結。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-143">Traverse links.</span></span>
- <span data-ttu-id="fd4e5-144">保留語言資訊。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-144">Preserve language information.</span></span>
- <span data-ttu-id="fd4e5-145">以遞迴方式篩選內嵌的專案。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-145">Recursively filter embedded items.</span></span>

<span data-ttu-id="fd4e5-146">在這些情況下，您需要完整的篩選器執行，包括用來存取屬性值的 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 方法。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-146">In these situations, you need a full filter implementation, including the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method to access property values.</span></span>

### <a name="legacy-implementation"></a><span data-ttu-id="fd4e5-147">舊版的執行</span><span class="sxs-lookup"><span data-stu-id="fd4e5-147">Legacy Implementation</span></span>

<span data-ttu-id="fd4e5-148">如先前所述，Windows Vista 和 Windows Search 包含新的屬性系統，其會封裝與專案內容不同的專案屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-148">As noted earlier, Windows Vista and Windows Search include a new property system that encapsulates an item's properties that is separate from an item's content.</span></span> <span data-ttu-id="fd4e5-149">這個屬性系統不存在於舊版的 Microsoft Windows 桌面搜尋 (WDS) 2.x。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-149">This property system does not exist in earlier versions of Microsoft Windows Desktop Search (WDS) 2.x.</span></span> <span data-ttu-id="fd4e5-150">如果您的篩選準則必須支援其他應用程式（如上所述），則可能需要處理內容和屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-150">If your filter must support other applications as described above, it may need to handle both content and properties.</span></span>

<span data-ttu-id="fd4e5-151">如需有關開發相容的篩選器的詳細資訊，請參閱下列主題、 [適用于繼承應用程式的 IFilter () ](/windows/win32/api/filter/nn-filter-ifilter)，以及 [針對繼承應用程式) 開發篩選增益集 (](../lwef/-search-2x-wds-ifilteraddins.md)。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-151">For more information on developing a compatible filter, see the following topics, [IFilter (for legacy applications)](/windows/win32/api/filter/nn-filter-ifilter), and [Developing Filter Add-ins (for legacy applications)](../lwef/-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="windows-search-filters"></a><span data-ttu-id="fd4e5-152">Windows Search 篩選</span><span class="sxs-lookup"><span data-stu-id="fd4e5-152">Windows Search Filters</span></span>

<span data-ttu-id="fd4e5-153">Microsoft 提供數個具有 Windows Search 的標準篩選。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-153">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="fd4e5-154">下表摘要說明 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL 內容。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-154">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL contents are summarized in the following table.</span></span> <span data-ttu-id="fd4e5-155">按一下篩選器處理常式的名稱，會帶您前往該 **IFilter** 執行的描述。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-155">Clicking the name of a filter handler takes you to the description for that **IFilter** implementation.</span></span>

| <span data-ttu-id="fd4e5-156">篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-156">Filter handler</span></span>                                                  | <span data-ttu-id="fd4e5-157">篩選的檔案</span><span class="sxs-lookup"><span data-stu-id="fd4e5-157">Files filtered</span></span>                              | <span data-ttu-id="fd4e5-158">IFilter DLL</span><span class="sxs-lookup"><span data-stu-id="fd4e5-158">IFilter DLL</span></span>  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [<span data-ttu-id="fd4e5-159">MIME 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-159">MIME Filter Handler</span></span>](#mime-filter-handler)                     | <span data-ttu-id="fd4e5-160">多用途網際網路郵件延伸 (MIME) </span><span class="sxs-lookup"><span data-stu-id="fd4e5-160">Multipurpose Internet Mail Extension (MIME)</span></span> | <span data-ttu-id="fd4e5-161">mimefilt.dll</span><span class="sxs-lookup"><span data-stu-id="fd4e5-161">mimefilt.dll</span></span> |
| [<span data-ttu-id="fd4e5-162">HTML 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-162">HTML Filter Handler</span></span>](#html-filter-handler)                     | <span data-ttu-id="fd4e5-163">HTML 3.0 或更早版本</span><span class="sxs-lookup"><span data-stu-id="fd4e5-163">HTML 3.0 or earlier</span></span>                         | <span data-ttu-id="fd4e5-164">nlhtml.dll</span><span class="sxs-lookup"><span data-stu-id="fd4e5-164">nlhtml.dll</span></span>   |
| [<span data-ttu-id="fd4e5-165">檔篩選器處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-165">Document Filter Handler</span></span>](#document-filter-handler)             | <span data-ttu-id="fd4e5-166">Microsoft Word、Excel、PowerPoint</span><span class="sxs-lookup"><span data-stu-id="fd4e5-166">Microsoft Word, Excel, PowerPoint</span></span>           | <span data-ttu-id="fd4e5-167">offfilt.dll</span><span class="sxs-lookup"><span data-stu-id="fd4e5-167">offfilt.dll</span></span>  |
| [<span data-ttu-id="fd4e5-168">純文字篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-168">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)         | <span data-ttu-id="fd4e5-169">純文字檔-預設 IFilter</span><span class="sxs-lookup"><span data-stu-id="fd4e5-169">Plain text files - Default IFilter</span></span>          | <span data-ttu-id="fd4e5-170">query.dll</span><span class="sxs-lookup"><span data-stu-id="fd4e5-170">query.dll</span></span>    |
| [<span data-ttu-id="fd4e5-171">Binary 或 Null 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-171">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler) | <span data-ttu-id="fd4e5-172">二進位檔案-Null IFilter</span><span class="sxs-lookup"><span data-stu-id="fd4e5-172">Binary files - Null IFilter</span></span>                 | <span data-ttu-id="fd4e5-173">query.dll</span><span class="sxs-lookup"><span data-stu-id="fd4e5-173">query.dll</span></span>    |

### <a name="mime-filter-handler"></a><span data-ttu-id="fd4e5-174">MIME 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-174">MIME Filter Handler</span></span>

<span data-ttu-id="fd4e5-175">mimefilt.dll 中的 MIME 篩選處理常式 () 會從副檔名為 .eml、.mht 和 mhtml 的檔案中解壓縮文字和屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-175">The MIME filter handler (in mimefilt.dll) extracts text and property information from files with the extensions .eml, .mht and .mhtml.</span></span>

### <a name="html-filter-handler"></a><span data-ttu-id="fd4e5-176">HTML 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-176">HTML Filter Handler</span></span>

<span data-ttu-id="fd4e5-177">) nlhtml.dll 中的 HTML 篩選處理常式 (會從 "htmlfiles" 類別中解壓縮文字和屬性資訊，以便 Windows Search 進行編制索引。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-177">The HTML filter handler (in nlhtml.dll) extracts text and property information from the class "htmlfiles" so that it can be indexed by Windows Search.</span></span> <span data-ttu-id="fd4e5-178">如需 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 與檔案類型之間關聯的描述，請參閱 [註冊篩選處理常式](-search-ifilter-registering-filters.md)中的「尋找檔案的 IFilter DLL」。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-178">For a description of the association between [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and file type, see "Finding the IFilter DLL for a File" in [Registering Filter Handlers](-search-ifilter-registering-filters.md).</span></span>

<span data-ttu-id="fd4e5-179">您可以使用 `META` html 檔的標記功能，將特殊處理要求傳送至 Html [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-179">You can use the `META` tag feature of HTML documents to convey special handling requests to the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter).</span></span> <span data-ttu-id="fd4e5-180">`META` 標記會出現在標記內 html 檔案的開頭附近 `HEAD ... /HEAD` ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-180">`META` tags occur near the beginning of an html file within the `HEAD ... /HEAD` tags, as illustrated in the following example.</span></span>

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

<span data-ttu-id="fd4e5-181">某些 HTML `META` 標記會自動對應到知名的屬性集和屬性識別碼 (屬性識別碼 (PID) ) 值，以便這些屬性的查詢將會搜尋對應的內容。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-181">Some HTML `META` tags are automatically mapped to well known property set and property ID (property identifier (PID)) values so that queries on these properties will search the mapped contents.</span></span> <span data-ttu-id="fd4e5-182">下表列出一些範例。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-182">Some examples are listed in the following table.</span></span> <span data-ttu-id="fd4e5-183">如需可用於檔案格式的系統屬性清單，請參閱 [自訂檔案格式的系統定義屬性](-shell-systemdefinedpropertiesforfileformats.md)。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-183">For a list of system properties that you can use for your file formats, see [System-Defined Properties for Custom File Formats](-shell-systemdefinedpropertiesforfileformats.md).</span></span>

| <span data-ttu-id="fd4e5-184">屬性範例</span><span class="sxs-lookup"><span data-stu-id="fd4e5-184">Property example</span></span>                              | <span data-ttu-id="fd4e5-185">對應至</span><span class="sxs-lookup"><span data-stu-id="fd4e5-185">Mapped to</span></span>                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fd4e5-186">meta name = "author" content = "ruth"</span><span class="sxs-lookup"><span data-stu-id="fd4e5-186">meta name="author" content="ruth"</span></span>             | <span data-ttu-id="fd4e5-187">摘要資訊屬性集中的 author 屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-187">The author property in the Summary Information property set.</span></span>            |
| <span data-ttu-id="fd4e5-188">meta name = "subject" content = "word 處理"</span><span class="sxs-lookup"><span data-stu-id="fd4e5-188">meta name="subject" content="word processing"</span></span> | <span data-ttu-id="fd4e5-189">摘要資訊屬性集中的 subject 屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-189">The subject property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="fd4e5-190">meta name = "關鍵字" content = "字型，serif"</span><span class="sxs-lookup"><span data-stu-id="fd4e5-190">meta name="keywords" content="fonts, serif"</span></span>   | <span data-ttu-id="fd4e5-191">摘要資訊屬性集中的關鍵字屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-191">The keyword property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="fd4e5-192">meta name = "ms. category" content = "小說"</span><span class="sxs-lookup"><span data-stu-id="fd4e5-192">meta name="ms.category" content="fiction"</span></span>     | <span data-ttu-id="fd4e5-193">檔摘要資訊屬性集中的 category 屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-193">The category property in the document Summary Information property set.</span></span> |

<span data-ttu-id="fd4e5-194">下表列出 HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 的部分功能。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-194">Some features of the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) are listed in the following table.</span></span>

[comment]: # (這個資料表必須是 HTML，才能正確地將範例格式化)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd4e5-196">Task</span><span class="sxs-lookup"><span data-stu-id="fd4e5-196">Task</span></span></th>
<th><span data-ttu-id="fd4e5-197">動作</span><span class="sxs-lookup"><span data-stu-id="fd4e5-197">Action</span></span></th>
<th><span data-ttu-id="fd4e5-198">範例</span><span class="sxs-lookup"><span data-stu-id="fd4e5-198">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd4e5-199">從檔案建立特殊的摘要</span><span class="sxs-lookup"><span data-stu-id="fd4e5-199">Creating special abstracts from files</span></span></td>
<td><span data-ttu-id="fd4e5-200">您 <code>META NAME=&quot;DESCRIPTION&quot;...</code> 可以使用標記來指示 <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> 在檔摘要中使用後面接著關鍵字的字串 <code>CONTENT</code> 。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-200">Use the <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag to instruct the <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> to use the string following the <code>CONTENT</code> keyword as the document abstract.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fd4e5-201">篩選程式可以針對每個篩選過的檔案產生摘要，這會預設為檔開頭的一組字元。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-201">The filtering process can generate abstracts for each filtered file, which default to being a set of characters at the beginning of the file.</span></span>
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd4e5-202">防止篩選個別檔案</span><span class="sxs-lookup"><span data-stu-id="fd4e5-202">Preventing individual files from being filtered</span></span></td>
<td><span data-ttu-id="fd4e5-203">將 <code>meta name</code> 標記新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-203">Add a <code>meta name</code> tag to the file.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd4e5-204">設定檔案 (的語言代碼，以確保系統選擇正確的語言斷詞工具和非搜尋字檔案) </span><span class="sxs-lookup"><span data-stu-id="fd4e5-204">Setting the language code for a file (to ensure the system chooses the correct language word breakers and noise word files)</span></span></td>
<td><span data-ttu-id="fd4e5-205">在檔案中新增下列 <code>meta name</code> 標記，其中 content 欄位會以字元或使用地區設定值) 來指定適當的語言代碼 (。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-205">Add the following <code>meta name</code> tag to the file, where the content field specifies the appropriate language code (either in characters or by using the locale value).</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a><span data-ttu-id="fd4e5-206">檔篩選器處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-206">Document Filter Handler</span></span>

<span data-ttu-id="fd4e5-207">檔篩選器處理常式 (在 offilt.dll) 會篩選 Microsoft Office 中某些檔副檔名的檔案。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-207">The Document filter handler (in offilt.dll) filters files for some extensions of documents in Microsoft Office.</span></span> <span data-ttu-id="fd4e5-208">例如，這些檔案包含副檔名為 .doc、.mdb、.ppt 和 .xlt 的檔案。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-208">These include files with the extensions .doc, .mdb, .ppt, and .xlt, for example.</span></span>

### <a name="plain-text-filter-handler"></a><span data-ttu-id="fd4e5-209">純文字篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-209">Plain Text Filter Handler</span></span>

<span data-ttu-id="fd4e5-210">若為純文字檔，Windows Search 會使用文字篩選處理常式，此處理程式會篩選系統屬性 (例如檔案名) 以及檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-210">For plain-text files, Windows Search uses the text filter handler, which filters both the system properties (such as file names) and the contents of a file.</span></span> <span data-ttu-id="fd4e5-211">當檔案類型在登錄中沒有 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 關聯時，Windows Search 只會為檔案的 Shell 屬性編制索引。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-211">When a file type does not have an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) association in the registry, Windows Search indexes only the Shell properties for the file.</span></span> <span data-ttu-id="fd4e5-212">不過，使用者可以使用 [**編制索引選項**] 控制台中的 [ **Advanced] 選項** 來 **編制屬性的索引**，或 **索引屬性和檔案內容**。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-212">However the user can use the **Advanced Options** in the **Indexing Options** control panel to **Index Properties** or **Index Properties and File Contents**.</span></span>

![顯示 [advanced options （選項）] 對話方塊的螢幕擷取畫面](images/ifilteradvancedoptions.png)

<span data-ttu-id="fd4e5-214">如果使用者為沒有相關聯的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)的檔案類型選擇此選項，則會使用文字篩選處理常式來解壓縮檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-214">If the user chooses this option for a file type without an associated [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), the text filter handler is used to extract the content of the file.</span></span> <span data-ttu-id="fd4e5-215">文字篩選處理常式不會「瞭解」任何檔案格式;篩選檔案的內容時，會將檔案視為字元序列。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-215">The text filter handler does not "understand" any document format; when filtering the contents of a file, it treats the file as a sequence of characters.</span></span> <span data-ttu-id="fd4e5-216">它會檢查檔開頭的 Unicode 位元組順序標記。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-216">It does check for the Unicode byte-order mark at the beginning of the file.</span></span>

### <a name="binary-or-null-filter-handler"></a><span data-ttu-id="fd4e5-217">Binary 或 Null 篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-217">Binary or Null Filter Handler</span></span>

<span data-ttu-id="fd4e5-218">當遇到已註冊的二進位檔案時，會使用 null 篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-218">When a registered binary file is encountered, the null filter handler is used.</span></span> <span data-ttu-id="fd4e5-219">Null 篩選處理常式只會捕獲系統屬性。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-219">The null filter handler retrieves only the system properties.</span></span> <span data-ttu-id="fd4e5-220">二進位檔案的內容不會進行篩選。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-220">The contents of a binary file are not filtered.</span></span> <span data-ttu-id="fd4e5-221">系統屬性的範例包括 **檔案名**、 **LastWriteTime**、 **FileSize** 和 **屬性**。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-221">Examples of system properties are **FileName**, **LastWriteTime**, **FileSize**, and **Attributes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd4e5-222">其他資源</span><span class="sxs-lookup"><span data-stu-id="fd4e5-222">Additional Resources</span></span>

- <span data-ttu-id="fd4e5-223">[GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-223">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="fd4e5-224">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-224">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="fd4e5-225">如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-225">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="fd4e5-226">若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fd4e5-226">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd4e5-227">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd4e5-227">Related topics</span></span>

[<span data-ttu-id="fd4e5-228">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-228">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="fd4e5-229">關於 Windows Search 中的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-229">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="fd4e5-230">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="fd4e5-230">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="fd4e5-231">從篩選處理常式傳回屬性</span><span class="sxs-lookup"><span data-stu-id="fd4e5-231">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="fd4e5-232">在 Windows Search 中執行篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-232">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="fd4e5-233">註冊篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-233">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="fd4e5-234">測試篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="fd4e5-234">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
