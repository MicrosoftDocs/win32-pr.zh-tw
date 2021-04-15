---
description: 篩選處理常式是 IFilter 介面的執行，可掃描檔中的文字和屬性。
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: 瞭解 Windows Search 中的篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49cc1d3e479ae03645665618c60a33bdcfe19ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511102"
---
# <a name="understanding-filter-handlers-in-windows-search"></a><span data-ttu-id="a974a-103">瞭解 Windows Search 中的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="a974a-103">Understanding Filter Handlers in Windows Search</span></span>

<span data-ttu-id="a974a-104">篩選處理常式是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行，可掃描檔中的文字和屬性。</span><span class="sxs-lookup"><span data-stu-id="a974a-104">Filter handlers, which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, scan documents for text and properties.</span></span> <span data-ttu-id="a974a-105">篩選處理常式會將這些專案中的文字區塊解壓縮，並篩選出內嵌的格式，並保留文字位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a974a-105">Filter handlers extract chunks of text from these items, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="a974a-106">它們也會解壓縮值的區塊，也就是檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="a974a-106">They also extract chunks of values, which are document properties.</span></span> <span data-ttu-id="a974a-107">**IFilter** 是建立高階應用程式的基礎，例如檔索引子和與應用程式無關的檢視器。</span><span class="sxs-lookup"><span data-stu-id="a974a-107">**IFilter** is the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span>

<span data-ttu-id="a974a-108">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="a974a-108">This topic is organized as follows:</span></span>

