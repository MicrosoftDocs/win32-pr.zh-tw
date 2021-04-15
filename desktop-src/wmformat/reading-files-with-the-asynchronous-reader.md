---
title: 使用非同步讀取器讀取檔案
description: 使用非同步讀取器讀取檔案
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media Format SDK，讀取檔案
- Windows Media Format SDK，非同步讀取器
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- 非同步讀取器，IWMReaderCallback 介面
- IWMReaderCallback，非同步讀取器
- 非同步讀取器，讀取檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374403"
---
# <a name="reading-files-with-the-asynchronous-reader"></a><span data-ttu-id="ef240-112">使用非同步讀取器讀取檔案</span><span class="sxs-lookup"><span data-stu-id="ef240-112">Reading Files with the Asynchronous Reader</span></span>

<span data-ttu-id="ef240-113">非同步讀取器會使用多個執行緒和非同步呼叫來讀取 ASF 檔案中的內容。</span><span class="sxs-lookup"><span data-stu-id="ef240-113">The asynchronous reader reads the content from ASF files using multiple threads and asynchronous calls.</span></span> <span data-ttu-id="ef240-114">非同步讀取器所支援的功能，適用于將內容呈現給使用者的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ef240-114">The features supported by the asynchronous reader make it well suited for applications that render content to end users.</span></span>

<span data-ttu-id="ef240-115">讀取器物件的最基本功能可細分為下列步驟。</span><span class="sxs-lookup"><span data-stu-id="ef240-115">The most basic functionality of the reader object can be broken down into the following steps.</span></span> <span data-ttu-id="ef240-116">在這些步驟中，「應用程式」指的是您使用 Windows Media Format SDK 撰寫的程式。</span><span class="sxs-lookup"><span data-stu-id="ef240-116">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="ef240-117">應用程式會執行 [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) 介面，以處理來自讀取器的訊息。</span><span class="sxs-lookup"><span data-stu-id="ef240-117">The application implements the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) interface to handle messages from the reader.</span></span> <span data-ttu-id="ef240-118">這包括兩個回呼方法： **OnStatus**，它會接收與讀取器和 **OnSample** 的各個層面狀態相關的訊息，這會從讀取器接收未壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="ef240-118">This includes two callback methods: **OnStatus**, which receives messages relating to the status of various aspects of the reader and **OnSample**, which receives uncompressed samples from the reader.</span></span>
2.  <span data-ttu-id="ef240-119">應用程式會將要讀取的檔案名傳遞給讀取器。</span><span class="sxs-lookup"><span data-stu-id="ef240-119">The application passes to the reader the name of a file to read.</span></span> <span data-ttu-id="ef240-120">當讀取器開啟檔案時，它會將輸出編號指派給每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="ef240-120">When the reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="ef240-121">如果檔案使用相互排除，讀取器會為所有互斥資料流程指派單一輸出。</span><span class="sxs-lookup"><span data-stu-id="ef240-121">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
3.  <span data-ttu-id="ef240-122">應用程式會從讀取器取得各種輸出的設定相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef240-122">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="ef240-123">收集的資訊將可讓應用程式正確地轉譯媒體範例。</span><span class="sxs-lookup"><span data-stu-id="ef240-123">The information gathered will enable the application to properly render media samples.</span></span>
4.  <span data-ttu-id="ef240-124">應用程式會指示讀取器開始從檔案讀取資料。</span><span class="sxs-lookup"><span data-stu-id="ef240-124">The application instructs the reader to begin reading data from the file.</span></span> <span data-ttu-id="ef240-125">讀取器會開始將未壓縮的範例傳遞給 **OnSample** 回呼，並在緩衝區物件中包裝的緩衝區中一次傳遞一個。</span><span class="sxs-lookup"><span data-stu-id="ef240-125">The reader begins delivering uncompressed samples to the **OnSample** callback one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="ef240-126">讀取器所提供的範例處於展示階段順序。</span><span class="sxs-lookup"><span data-stu-id="ef240-126">The samples delivered by the reader are in presentation-time order.</span></span> <span data-ttu-id="ef240-127">讀取器將繼續傳遞範例，直到應用程式停止為止，或直到到達檔案結尾為止。</span><span class="sxs-lookup"><span data-stu-id="ef240-127">The reader will continue delivering samples until stopped by the application or until the end of the file is reached.</span></span>
5.  <span data-ttu-id="ef240-128">應用程式會在讀取器傳遞之後，負責呈現資料。</span><span class="sxs-lookup"><span data-stu-id="ef240-128">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="ef240-129">Windows Media Format SDK 不提供任何轉譯常式。</span><span class="sxs-lookup"><span data-stu-id="ef240-129">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="ef240-130">一般而言，應用程式會使用其他 Sdk 來呈現資料，例如 Microsoft DirectX® SDK，或 Microsoft Windows Platform SDK 的多媒體功能。</span><span class="sxs-lookup"><span data-stu-id="ef240-130">Typically, applications will use other SDKs to render data, such as the Microsoft DirectX® SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>
6.  <span data-ttu-id="ef240-131">當讀取完成時，應用程式會指示讀取器關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="ef240-131">When reading is complete, the application instructs the reader to close the file.</span></span>

