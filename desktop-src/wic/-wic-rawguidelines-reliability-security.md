---
description: 可靠性和安全性
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: 可靠性和安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0f0e4a244de2c1463cdadb76162c18b041812b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996883"
---
# <a name="reliability-and-security"></a><span data-ttu-id="53592-103">可靠性和安全性</span><span class="sxs-lookup"><span data-stu-id="53592-103">Reliability and Security</span></span>

<span data-ttu-id="53592-104">因為 Windows 影像處理元件 (WIC) 編解碼器會從 Windows shell 和影像中心中叫用，所以編解碼器作者應盡全力確保其 WIC 編解碼器中的高可用性和安全性。</span><span class="sxs-lookup"><span data-stu-id="53592-104">Because Windows Imaging Component (WIC) codecs will be invoked from within the Windows shell and Photo Gallery, codec authors should make every effort to ensure a high level of reliability and security in their WIC codecs.</span></span>

<span data-ttu-id="53592-105">撰寫可靠的程式碼大多取決於良好的程式碼撰寫作法、有效的程式碼評論，以及完整的單元測試和案例測試。</span><span class="sxs-lookup"><span data-stu-id="53592-105">Writing reliable code largely depends on good coding practices, effective code reviews, and thorough unit testing and scenario testing.</span></span> <span data-ttu-id="53592-106">此外，下列指導方針可協助確保編解碼器符合與可靠性相關的 Windows Vista 原則。</span><span class="sxs-lookup"><span data-stu-id="53592-106">In addition, the following guidelines will help ensure that the codec complies with Windows Vista policies regarding reliability.</span></span>

-   <span data-ttu-id="53592-107">啟用 i/o 取消。</span><span class="sxs-lookup"><span data-stu-id="53592-107">Enable I/O cancellation.</span></span>

    <span data-ttu-id="53592-108">編解碼器作者應提供方法讓終端使用者取消任何長時間執行的作業。</span><span class="sxs-lookup"><span data-stu-id="53592-108">Codec authors should provide a way for the end user to cancel any long-running operation.</span></span> <span data-ttu-id="53592-109">WIC 編解碼器是藉由實 IWICBitmapProgressNotification 來支援。</span><span class="sxs-lookup"><span data-stu-id="53592-109">WIC codecs support this by implementing IWICBitmapProgressNotification.</span></span> <span data-ttu-id="53592-110">這可讓呼叫的應用程式指定回呼函式，讓編解碼器在指定的間隔呼叫，以通知呼叫端目前作業的進度。</span><span class="sxs-lookup"><span data-stu-id="53592-110">This allows a calling application to specify a callback function for the codec to call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="53592-111">當應用程式傳回從回呼函式取消的錯誤時 \_ ，編解碼器必須取消正在進行中的任何作業，並將 HRESULT 傳播回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="53592-111">When an application returns ERROR\_CANCELLED from the callback function, the codec must cancel whatever operation is in progress and propagate the HRESULT back to the caller.</span></span> <span data-ttu-id="53592-112">這對原始編解碼器而言特別重要，因為它可能需要幾秒鐘的時間來解碼完整大小的原始影像，而應用程式需要一種方法來中止這項處理。</span><span class="sxs-lookup"><span data-stu-id="53592-112">This is especially important for RAW codecs, because it might take several seconds to decode a full-size RAW image and applications need a way to abort this processing.</span></span>

