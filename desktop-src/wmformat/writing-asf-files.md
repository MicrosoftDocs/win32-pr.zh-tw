---
title: 寫入 ASF 檔案
description: 寫入 ASF 檔案
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK，寫入 ASF 檔案
- Windows Media Format SDK，建立 ASF 檔案
- 'Windows Media Format SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，寫入檔案
- ASF (Advanced Systems Format) ，寫入檔案
- Advanced Systems Format (ASF) ，建立檔案
- ASF (Advanced Systems Format) ，建立檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841892"
---
# <a name="writing-asf-files"></a><span data-ttu-id="7e988-110">寫入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="7e988-110">Writing ASF Files</span></span>

<span data-ttu-id="7e988-111">您可以使用 Windows Media Format SDK 的寫入器物件，從數位媒體資料建立 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="7e988-111">You can use the writer object of the Windows Media Format SDK to create ASF files from digital media data.</span></span> <span data-ttu-id="7e988-112">若要建立寫入器物件的實例，請呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數。</span><span class="sxs-lookup"><span data-stu-id="7e988-112">To create an instance of the writer object, call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="7e988-113">寫入器物件會協調許多元件的功能，包括 Windows Media 格式 SDK 外部的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="7e988-113">The writer object coordinates the functionality of a number of components, including codecs, which are external to the Windows Media Format SDK.</span></span>

<span data-ttu-id="7e988-114">寫入器物件的基本功能可細分為下列步驟。</span><span class="sxs-lookup"><span data-stu-id="7e988-114">The basic functionality of the writer object can be broken down into the following steps.</span></span> <span data-ttu-id="7e988-115">在這些步驟中，「應用程式」指的是您使用 Windows Media Format SDK 撰寫的程式。</span><span class="sxs-lookup"><span data-stu-id="7e988-115">In these steps, "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="7e988-116">應用程式會為寫入器提供用來建立 ASF 檔案的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e988-116">The application supplies the writer with a profile to use in creating the ASF file.</span></span> <span data-ttu-id="7e988-117">當寫入器載入設定檔資料時，它會將輸入編號指派給設定檔的每個連接。</span><span class="sxs-lookup"><span data-stu-id="7e988-117">When the writer loads the profile data, it assigns an input number to each connection of the profile.</span></span>
2.  <span data-ttu-id="7e988-118">應用程式會為寫入器提供要寫入之檔案的輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7e988-118">The application supplies the writer with an output file name for the file to be written.</span></span> <span data-ttu-id="7e988-119">寫入器會建立寫入器檔案接收物件，以管理檔案建立和輸入。</span><span class="sxs-lookup"><span data-stu-id="7e988-119">The writer creates a writer file sink object to manage the file creation and input.</span></span> <span data-ttu-id="7e988-120">如需詳細資訊，請參閱 [寫入器檔案接收物件](writer-file-sink-object.md)。</span><span class="sxs-lookup"><span data-stu-id="7e988-120">For more information, see [Writer File Sink Object](writer-file-sink-object.md).</span></span>
3.  <span data-ttu-id="7e988-121">寫入器會根據設定檔中的資訊，建立新檔案的標頭。</span><span class="sxs-lookup"><span data-stu-id="7e988-121">The writer creates a header for the new file based on information in the profile.</span></span>
4.  <span data-ttu-id="7e988-122">應用程式會將未壓縮的範例傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="7e988-122">The application passes uncompressed samples to the writer.</span></span> <span data-ttu-id="7e988-123">在緩衝區物件中包裝的緩衝區中，一次傳遞一個範例。</span><span class="sxs-lookup"><span data-stu-id="7e988-123">Samples are passed one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="7e988-124">應用程式應該同時傳遞每個資料流程的範例，讓寫入器以展示時間順序接收所有範例。</span><span class="sxs-lookup"><span data-stu-id="7e988-124">The application should pass samples for each stream concurrently so that the writer receives all samples in presentation-time order.</span></span>
5.  <span data-ttu-id="7e988-125">寫入器會將範例傳遞給適當的編解碼器以進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="7e988-125">The writer passes the samples to the appropriate codec for compression.</span></span> <span data-ttu-id="7e988-126">當寫入器收到壓縮的範例時，它會使用來自其他資料流程的範例來交錯它們，如此一來，範例就會以展示時間順序進入檔案，而不受串流。</span><span class="sxs-lookup"><span data-stu-id="7e988-126">When the writer receives the compressed samples, it interleaves them with samples from the other streams so that samples go into the file in presentation time order irrespective of stream.</span></span> <span data-ttu-id="7e988-127">然後，範例資料會變成封包，並寫入檔案的資料區段。</span><span class="sxs-lookup"><span data-stu-id="7e988-127">The sample data is then made into packets and written to the data section of the file.</span></span>
6.  <span data-ttu-id="7e988-128">當處理所有樣本時，寫入器可以將索引新增至檔案，以增強搜尋效能。</span><span class="sxs-lookup"><span data-stu-id="7e988-128">When all samples are processed, the writer can add an index to the file to enhance seeking performance.</span></span>