- [<span data-ttu-id="a974a-109">關於 IFilter 介面</span><span class="sxs-lookup"><span data-stu-id="a974a-109">About the IFilter Interface</span></span>](#about-the-ifilter-interface)
  - [<span data-ttu-id="a974a-110">隔離流程</span><span class="sxs-lookup"><span data-stu-id="a974a-110">Isolation Process</span></span>](#isolation-process)
  - [<span data-ttu-id="a974a-111">IFilter Dll</span><span class="sxs-lookup"><span data-stu-id="a974a-111">IFilter DLLs</span></span>](#ifilter-dlls)
  - [<span data-ttu-id="a974a-112">IFilter 結構</span><span class="sxs-lookup"><span data-stu-id="a974a-112">IFilter Structure</span></span>](#ifilter-structure)
  - [<span data-ttu-id="a974a-113">機器碼</span><span class="sxs-lookup"><span data-stu-id="a974a-113">Native Code</span></span>](#native-code)
- [<span data-ttu-id="a974a-114">尋找 IFilter 類別識別碼</span><span class="sxs-lookup"><span data-stu-id="a974a-114">Finding the IFilter Class Identifier</span></span>](#finding-the-ifilter-class-identifier)
  - [<span data-ttu-id="a974a-115">IFilter：： GetChunk 和地區設定碼識別碼</span><span class="sxs-lookup"><span data-stu-id="a974a-115">IFilter::GetChunk and Locale Code Identifiers</span></span>](#ifiltergetchunk-and-locale-code-identifiers)
- [<span data-ttu-id="a974a-116">其他資源</span><span class="sxs-lookup"><span data-stu-id="a974a-116">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="a974a-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a974a-117">Related topics</span></span>](#related-topics)

## <a name="about-the-ifilter-interface"></a><span data-ttu-id="a974a-118">關於 IFilter 介面</span><span class="sxs-lookup"><span data-stu-id="a974a-118">About the IFilter Interface</span></span>

<span data-ttu-id="a974a-119">Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="a974a-119">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="a974a-120">您可以藉由撰寫篩選器來解壓縮內容，並使用屬性處理常式來解壓縮檔案的屬性，藉此擴充 Windows Search 來編制新的或專屬檔案類型的索引。</span><span class="sxs-lookup"><span data-stu-id="a974a-120">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="a974a-121">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的設計目的是為了符合全文搜尋引擎的特定需求。</span><span class="sxs-lookup"><span data-stu-id="a974a-121">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is designed to meet the specific needs of full-text search engines.</span></span> <span data-ttu-id="a974a-122">像 Windows Search 的全文搜尋引擎會呼叫 **IFilter** 方法，以將文字和屬性資訊解壓縮，並將其新增至索引。</span><span class="sxs-lookup"><span data-stu-id="a974a-122">Full-text search engines like Windows Search call the **IFilter** methods to extract text and property information and add them to an index.</span></span> <span data-ttu-id="a974a-123">Windows Search 將傳回的 [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 方法的結果分成單字，將其正規化，並將它們儲存在索引中。</span><span class="sxs-lookup"><span data-stu-id="a974a-123">Windows Search breaks the results of the returned [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) method into words, normalizes them, and saves them in an index.</span></span> <span data-ttu-id="a974a-124">如果有的話，搜尋引擎會使用文字區塊 (LCID) 的語言代碼識別碼，來執行特定語言的斷詞和正規化。</span><span class="sxs-lookup"><span data-stu-id="a974a-124">If available, the search engine uses the language code identifier (LCID) of a text chunk to perform language-specific word breaking and normalization.</span></span>

<span data-ttu-id="a974a-125">Windows Search 使用下表所述的三個函式，來存取已註冊的篩選處理常式 ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面) 的實作為。</span><span class="sxs-lookup"><span data-stu-id="a974a-125">Windows Search uses three functions, described in the following table, to access registered filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span> <span data-ttu-id="a974a-126">這些函數在載入和系結至内嵌物件的篩選處理常式時特別有用。</span><span class="sxs-lookup"><span data-stu-id="a974a-126">These functions are especially useful when loading and binding to an embedded object's filter handler.</span></span>

| <span data-ttu-id="a974a-127">函式</span><span class="sxs-lookup"><span data-stu-id="a974a-127">Function</span></span>               | <span data-ttu-id="a974a-128">描述</span><span class="sxs-lookup"><span data-stu-id="a974a-128">Description</span></span>                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a974a-129">LoadIFilter</span><span class="sxs-lookup"><span data-stu-id="a974a-129">LoadIFilter</span></span>            | <span data-ttu-id="a974a-130">取得最適合指定之內容類型的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 指標。</span><span class="sxs-lookup"><span data-stu-id="a974a-130">Gets a pointer to the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) that is most suitable for the specified content type.</span></span>                                                                                            |
| <span data-ttu-id="a974a-131">BindIFilterFromStorage</span><span class="sxs-lookup"><span data-stu-id="a974a-131">BindIFilterFromStorage</span></span> | <span data-ttu-id="a974a-132">取得 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 的指標，最適合 [IStorage 介面](/windows/win32/api/objidl/nn-objidl-istorage) 物件中所含的內容。</span><span class="sxs-lookup"><span data-stu-id="a974a-132">Gets a pointer to the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) that is most suitable for the content contained in an [IStorage Interface](/windows/win32/api/objidl/nn-objidl-istorage) object.</span></span> |
| <span data-ttu-id="a974a-133">BindIFilterFromStream</span><span class="sxs-lookup"><span data-stu-id="a974a-133">BindIFilterFromStream</span></span>  | <span data-ttu-id="a974a-134">取得最適合指定類別識別碼的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 指標， (CLSID) 從資料流程變數抓取。</span><span class="sxs-lookup"><span data-stu-id="a974a-134">Gets a pointer to the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) that is most suitable for a specified class identifier (CLSID) retrieved from a stream variable.</span></span>                                                 |

<span data-ttu-id="a974a-135">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面有五個方法，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="a974a-135">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface has five methods, described in the following table.</span></span>

| <span data-ttu-id="a974a-136">方法</span><span class="sxs-lookup"><span data-stu-id="a974a-136">Method</span></span>                                                    | <span data-ttu-id="a974a-137">描述</span><span class="sxs-lookup"><span data-stu-id="a974a-137">Description</span></span>                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a974a-138">**IFilter：： Init**</span><span class="sxs-lookup"><span data-stu-id="a974a-138">**IFilter::Init**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-init)          | <span data-ttu-id="a974a-139">初始化篩選會話。</span><span class="sxs-lookup"><span data-stu-id="a974a-139">Initializes a filtering session.</span></span>                                                                                   |
| [<span data-ttu-id="a974a-140">**IFilter：： GetChunk**</span><span class="sxs-lookup"><span data-stu-id="a974a-140">**IFilter::GetChunk**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | <span data-ttu-id="a974a-141">在第一個或下一個區塊的開頭放置 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ，並傳回描述項。</span><span class="sxs-lookup"><span data-stu-id="a974a-141">Positions [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) at the beginning of the first or next chunk and returns a descriptor.</span></span> |
| [<span data-ttu-id="a974a-142">**IFilter：： GetText**</span><span class="sxs-lookup"><span data-stu-id="a974a-142">**IFilter::GetText**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | <span data-ttu-id="a974a-143">抓取目前區塊中的文字。</span><span class="sxs-lookup"><span data-stu-id="a974a-143">Retrieves text from the current chunk.</span></span>                                                                             |
| [<span data-ttu-id="a974a-144">**IFilter：： GetValue**</span><span class="sxs-lookup"><span data-stu-id="a974a-144">**IFilter::GetValue**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | <span data-ttu-id="a974a-145">從目前的區塊抓取值。</span><span class="sxs-lookup"><span data-stu-id="a974a-145">Retrieves values from the current chunk.</span></span>                                                                           |
| [<span data-ttu-id="a974a-146">**IFilter：： BindRegion**</span><span class="sxs-lookup"><span data-stu-id="a974a-146">**IFilter::BindRegion**</span></span>](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | <span data-ttu-id="a974a-147">抓取代表物件之指定部分的介面。</span><span class="sxs-lookup"><span data-stu-id="a974a-147">Retrieves an interface representing the specified portion of object.</span></span> <span data-ttu-id="a974a-148">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="a974a-148">Reserved for future use.</span></span>                      |

### <a name="isolation-process"></a><span data-ttu-id="a974a-149">隔離流程</span><span class="sxs-lookup"><span data-stu-id="a974a-149">Isolation Process</span></span>

<span data-ttu-id="a974a-150">Windows Search 在具有限制許可權的本機系統安全性內容中執行 Ifilter。</span><span class="sxs-lookup"><span data-stu-id="a974a-150">Windows Search runs IFilters in the Local System security context with restricted rights.</span></span> <span data-ttu-id="a974a-151">在此 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 主機隔離流程中，會移除一些許可權：</span><span class="sxs-lookup"><span data-stu-id="a974a-151">In this [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) host isolation process, a number of rights are removed:</span></span>

- <span data-ttu-id="a974a-152">限制的程式碼</span><span class="sxs-lookup"><span data-stu-id="a974a-152">Restricted Code</span></span>
- <span data-ttu-id="a974a-153">所有人</span><span class="sxs-lookup"><span data-stu-id="a974a-153">Everyone</span></span>
- <span data-ttu-id="a974a-154">本機</span><span class="sxs-lookup"><span data-stu-id="a974a-154">Local</span></span>
- <span data-ttu-id="a974a-155">互動式</span><span class="sxs-lookup"><span data-stu-id="a974a-155">Interactive</span></span>
- <span data-ttu-id="a974a-156">驗證的使用者</span><span class="sxs-lookup"><span data-stu-id="a974a-156">Authenticated Users</span></span>
- <span data-ttu-id="a974a-157">內建使用者</span><span class="sxs-lookup"><span data-stu-id="a974a-157">Built-in Users</span></span>
- <span data-ttu-id="a974a-158">使用者的安全識別碼 (SID) </span><span class="sxs-lookup"><span data-stu-id="a974a-158">Users' security identifier (SID)</span></span>

<span data-ttu-id="a974a-159">移除這些許可權表示 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面沒有磁片系統或網路或任何使用者介面或剪貼簿功能的存取權。</span><span class="sxs-lookup"><span data-stu-id="a974a-159">The removal of these rights means the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface does not have access to the disk system or network or to any user interface or clipboard functions.</span></span> <span data-ttu-id="a974a-160">此外，隔離進程會在防止建立子進程的工作物件下執行，並在工作集上強加 100 MB 的限制。</span><span class="sxs-lookup"><span data-stu-id="a974a-160">Furthermore, the isolation process runs under a job object that prevents child processes from being created and imposes a 100 MB limit on the working set.</span></span> <span data-ttu-id="a974a-161">**IFilter** 介面主機隔離進程會提高編制索引平臺的穩定性，因為可能會不正確地執行協力廠商篩選。</span><span class="sxs-lookup"><span data-stu-id="a974a-161">the **IFilter** interface host isolation process increases the stability of the indexing platform, due to the possibility of incorrectly implemented third-party filters.</span></span>

> [!NOTE]  
> <span data-ttu-id="a974a-162">您必須撰寫篩選處理常式來管理緩衝區，並正確地堆疊。</span><span class="sxs-lookup"><span data-stu-id="a974a-162">Filter handlers must be written to manage buffers, and stack correctly.</span></span> <span data-ttu-id="a974a-163">所有字串複本都必須有明確的檢查，以防止緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="a974a-163">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="a974a-164">您應該一律確認已配置的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="a974a-164">You should always verify the allocated size of the buffer.</span></span> <span data-ttu-id="a974a-165">您應該一律依據緩衝區大小來測試資料的大小。</span><span class="sxs-lookup"><span data-stu-id="a974a-165">You should always test the size of the data against the size of the buffer.</span></span>

### <a name="ifilter-dlls"></a><span data-ttu-id="a974a-166">IFilter Dll</span><span class="sxs-lookup"><span data-stu-id="a974a-166">IFilter DLLs</span></span>

<span data-ttu-id="a974a-167">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) Dll 會執行 **IFilter** 介面，讓用戶端可以從檔案類型、類別或察覺的型別中解壓縮文字和屬性值資訊。</span><span class="sxs-lookup"><span data-stu-id="a974a-167">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLLs implement the **IFilter** interface to enable a client to extract text and property value information from a file type, class, or perceived type.</span></span> <span data-ttu-id="a974a-168">Windows Search 篩選進程 **SearchFilterHost.exe** 系結至為專案註冊之類別、感知類型或副檔名的 **IFilter** 。</span><span class="sxs-lookup"><span data-stu-id="a974a-168">The Windows Search filtering process **SearchFilterHost.exe** binds to the **IFilter** that is registered for the class, perceived type, or name extension of the item.</span></span>

### <a name="ifilter-structure"></a><span data-ttu-id="a974a-169">IFilter 結構</span><span class="sxs-lookup"><span data-stu-id="a974a-169">IFilter Structure</span></span>

<span data-ttu-id="a974a-170">每個 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 都是一個 DLL 檔案，它會 (COM) server 來提供指定的篩選功能，以執行同進程元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="a974a-170">Each [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is a DLL file that implements an in-process Component Object Model (COM) server to supply the specified filtering capabilities.</span></span> <span data-ttu-id="a974a-171">下圖說明典型的 **IFilter** dll 的整體結構。</span><span class="sxs-lookup"><span data-stu-id="a974a-171">The following figure illustrates shows the overall structure of a typical **IFilter** DLLs.</span></span> <span data-ttu-id="a974a-172">更複雜的範例可能會執行一個以上的 **IFilter** 類別。</span><span class="sxs-lookup"><span data-stu-id="a974a-172">A more complex example could implement more than one **IFilter** class.</span></span>

![一般 ifilter dll 結構的圖表](images/ifilter-structure.png)

### <a name="native-code"></a><span data-ttu-id="a974a-174">機器碼</span><span class="sxs-lookup"><span data-stu-id="a974a-174">Native Code</span></span>

<span data-ttu-id="a974a-175">您必須以機器碼撰寫篩選器，因為可能的 common language runtime (CLR) 在中執行多個增益集的進程的版本控制問題。</span><span class="sxs-lookup"><span data-stu-id="a974a-175">Filters must be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span> <span data-ttu-id="a974a-176">在 Windows 7 （含）以後版本和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選。</span><span class="sxs-lookup"><span data-stu-id="a974a-176">In Windows 7 and later and later, filters written in managed code are explicitly blocked.</span></span>

## <a name="finding-the-ifilter-class-identifier"></a><span data-ttu-id="a974a-177">尋找 IFilter 類別識別碼</span><span class="sxs-lookup"><span data-stu-id="a974a-177">Finding the IFilter Class Identifier</span></span>

<span data-ttu-id="a974a-178">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL 的類別會在 PersistentHandler 登錄機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="a974a-178">The class of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL is registered under the PersistentHandler registry key.</span></span> <span data-ttu-id="a974a-179">下列 HTML 檔案範例將說明如何尋找 HTML 檔案的 **IFilter** DLL。</span><span class="sxs-lookup"><span data-stu-id="a974a-179">The following example, for HTML files, illustrates how to find the **IFilter** DLL for an HTML document.</span></span> <span data-ttu-id="a974a-180">這個範例會遵循類似于系統用來尋找與專案相關聯之 **IFilter** 的邏輯。</span><span class="sxs-lookup"><span data-stu-id="a974a-180">This example follows logic similar to that used by the system to find the **IFilter** associated with an item.</span></span>

1. <span data-ttu-id="a974a-181">檢查 DLL 所篩選之檔案類型的副檔名是否有在登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別下註冊的 PersistentHandler。</span><span class="sxs-lookup"><span data-stu-id="a974a-181">Check whether the extension for the type of files that the DLL filters has a PersistentHandler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="a974a-182">讓此機碼成為 `Value1` 。</span><span class="sxs-lookup"><span data-stu-id="a974a-182">Let this key be `Value1`.</span></span> <span data-ttu-id="a974a-183">如果該專案已經存在，請跳到此程式的步驟4，並 `Value1` 在該機碼中使用。</span><span class="sxs-lookup"><span data-stu-id="a974a-183">If that entry already exists, then skip to step 4 of this procedure and use `Value1` in that key.</span></span> <span data-ttu-id="a974a-184">值的類型是 REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="a974a-184">The values are of type REG\_SZ.</span></span>

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. <span data-ttu-id="a974a-185">或者，如果沒有針對延伸模組註冊的 PersistentHandler，請在 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別的登錄專案底下，尋找與檔案類型相關聯的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="a974a-185">Alternatively, if there is not a PersistentHandler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="a974a-186">讓此機碼成為 `Value2` 。</span><span class="sxs-lookup"><span data-stu-id="a974a-186">Let this key be `Value2`.</span></span>

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. <span data-ttu-id="a974a-187">判斷是否已為 CLSID 註冊 PersistentHandler。</span><span class="sxs-lookup"><span data-stu-id="a974a-187">Determine whether a PersistentHandler is registered for the CLSID.</span></span> <span data-ttu-id="a974a-188">`Value2`在步驟2中決定使用，尋找 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ Value2 專案的 PersistentHandler。</span><span class="sxs-lookup"><span data-stu-id="a974a-188">Using `Value2` determined in step 2, find the PersistentHandler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\Value2 entry.</span></span> <span data-ttu-id="a974a-189">讓此機碼成為 `Value3` 。</span><span class="sxs-lookup"><span data-stu-id="a974a-189">Let this key be `Value3`.</span></span>

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="a974a-190">判斷 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 持續性處理常式 GUID。</span><span class="sxs-lookup"><span data-stu-id="a974a-190">Determine the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) persistent handler GUID.</span></span> <span data-ttu-id="a974a-191">使用 `Value1` 和 `Value3` ，尋找檔案類型的 **IFilter** 持續性處理常式 GUID。</span><span class="sxs-lookup"><span data-stu-id="a974a-191">Using `Value1` and `Value3`, find the **IFilter** Persistent Handler GUID for the document type.</span></span> <span data-ttu-id="a974a-192">登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ Value1 或 3 \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF "/> 下的值會產生此檔案類型的 **IFilter** PersistentHandler GUID。</span><span class="sxs-lookup"><span data-stu-id="a974a-192">The value under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\Value1 or 3\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF"/> yields the **IFilter** PersistentHandler GUID for this document type.</span></span> <span data-ttu-id="a974a-193">讓此機碼成為 `Value4` 。</span><span class="sxs-lookup"><span data-stu-id="a974a-193">Let this key be `Value4`.</span></span> <span data-ttu-id="a974a-194">在此範例中， **IFilter** 介面 GUID 是89BCB740-6119-101A-BCB7-00DD010655AF。</span><span class="sxs-lookup"><span data-stu-id="a974a-194">In this example, the **IFilter** interface GUID is 89BCB740-6119-101A-BCB7-00DD010655AF.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {EEC97550-47A9-11CF-B952-00AA0051FE20}
                 = HTML File Persistent Handler
                    Data type         REG_SZ
                        PersistentAddinsRegistered
                        {89BCB740-6119-101A-BCB7-00DD010655AF}

                    Data type         REG_SZ
                        default = {E0CA5340-4534-11CF-B952-00AA0051FE20}
```

> [!NOTE]  
> <span data-ttu-id="a974a-195">在此範例中，會 nlhtml.dll HTML 檔案的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL。</span><span class="sxs-lookup"><span data-stu-id="a974a-195">In this example, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for HTML documents is nlhtml.dll.</span></span>

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a><span data-ttu-id="a974a-196">IFilter：： GetChunk 和地區設定碼識別碼</span><span class="sxs-lookup"><span data-stu-id="a974a-196">IFilter::GetChunk and Locale Code Identifiers</span></span>

<span data-ttu-id="a974a-197">文字的 LCID 可以在單一檔案中變更。</span><span class="sxs-lookup"><span data-stu-id="a974a-197">The LCID of text can change within a single file.</span></span> <span data-ttu-id="a974a-198">例如，指令手動的文字可能會在英文 (en-us) 和西班牙文 (es) ，或文字可能包含非主要語言的單一單字。</span><span class="sxs-lookup"><span data-stu-id="a974a-198">For example, the text of an instruction manual might alternate between English (en-us) and Spanish (es) or the text may include a single word in a language other than the primary language.</span></span> <span data-ttu-id="a974a-199">無論是哪一種情況，您的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 都必須在每次 LCID 變更時開始新的區塊。</span><span class="sxs-lookup"><span data-stu-id="a974a-199">In either case, your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) must begin a new chunk each time the LCID changes.</span></span> <span data-ttu-id="a974a-200">因為 LCID 是用來選擇適當的斷詞工具，所以請務必正確地加以識別。</span><span class="sxs-lookup"><span data-stu-id="a974a-200">Because the LCID is used to choose an appropriate word breaker, it is very important that you correctly identify it.</span></span> <span data-ttu-id="a974a-201">如果 **IFilter** 無法判斷文字的地區設定，則它應該會傳回值為零的 LCID 和區塊。</span><span class="sxs-lookup"><span data-stu-id="a974a-201">If the **IFilter** cannot determine the locale of the text, then it should return an LCID of zero with the chunk.</span></span> <span data-ttu-id="a974a-202">傳回零的 LCID 會導致 Windows Search 使用語言自動偵測 (LAD) 技術來判斷區塊的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="a974a-202">Returning an LCID of zero causes Windows Search to use Language Auto-Detection (LAD) technology to determine the locale ID of the chunk.</span></span> <span data-ttu-id="a974a-203">如果 Windows Search 找不到相符項，則會藉由呼叫 [GetSystemDefaultLocaleName 函數](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) 函數) ，預設為系統預設的地區設定 (。</span><span class="sxs-lookup"><span data-stu-id="a974a-203">If Windows Search cannot find a match, it defaults to the system default locale (by calling the [GetSystemDefaultLocaleName Function](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) function).</span></span> <span data-ttu-id="a974a-204">如需詳細資訊，請參閱 [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)、 [**區塊 \_ BREAKTYPE**](/windows/win32/api/filter/ne-filter-chunk_breaktype)、 [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)和 [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。</span><span class="sxs-lookup"><span data-stu-id="a974a-204">For more information, see [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**CHUNK\_BREAKTYPE**](/windows/win32/api/filter/ne-filter-chunk_breaktype), [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), and [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).</span></span>

<span data-ttu-id="a974a-205">如果您控制檔案格式，但目前不包含地區設定資訊，您應該新增使用者功能，以啟用適當的地區設定識別。</span><span class="sxs-lookup"><span data-stu-id="a974a-205">If you control the file format and it currently does not contain locale information, you should add a user feature to enable proper locale identification.</span></span> <span data-ttu-id="a974a-206">使用不相符的斷詞工具可能會導致使用者的查詢體驗不佳。</span><span class="sxs-lookup"><span data-stu-id="a974a-206">Using a mismatched word breaker can result in a poor query experience for the user.</span></span> <span data-ttu-id="a974a-207">如需詳細資訊，請參閱 [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker)。</span><span class="sxs-lookup"><span data-stu-id="a974a-207">For more information, see [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker).</span></span>

> [!NOTE]  
> <span data-ttu-id="a974a-208">篩選器會與檔案類型相關聯，如副檔名、MIME 類型或 Clsid 所表示。</span><span class="sxs-lookup"><span data-stu-id="a974a-208">Filters are associated with file types, as denoted by file name extensions, MIME types or CLSIDs.</span></span> <span data-ttu-id="a974a-209">雖然一個篩選準則可以處理多個檔案類型，但每個類型只能使用一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="a974a-209">While one filter can handle multiple file types, each type works with only one filter.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a974a-210">其他資源</span><span class="sxs-lookup"><span data-stu-id="a974a-210">Additional Resources</span></span>

- <span data-ttu-id="a974a-211">[GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。</span><span class="sxs-lookup"><span data-stu-id="a974a-211">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="a974a-212">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="a974a-212">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="a974a-213">如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a974a-213">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="a974a-214">若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a974a-214">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a974a-215">相關主題</span><span class="sxs-lookup"><span data-stu-id="a974a-215">Related topics</span></span>

[<span data-ttu-id="a974a-216">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="a974a-216">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="a974a-217">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a974a-217">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="a974a-218">從篩選處理常式傳回屬性</span><span class="sxs-lookup"><span data-stu-id="a974a-218">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="a974a-219">Windows 隨附的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="a974a-219">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="a974a-220">在 Windows Search 中執行篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="a974a-220">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="a974a-221">註冊篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="a974a-221">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="a974a-222">測試篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="a974a-222">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