-   <span data-ttu-id="53592-113">請確定程式碼是在執行其函式所需的最小範圍內執行。</span><span class="sxs-lookup"><span data-stu-id="53592-113">Make sure that code runs in the smallest scope that is required to perform its function.</span></span>

    <span data-ttu-id="53592-114">編解碼器作者必須確保編解碼器不會取用超過所需的資源，或有比所需更大的範圍。</span><span class="sxs-lookup"><span data-stu-id="53592-114">Codec authors must ensure that the codec does not consume more resources than necessary or have a greater scope than is required.</span></span> <span data-ttu-id="53592-115">WIC 中的編解碼器範圍是單一影像檔案;當載入影像檔案時，會建立編解碼器，並在關閉映射時釋放編解碼器。</span><span class="sxs-lookup"><span data-stu-id="53592-115">The scope of a codec in WIC is a single image file; the codec is created when an image file is loaded, and the codec is released when the image is closed.</span></span> <span data-ttu-id="53592-116">因為 WIC 是可延伸的元件平臺，所以 WIC 編解碼器會有重迭的載入和卸載，並且會啟動和停止，全都在相同的進程中。</span><span class="sxs-lookup"><span data-stu-id="53592-116">Because WIC is an extensible component-based platform, WIC codecs will have overlapping loads and unloads, and starts and stops, all within the same process.</span></span> <span data-ttu-id="53592-117">如果編解碼器的基礎基礎結構需要在大於單一映射的範圍中啟動和停止作業，則可靠性將會受到影響。</span><span class="sxs-lookup"><span data-stu-id="53592-117">If the underlying infrastructure of a codec requires start and stop operations at a scope larger than a single image, reliability will be impacted.</span></span> <span data-ttu-id="53592-118">Windows 檔案總管及其他應用程式會使用已啟用 WIC 的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="53592-118">WIC-enabled codecs will be used by the Windows Explorer, as well as other applications.</span></span> <span data-ttu-id="53592-119">因此，如果在進程的存留期內仍載入編解碼器，記憶體將不會有效率地釋出，而且編解碼器的失敗可能會使 Windows 檔案總管停止回應，而且可能需要重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="53592-119">Therefore, if a codec remains loaded for the lifetime of the process, memory will not be released efficiently and a failure of the codec could hang Windows Explorer and potentially require the machine to be rebooted.</span></span> <span data-ttu-id="53592-120"> (請考慮每次在 Windows 檔案總管中 thumbnailed 映射時都會叫用編解碼器：這是輕量作業的關鍵。 ) </span><span class="sxs-lookup"><span data-stu-id="53592-120">(Consider that the codec will be invoked every time an image is thumbnailed for the first time in Windows Explorer: it is essential that this be a lightweight operation.)</span></span>

-   <span data-ttu-id="53592-121">使用靜態和動態程式碼分析工具。</span><span class="sxs-lookup"><span data-stu-id="53592-121">Use static and dynamic code analysis tools.</span></span>

    -   <span data-ttu-id="53592-122">靜態分析工具：</span><span class="sxs-lookup"><span data-stu-id="53592-122">Static analysis tools:</span></span>

        <span data-ttu-id="53592-123">前置詞-用於偵測編譯時期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="53592-123">PREfix - for detecting errors at compile time.</span></span>

        <span data-ttu-id="53592-124">PREfast-用於分析 bug 的程式碼。</span><span class="sxs-lookup"><span data-stu-id="53592-124">PREfast - for analyzing code for bugs.</span></span>

    -   <span data-ttu-id="53592-125">動態分析工具：</span><span class="sxs-lookup"><span data-stu-id="53592-125">Dynamic analysis tools:</span></span>

        <span data-ttu-id="53592-126">AppVerifier-藉由模擬常見的真實世界軟體問題，有助於讓應用程式更具彈性。</span><span class="sxs-lookup"><span data-stu-id="53592-126">AppVerifier - which helps make applications more resilient by simulating common real-world software issues.</span></span>

-   <span data-ttu-id="53592-127">確認程式碼審核中的所有輸入。</span><span class="sxs-lookup"><span data-stu-id="53592-127">Verify all inputs in code reviews.</span></span>

    <span data-ttu-id="53592-128">所有匯出方法和所有檔案資料的參數都必須謹慎地經過驗證，以確保其有效性，並在發生錯誤時妥善拒絕，以防止緩衝區溢位和不足、算術溢位和下溢，以及非預期的類型。</span><span class="sxs-lookup"><span data-stu-id="53592-128">All parameters for exported methods and all file data must be carefully verified for validity and robustly rejected if faulty, in order to protect against buffer overruns and underruns, arithmetic overflows and underflows, and unexpected types.</span></span>