<span data-ttu-id="7e988-129">這些步驟說明于 WMStats 範例應用程式中，還有其他步驟。</span><span class="sxs-lookup"><span data-stu-id="7e988-129">These steps are illustrated in the WMStats sample application, among others.</span></span> <span data-ttu-id="7e988-130">如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="7e988-130">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="7e988-131">寫入器也支援更先進的功能，可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="7e988-131">The writer also supports more advanced functionality, enabling you to do the following:</span></span>

-   <span data-ttu-id="7e988-132">編輯檔案標頭中的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7e988-132">Edit metadata in the header of the file.</span></span>
-   <span data-ttu-id="7e988-133">撰寫 precompressed 範例。</span><span class="sxs-lookup"><span data-stu-id="7e988-133">Write precompressed samples.</span></span>
-   <span data-ttu-id="7e988-134">寫入網路接收器以串流處理即時資料。</span><span class="sxs-lookup"><span data-stu-id="7e988-134">Write to network sinks for streaming live data.</span></span>
-   <span data-ttu-id="7e988-135">寫入至檔案接收以取得 advanced file control 選項。</span><span class="sxs-lookup"><span data-stu-id="7e988-135">Write to file sinks for advanced file control options.</span></span>
-   <span data-ttu-id="7e988-136">寫入推播接收器，以散發給將傳遞內容給終端使用者的伺服器。</span><span class="sxs-lookup"><span data-stu-id="7e988-136">Write to push sinks for distribution to servers that will deliver content to end users.</span></span>
-   <span data-ttu-id="7e988-137">傳遞 postview 範例以驗證輸出。</span><span class="sxs-lookup"><span data-stu-id="7e988-137">Deliver postview samples for verification of output.</span></span>
-   <span data-ttu-id="7e988-138">傳遞寫入器-效能統計資料。</span><span class="sxs-lookup"><span data-stu-id="7e988-138">Deliver writer-performance statistics.</span></span>

<span data-ttu-id="7e988-139">下列各節將詳細說明如何使用寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="7e988-139">The following sections describe the use of the writer object in detail.</span></span>