<span data-ttu-id="ef240-132">這些步驟說明于 >audioplayer 範例應用程式中，還有其他步驟。</span><span class="sxs-lookup"><span data-stu-id="ef240-132">These steps are illustrated in the AudioPlayer sample application, among others.</span></span> <span data-ttu-id="ef240-133">如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="ef240-133">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="ef240-134">讀取器也支援更先進的功能。</span><span class="sxs-lookup"><span data-stu-id="ef240-134">The reader also supports more advanced functionality.</span></span> <span data-ttu-id="ef240-135">讀取器可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="ef240-135">The reader enables you to do the following:</span></span>

-   <span data-ttu-id="ef240-136">暫停檔案的播放。</span><span class="sxs-lookup"><span data-stu-id="ef240-136">Pause playback of a file.</span></span>
-   <span data-ttu-id="ef240-137">取得讀取器效能統計資料。</span><span class="sxs-lookup"><span data-stu-id="ef240-137">Retrieve reader performance statistics.</span></span>
-   <span data-ttu-id="ef240-138">適用于互斥資料流程的控制資料流程選取範圍。</span><span class="sxs-lookup"><span data-stu-id="ef240-138">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="ef240-139">手動設定緩衝區以進行輸出。</span><span class="sxs-lookup"><span data-stu-id="ef240-139">Manually allocate buffers for output.</span></span>
-   <span data-ttu-id="ef240-140">提供您自己的時鐘。</span><span class="sxs-lookup"><span data-stu-id="ef240-140">Provide your own clock.</span></span>
-   <span data-ttu-id="ef240-141">取得檔案作業的狀態 (緩衝、下載或儲存) 。</span><span class="sxs-lookup"><span data-stu-id="ef240-141">Retrieve the status of file operations (buffering, download, or save).</span></span>
-   <span data-ttu-id="ef240-142">使用標準 COM 介面、 **IStream** 來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="ef240-142">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="ef240-143">搜尋 ASF 檔案中的特定點。</span><span class="sxs-lookup"><span data-stu-id="ef240-143">Seek to specific points in an ASF file.</span></span>
-   <span data-ttu-id="ef240-144">從檔案標頭讀取設定檔資料。</span><span class="sxs-lookup"><span data-stu-id="ef240-144">Read profile data from the header of the file.</span></span>

<span data-ttu-id="ef240-145">下列各節將詳細說明如何使用 reader 物件。</span><span class="sxs-lookup"><span data-stu-id="ef240-145">The following sections describe the use of the reader object in detail.</span></span>

-   [<span data-ttu-id="ef240-146">在 OnStatus 回呼中執行讀取器訊息</span><span class="sxs-lookup"><span data-stu-id="ef240-146">To Implement Reader Messages in the OnStatus Callback</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [<span data-ttu-id="ef240-147">若要執行 OnSample 回呼</span><span class="sxs-lookup"><span data-stu-id="ef240-147">To Implement the OnSample Callback</span></span>](to-implement-the-onsample-callback.md)
-   [<span data-ttu-id="ef240-148">建立讀取器並開啟檔案</span><span class="sxs-lookup"><span data-stu-id="ef240-148">To Create a Reader and Open a File</span></span>](to-create-a-reader-and-open-a-file.md)
-   [<span data-ttu-id="ef240-149">使用非同步讀取器取出媒體範例</span><span class="sxs-lookup"><span data-stu-id="ef240-149">To Retrieve Media Samples with the Asynchronous Reader</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [<span data-ttu-id="ef240-150">使用非同步讀取器依時間進行搜尋</span><span class="sxs-lookup"><span data-stu-id="ef240-150">To Seek By Time Using the Asynchronous Reader</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="ef240-151">使用非同步讀取器依框架編號搜尋</span><span class="sxs-lookup"><span data-stu-id="ef240-151">To Seek By Frame Number Using the Asynchronous Reader</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="ef240-152">使用非同步讀取器依 SMPTE 時間程式碼進行搜尋</span><span class="sxs-lookup"><span data-stu-id="ef240-152">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="ef240-153">搜尋標記</span><span class="sxs-lookup"><span data-stu-id="ef240-153">To Seek to Markers</span></span>](to-seek-to-markers.md)
-   [<span data-ttu-id="ef240-154">暫停或停止播放</span><span class="sxs-lookup"><span data-stu-id="ef240-154">To Pause or Stop Playback</span></span>](to-pause-or-stop-playback.md)
-   [<span data-ttu-id="ef240-155">取得讀取器效能統計資料</span><span class="sxs-lookup"><span data-stu-id="ef240-155">To Get Reader Performance Statistics</span></span>](to-get-reader-performance-statistics.md)
-   [<span data-ttu-id="ef240-156">使用手動資料流程選取</span><span class="sxs-lookup"><span data-stu-id="ef240-156">To Use Manual Stream Selection</span></span>](to-use-manual-stream-selection.md)
-   [<span data-ttu-id="ef240-157">使用非同步讀取器傳遞壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="ef240-157">To Deliver Compressed Samples with the Asynchronous Reader</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a><span data-ttu-id="ef240-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef240-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef240-159">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="ef240-159">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="ef240-160">**讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="ef240-160">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