-   <span data-ttu-id="53592-129">使用檔案模糊化技術來探索潛在的當機和停止回應。</span><span class="sxs-lookup"><span data-stu-id="53592-129">Use file fuzzing techniques to discover potential crashes and hangs.</span></span>

    <span data-ttu-id="53592-130">檔案模糊化是以隨機排列的輸入來測試編解碼器的流程。</span><span class="sxs-lookup"><span data-stu-id="53592-130">File fuzzing is the process of testing the codec with randomly permuted inputs.</span></span>

    <span data-ttu-id="53592-131">有兩種形式的檔案模糊化： undirected (隨機) 模糊化和導向的模糊。</span><span class="sxs-lookup"><span data-stu-id="53592-131">There are two forms of file fuzzing: undirected (random) fuzzing and directed fuzzing.</span></span> <span data-ttu-id="53592-132">Undirected 模糊化會執行一些隨機的位，以查看隨機輸入是否可能會損毀編解碼器。</span><span class="sxs-lookup"><span data-stu-id="53592-132">Undirected fuzzing does some random bit flipping to see if random input can crash the codec.</span></span> <span data-ttu-id="53592-133">導向的模糊會根據檔案格式的某些知識 permutes 輸入。</span><span class="sxs-lookup"><span data-stu-id="53592-133">Directed fuzzing permutes the input based on some knowledge of the file format.</span></span> <span data-ttu-id="53592-134">例如，如果迴圈冗余檢查 (CRC) 在位元組位移32，則變更任何未更新 CRC 的位元組可能不會執行大部分的 codepaths。</span><span class="sxs-lookup"><span data-stu-id="53592-134">For example, if there is a cycle redundancy check (CRC) at byte offset 32, then changing any bytes without updating the CRC will likely not exercise most of the codepaths.</span></span> <span data-ttu-id="53592-135">在此範例中，當任何位元組遭到修改時，導向的 fuzzer 應該會修正 CRC。</span><span class="sxs-lookup"><span data-stu-id="53592-135">In this example, a directed fuzzer should fix the CRC when any bytes are modified.</span></span>

    <span data-ttu-id="53592-136">應建立檔案模糊化的影像輸入集，以便測試此解碼器支援的每個參數組合。</span><span class="sxs-lookup"><span data-stu-id="53592-136">The input set of images for file fuzzing should be created so that each parameter combination that the decoder supports is tested.</span></span> <span data-ttu-id="53592-137">例如，如果此解碼器支援小位元組、大到小的檔案和三個壓縮設定，則映射的輸入集應該包含每個壓縮設定的位元組由小到大檔案，以及每個壓縮設定的位元組由大到小的檔案。</span><span class="sxs-lookup"><span data-stu-id="53592-137">For example, if the decoder supports little- and big-endian files and three compression settings, then the input set of image should consist of little-endian files of each compression setting and big-endian files for each compression setting.</span></span> <span data-ttu-id="53592-138">這種方法會產生一組大型但非常穩固的輸入影像來進行測試。</span><span class="sxs-lookup"><span data-stu-id="53592-138">This approach will yield a large, but very robust set of input images to be tested.</span></span> <span data-ttu-id="53592-139">即使沒有任何相機會產生每個組合，但是編碼器支援這些理論組合，編解碼器作者應模糊這些輸入。</span><span class="sxs-lookup"><span data-stu-id="53592-139">Even if no camera produces each of the combinations but the decoder supports these theoretical combinations, codec authors should fuzz these inputs.</span></span>

    <span data-ttu-id="53592-140">在編解碼器開發期間定期執行影像檔案的模糊測試，可以大幅增強安全性。</span><span class="sxs-lookup"><span data-stu-id="53592-140">Security can be greatly enhanced by regularly performing fuzz testing of image files during codec development.</span></span> <span data-ttu-id="53592-141">編解碼器在格式不正確的要求或格式不正確的情況下，應該一律能夠偵測影像檔損毀並正常失敗。</span><span class="sxs-lookup"><span data-stu-id="53592-141">Codecs should always be able to detect image file corruption and fail gracefully in the case of a malformed request or of malformed data.</span></span>