| <span data-ttu-id="7e988-140">區段</span><span class="sxs-lookup"><span data-stu-id="7e988-140">Section</span></span>                                                                    | <span data-ttu-id="7e988-141">描述</span><span class="sxs-lookup"><span data-stu-id="7e988-141">Description</span></span>                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e988-142">將設定檔與寫入器搭配使用</span><span class="sxs-lookup"><span data-stu-id="7e988-142">To Use Profiles with the Writer</span></span>](to-use-profiles-with-the-writer.md)     | <span data-ttu-id="7e988-143">描述如何指定要搭配寫入器使用的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e988-143">Describes how to specify a profile to use with the writer.</span></span>                                             |
| [<span data-ttu-id="7e988-144">使用輸入</span><span class="sxs-lookup"><span data-stu-id="7e988-144">Working with Inputs</span></span>](working-with-inputs.md)                             | <span data-ttu-id="7e988-145">描述如何識別和設定寫入器中的輸入設定。</span><span class="sxs-lookup"><span data-stu-id="7e988-145">Describes how to identify and configure the input settings in the writer.</span></span>                              |
| [<span data-ttu-id="7e988-146">使用寫入器編輯中繼資料</span><span class="sxs-lookup"><span data-stu-id="7e988-146">To Edit Metadata with the Writer</span></span>](to-edit-metadata-with-the-writer.md)   | <span data-ttu-id="7e988-147">描述如何使用寫入器來編輯新檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7e988-147">Describes how to use the writer to edit metadata for a new file.</span></span>                                       |
| [<span data-ttu-id="7e988-148">撰寫範例</span><span class="sxs-lookup"><span data-stu-id="7e988-148">To Write Samples</span></span>](to-write-samples.md)                                   | <span data-ttu-id="7e988-149">描述如何將範例傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="7e988-149">Describes how to pass samples to the writer.</span></span>                                                           |
| [<span data-ttu-id="7e988-150">設定資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="7e988-150">Setting Data Unit Extensions</span></span>](setting-data-unit-extensions.md)           | <span data-ttu-id="7e988-151">說明如何將擴充資料新增至範例。</span><span class="sxs-lookup"><span data-stu-id="7e988-151">Describes how to add extended data to samples.</span></span>                                                         |
| [<span data-ttu-id="7e988-152">撰寫壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="7e988-152">Writing Compressed Samples</span></span>](writing-compressed-samples.md)               | <span data-ttu-id="7e988-153">說明如何將預先壓縮的範例傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="7e988-153">Describes how to pass pre-compressed samples to the writer.</span></span>                                            |
| [<span data-ttu-id="7e988-154">寫入影像資料流程</span><span class="sxs-lookup"><span data-stu-id="7e988-154">Writing Image Streams</span></span>](writing-image-streams.md)                         | <span data-ttu-id="7e988-155">說明如何設定影像資料流程的輸入。</span><span class="sxs-lookup"><span data-stu-id="7e988-155">Describes how to configure an input for an image stream.</span></span>                                               |
| [<span data-ttu-id="7e988-156">撰寫影片影像範例</span><span class="sxs-lookup"><span data-stu-id="7e988-156">Writing Video Image Samples</span></span>](writing-video-image-samples.md)             | <span data-ttu-id="7e988-157">說明如何設定影片影像範例。</span><span class="sxs-lookup"><span data-stu-id="7e988-157">Describes how to configure Video Image samples.</span></span>                                                        |
| [<span data-ttu-id="7e988-158">寫入變數位元速率資料流程</span><span class="sxs-lookup"><span data-stu-id="7e988-158">Writing Variable Bit Rate Streams</span></span>](writing-variable-bit-rate-streams.md) | <span data-ttu-id="7e988-159">說明如何將變數的位元速率寫入 (VBR) 資料流程。</span><span class="sxs-lookup"><span data-stu-id="7e988-159">Describes how to write variable bit rate (VBR) streams.</span></span>                                                |
| [<span data-ttu-id="7e988-160">使用 Two-Pass 編碼</span><span class="sxs-lookup"><span data-stu-id="7e988-160">Using Two-Pass Encoding</span></span>](using-two-pass-encoding.md)                     | <span data-ttu-id="7e988-161">描述如何在寫入檔案之前，讓編解碼器先執行初步傳遞。</span><span class="sxs-lookup"><span data-stu-id="7e988-161">Describes how to have the codec perform a preliminary pass before writing the file.</span></span>                    |
| [<span data-ttu-id="7e988-162">強制插入 Key-Frame</span><span class="sxs-lookup"><span data-stu-id="7e988-162">To Force Key-Frame Insertion</span></span>](to-force-key-frame-insertion.md)           | <span data-ttu-id="7e988-163">說明如何手動強制編解碼器將範例編碼為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="7e988-163">Describes how to manually force the codec to encode a sample as a key frame.</span></span>                           |
| [<span data-ttu-id="7e988-164">管理寫入器延遲</span><span class="sxs-lookup"><span data-stu-id="7e988-164">To Manage Writer Latency</span></span>](to-manage-writer-latency.md)                   | <span data-ttu-id="7e988-165">描述如何將撰寫範例所需的時間降到最低，以將範例處理到輸出檔或接收。</span><span class="sxs-lookup"><span data-stu-id="7e988-165">Describes how to minimize the time it takes the writer to process samples into an output file or sink.</span></span> |
| [<span data-ttu-id="7e988-166">使用寫入器接收器</span><span class="sxs-lookup"><span data-stu-id="7e988-166">Working with Writer Sinks</span></span>](working-with-writer-sinks.md)                 | <span data-ttu-id="7e988-167">說明如何使用寫入器接收將內容傳遞至檔案或網路位置。</span><span class="sxs-lookup"><span data-stu-id="7e988-167">Describes how to use writer sinks to deliver your content to files or network locations.</span></span>               |
| [<span data-ttu-id="7e988-168">取得寫入器統計資料</span><span class="sxs-lookup"><span data-stu-id="7e988-168">To Get Writer Statistics</span></span>](to-get-writer-statistics.md)                   | <span data-ttu-id="7e988-169">描述如何取得寫入器的統計資料。</span><span class="sxs-lookup"><span data-stu-id="7e988-169">Describes how to get statistics for the writer.</span></span>                                                        |
| [<span data-ttu-id="7e988-170">使用寫入器 Postview</span><span class="sxs-lookup"><span data-stu-id="7e988-170">To Use Writer Postview</span></span>](to-use-writer-postview.md)                       | <span data-ttu-id="7e988-171">描述當您撰寫要驗證的檔案時，如何取得未壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="7e988-171">Describes how to get uncompressed samples as you write a file for verification.</span></span>                        |



 

## <a name="related-topics"></a><span data-ttu-id="7e988-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e988-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e988-173">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="7e988-173">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="7e988-174">**寫入器檔案接收物件**</span><span class="sxs-lookup"><span data-stu-id="7e988-174">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="7e988-175">**寫入器網路接收物件**</span><span class="sxs-lookup"><span data-stu-id="7e988-175">**Writer Network Sink Object**</span></span>](writer-network-sink-object.md)
</dt> <dt>

[<span data-ttu-id="7e988-176">**寫入器物件**</span><span class="sxs-lookup"><span data-stu-id="7e988-176">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




