---
description: Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Windows Search 中篩選處理常式的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511108"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="828a3-103">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="828a3-103">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="828a3-104">Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。</span><span class="sxs-lookup"><span data-stu-id="828a3-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="828a3-105">您可以藉由撰寫篩選處理常式來將內容解壓縮，並將屬性處理常式解壓縮以解壓縮檔案的內容，藉此擴充 Windows Search 來為新的或專屬的檔案類型編制索引。</span><span class="sxs-lookup"><span data-stu-id="828a3-105">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="828a3-106">篩選器會與檔案類型相關聯，如副檔名、MIME 類型或類別識別碼， (Clsid) 。</span><span class="sxs-lookup"><span data-stu-id="828a3-106">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="828a3-107">雖然一個篩選準則可以處理多個檔案類型，但每個類型只能使用一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="828a3-107">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="828a3-108">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="828a3-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="828a3-109">機器碼</span><span class="sxs-lookup"><span data-stu-id="828a3-109">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="828a3-110">Windows Search 的安全程式碼做法</span><span class="sxs-lookup"><span data-stu-id="828a3-110">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="828a3-111">其他資源</span><span class="sxs-lookup"><span data-stu-id="828a3-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="828a3-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="828a3-112">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="828a3-113">機器碼</span><span class="sxs-lookup"><span data-stu-id="828a3-113">Native Code</span></span>

<span data-ttu-id="828a3-114">在 Windows 7 和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選。</span><span class="sxs-lookup"><span data-stu-id="828a3-114">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="828a3-115">篩選準則必須以機器碼撰寫，因為有多個增益集在中執行的進程可能發生 CLR 版本控制問題。</span><span class="sxs-lookup"><span data-stu-id="828a3-115">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="828a3-116">Windows Search 的安全程式碼做法</span><span class="sxs-lookup"><span data-stu-id="828a3-116">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="828a3-117">以下是撰寫安全應用程式以搭配 Windows Search 使用的做法。</span><span class="sxs-lookup"><span data-stu-id="828a3-117">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="828a3-118">**針對查詢應用程式：**</span><span class="sxs-lookup"><span data-stu-id="828a3-118">**For query applications:**</span></span>

-   <span data-ttu-id="828a3-119">撰寫搜尋用戶端時，您應該選擇在安全性內容中執行的 API，讓使用者擁有最低許可權。</span><span class="sxs-lookup"><span data-stu-id="828a3-119">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="828a3-120">例如，ASP 頁面可以使用 IXSSO query 物件，該物件會以使用者進程的形式執行。</span><span class="sxs-lookup"><span data-stu-id="828a3-120">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="828a3-121">**針對 Ifilter 和語言資源：**</span><span class="sxs-lookup"><span data-stu-id="828a3-121">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="828a3-122">如果將檔案類型的新篩選處理常式安裝為現有篩選註冊的取代，則安裝程式應儲存目前的註冊，並在新的篩選器處理常式卸載時還原。</span><span class="sxs-lookup"><span data-stu-id="828a3-122">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="828a3-123">沒有任何機制可連結篩選。</span><span class="sxs-lookup"><span data-stu-id="828a3-123">There is no mechanism to chain filters.</span></span> <span data-ttu-id="828a3-124">因此，新的篩選處理常式會負責複寫舊篩選器的任何必要功能。</span><span class="sxs-lookup"><span data-stu-id="828a3-124">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="828a3-125">Windows Search 在本機安全性內容中執行的 Ifilter、斷詞工具和字幹分析器。</span><span class="sxs-lookup"><span data-stu-id="828a3-125">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="828a3-126">它們應該寫入來管理緩衝區，並正確地堆疊。</span><span class="sxs-lookup"><span data-stu-id="828a3-126">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="828a3-127">所有字串複本都必須有明確的檢查，以防止緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="828a3-127">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="828a3-128">您應該一律確認已配置的緩衝區大小，並根據緩衝區大小測試資料的大小。</span><span class="sxs-lookup"><span data-stu-id="828a3-128">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="828a3-129">緩衝區溢位是利用不會強制執行緩衝區大小限制之程式碼的常見技術。</span><span class="sxs-lookup"><span data-stu-id="828a3-129">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="828a3-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)、斷詞工具和字幹分析器元件絕對不應該呼叫 [ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函式函式或會終止進程及其所有線程的類似 API。</span><span class="sxs-lookup"><span data-stu-id="828a3-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="828a3-131">請勿在 DllMain 進入點中配置或釋放資源。</span><span class="sxs-lookup"><span data-stu-id="828a3-131">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="828a3-132">這可能會導致低資源壓力測試期間發生失敗。</span><span class="sxs-lookup"><span data-stu-id="828a3-132">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="828a3-133">將所有物件編寫為安全線程。</span><span class="sxs-lookup"><span data-stu-id="828a3-133">Code all objects to be thread-safe.</span></span> <span data-ttu-id="828a3-134">Windows Search 一次在一個執行緒中呼叫斷詞工具或分析器的任一個實例，但它可能會在多個執行緒上同時呼叫多個實例。</span><span class="sxs-lookup"><span data-stu-id="828a3-134">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="828a3-135">避免建立暫存檔案或寫入登錄。</span><span class="sxs-lookup"><span data-stu-id="828a3-135">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="828a3-136">如果您使用 Microsoft Visual C++ 編譯器，請務必使用 **/gs** 選項來編譯應用程式。</span><span class="sxs-lookup"><span data-stu-id="828a3-136">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="828a3-137">**/Gs** 選項可用來偵測緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="828a3-137">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="828a3-138">/GS 選項會將安全性檢查放入已編譯的程式碼中。</span><span class="sxs-lookup"><span data-stu-id="828a3-138">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="828a3-139">如需詳細資訊， [](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)請參閱  / Platform SDK Visual C++ 編譯器選項一節中的 DllGetClassObject 函式 **GS** (緩衝區安全性檢查) 。</span><span class="sxs-lookup"><span data-stu-id="828a3-139">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="828a3-140">其他資源</span><span class="sxs-lookup"><span data-stu-id="828a3-140">Additional Resources</span></span>

-   <span data-ttu-id="828a3-141">[IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)範例會示範如何建立用來執行 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基類。</span><span class="sxs-lookup"><span data-stu-id="828a3-141">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="828a3-142">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="828a3-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="828a3-143">如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="828a3-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="828a3-144">若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="828a3-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="828a3-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="828a3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="828a3-146">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="828a3-146">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="828a3-147">關於 Windows Search 中的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="828a3-147">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="828a3-148">從篩選處理常式傳回屬性</span><span class="sxs-lookup"><span data-stu-id="828a3-148">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="828a3-149">Windows 隨附的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="828a3-149">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="828a3-150">在 Windows Search 中執行篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="828a3-150">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="828a3-151">註冊篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="828a3-151">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="828a3-152">測試篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="828a3-152">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