-   <span data-ttu-id="53592-142">將程式碼壓力。</span><span class="sxs-lookup"><span data-stu-id="53592-142">Stress the code.</span></span>

    <span data-ttu-id="53592-143">對編解碼器進行壓力測試，方法是在多個同時執行的程式中持續執行，並在各種不同大小的影像上，以所有可能的循序執行所有支援的作業， (包括每個支援相機) 的非常大型影像。</span><span class="sxs-lookup"><span data-stu-id="53592-143">Stress-test the codec by running it continually in multiple simultaneous processes, performing all supported operations in all possible sequences, on images of varying sizes (including very large images) from every supported camera.</span></span>

-   <span data-ttu-id="53592-144">執行緒安全性。</span><span class="sxs-lookup"><span data-stu-id="53592-144">Thread safety.</span></span>

    <span data-ttu-id="53592-145">從 Windows 7，WIC 要求原始編解碼器必須是 COM 單元類型 "Both"。</span><span class="sxs-lookup"><span data-stu-id="53592-145">As of Windows 7, WIC requires that RAW CODECs be of COM apartment type "Both".</span></span> <span data-ttu-id="53592-146">這表示您必須在多執行緒案例中，進行適當的鎖定來處理跨單元呼叫端和呼叫端。</span><span class="sxs-lookup"><span data-stu-id="53592-146">This means that you must do the appropriate locking to handle cross-apartment callers and callers in multi-threaded scenarios.</span></span> <span data-ttu-id="53592-147">多執行緒單元內的物件 (MTA) 可由 MTA 內任意數目的執行緒同時呼叫，以在多核心系統和某些伺服器案例上提供更佳的效能。</span><span class="sxs-lookup"><span data-stu-id="53592-147">Objects within an Multi Threaded Apartment (MTA) may be called concurrently by any number of threads within the MTA, allowing for better performance on multi-core systems and certain server scenarios.</span></span> <span data-ttu-id="53592-148">此外，位於 MTA 內的 WIC 編解碼器可以呼叫位於 MTA 內的其他物件，而不需要在位於不同 STA 單元的執行緒之間呼叫的封送處理成本。</span><span class="sxs-lookup"><span data-stu-id="53592-148">In addition, WIC CODECs that live within an MTA can call other objects that live within the MTA without the marshalling cost associated of calling between threads that live in different STA apartments.</span></span> <span data-ttu-id="53592-149">在 Windows 7 中，所有的內建 WIC 編解碼器都已更新為支援 Mta，包括 JPEG、TIFF、PNG、GIF、.ICO 和 BMP。</span><span class="sxs-lookup"><span data-stu-id="53592-149">In Windows 7, all in-box WIC CODECs have been updated to support MTAs, including JPEG, TIFF, PNG, GIF, ICO, and BMP.</span></span> <span data-ttu-id="53592-150">不支援 Mta 的協力廠商編解碼器會在多執行緒應用程式中造成顯著的效能成本，因為封送處理。</span><span class="sxs-lookup"><span data-stu-id="53592-150">3rd-party CODECs that do not to support MTAs will cause significant performance costs in multithreaded applications due to marshaling.</span></span> <span data-ttu-id="53592-151">啟用 MTA 支援需要在協力廠商編解碼器中執行適當的同步處理。</span><span class="sxs-lookup"><span data-stu-id="53592-151">Enabling MTA support requires proper synchronization to be implemented in the 3rd-party CODEC.</span></span> <span data-ttu-id="53592-152">這些同步處理技術的確切執行已超出本檔的範圍。</span><span class="sxs-lookup"><span data-stu-id="53592-152">Exact implementation of these synchronization techniques is beyond the scope of this paper.</span></span> <span data-ttu-id="53592-153">以下提供同步處理 COM 物件的一般參考。</span><span class="sxs-lookup"><span data-stu-id="53592-153">A general reference for synchronizing COM objects is provided below.</span></span>

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a><span data-ttu-id="53592-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="53592-154">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="53592-155">**概念**</span><span class="sxs-lookup"><span data-stu-id="53592-155">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53592-156">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="53592-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="53592-157">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="53592-157">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="53592-158">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="53592-158">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



