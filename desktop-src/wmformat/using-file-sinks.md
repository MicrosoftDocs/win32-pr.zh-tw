---
title: 使用檔案接收
description: 使用檔案接收
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Advanced Systems Format (ASF) ，file 接收
- ASF (Advanced Systems Format) ，file 接收
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收，檔案接收
- 檔接收，關於
- 檔案接收，建立
- 檔案接收，停止
- 檔案接收，開始
- 檔案接收，關閉
- 接收、統計資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092583"
---
# <a name="using-file-sinks"></a><span data-ttu-id="0392b-114">使用檔案接收</span><span class="sxs-lookup"><span data-stu-id="0392b-114">Using File Sinks</span></span>

<span data-ttu-id="0392b-115">在一般情況下，您可以使用 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) 方法，直接傳遞寫入器的輸出檔名稱，而寫入器物件會自動將檔案寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="0392b-115">Under normal circumstances, you can simply pass the writer an output file name using the [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) method, and the writer object will write the file to disk automatically.</span></span> <span data-ttu-id="0392b-116">在此情況下，寫入器實際上是建立和控制寫入器檔案接收物件，該物件會處理將檔案寫入磁片的程式。</span><span class="sxs-lookup"><span data-stu-id="0392b-116">In this case, the writer is actually creating and controlling a writer file sink object that handles writing the file to disk.</span></span> <span data-ttu-id="0392b-117">寫入器檔案接收物件可控制從寫入器物件到單一檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="0392b-117">A writer file sink object controls the flow of data from the writer object to a single file.</span></span>

<span data-ttu-id="0392b-118">您可以建立自己的檔案接收，以更充分掌控接收器寫入檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="0392b-118">You can create your own file sinks to get more control over how the sink writes the file.</span></span> <span data-ttu-id="0392b-119">您也可以存取寫入器所建立的預設寫入器檔案接收，以回應 **SetOutputFilename** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0392b-119">You can also access the default writer file sink created by the writer in response to a call to **SetOutputFilename**.</span></span>

## <a name="creating-file-sinks"></a><span data-ttu-id="0392b-120">建立檔案接收</span><span class="sxs-lookup"><span data-stu-id="0392b-120">Creating File Sinks</span></span>

<span data-ttu-id="0392b-121">若要建立檔案接收並將它新增至寫入器，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="0392b-121">To create a file sink and add it to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="0392b-122">藉由呼叫 [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) 函數來建立新的接收。</span><span class="sxs-lookup"><span data-stu-id="0392b-122">Create a new sink by calling the [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) function.</span></span>
2.  <span data-ttu-id="0392b-123">藉由呼叫 [**IWMWriterFileSink：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open)，提供接收的檔案名。</span><span class="sxs-lookup"><span data-stu-id="0392b-123">Supply a file name for the sink by calling [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span></span>
3.  <span data-ttu-id="0392b-124">藉由呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink)，將 file 接收新增至寫入器。</span><span class="sxs-lookup"><span data-stu-id="0392b-124">Add the file sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span></span>
4.  <span data-ttu-id="0392b-125">以一般方式執行撰寫。</span><span class="sxs-lookup"><span data-stu-id="0392b-125">Perform writing in the usual way.</span></span>
5.  <span data-ttu-id="0392b-126">寫入完成後，接收會自動關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="0392b-126">After writing is completed, the sink will close the file automatically.</span></span>

## <a name="stopping-and-starting-file-sinks"></a><span data-ttu-id="0392b-127">停止和開機檔案接收</span><span class="sxs-lookup"><span data-stu-id="0392b-127">Stopping and Starting File Sinks</span></span>

<span data-ttu-id="0392b-128">開始寫入作業之後，您可以藉由呼叫 [**IWMWriterFileSink2：： stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop)來停止寫入至檔案接收。</span><span class="sxs-lookup"><span data-stu-id="0392b-128">After writing operations begin, you can stop writing to a file sink by calling [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span></span>

<span data-ttu-id="0392b-129">您可能會想要停止寫入接收的原因很多。</span><span class="sxs-lookup"><span data-stu-id="0392b-129">There are many potential reasons why you would want to stop writing to a sink.</span></span> <span data-ttu-id="0392b-130">例如，如果您是從即時來源進行錄製，您可能只對部分內容感興趣。</span><span class="sxs-lookup"><span data-stu-id="0392b-130">For example, if you are recording from a live source, you may only be interested in some of the content.</span></span>

<span data-ttu-id="0392b-131">您可以藉由呼叫 [**IWMWriterFileSink2：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start)來繼續寫入至檔案接收。</span><span class="sxs-lookup"><span data-stu-id="0392b-131">You can resume writing to a file sink by calling [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span></span> <span data-ttu-id="0392b-132">[ **停止** 並 **開始** ] 會使用呈現時間來控制大約執行命令的時間。</span><span class="sxs-lookup"><span data-stu-id="0392b-132">Both **Stop** and **Start** use presentation times to control approximately when the command is executed.</span></span> <span data-ttu-id="0392b-133">您可以使用 [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) 方法來更充分掌控開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="0392b-133">You can use the [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) methods to gain more control over start and stop times.</span></span>

## <a name="closing-file-sinks"></a><span data-ttu-id="0392b-134">關閉檔接收</span><span class="sxs-lookup"><span data-stu-id="0392b-134">Closing File Sinks</span></span>

<span data-ttu-id="0392b-135">一般情況下，檔案接收會自動關閉。</span><span class="sxs-lookup"><span data-stu-id="0392b-135">Normally, a file sink is closed automatically.</span></span> <span data-ttu-id="0392b-136">如果您已完成寫入至接收，但是將作業寫入其他接收，則應該明確地關閉接收以節省資源。</span><span class="sxs-lookup"><span data-stu-id="0392b-136">If you are finished writing to a sink, but writing operations to other sinks are continuing, you should explicitly close the sink to conserve resources.</span></span> <span data-ttu-id="0392b-137">若要關閉 file 接收器，請呼叫 [**IWMWriterFileSink2：： close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close)。</span><span class="sxs-lookup"><span data-stu-id="0392b-137">To close a file sink, call [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span></span>

## <a name="getting-sink-statistics"></a><span data-ttu-id="0392b-138">取得接收統計資料</span><span class="sxs-lookup"><span data-stu-id="0392b-138">Getting Sink Statistics</span></span>

<span data-ttu-id="0392b-139">您可以分別呼叫 [**IWMWriterFileSink2：： GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) 和 [**IWMWriterFileSink2：： GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) ，來取得開啟接收器的檔案大小和持續時間。</span><span class="sxs-lookup"><span data-stu-id="0392b-139">You can get the file size and duration for an open sink by calling [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) and [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0392b-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="0392b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0392b-141">**IWMWriterFileSink 介面**</span><span class="sxs-lookup"><span data-stu-id="0392b-141">**IWMWriterFileSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[<span data-ttu-id="0392b-142">**IWMWriterFileSink2 介面**</span><span class="sxs-lookup"><span data-stu-id="0392b-142">**IWMWriterFileSink2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[<span data-ttu-id="0392b-143">**IWMWriterFileSink3 介面**</span><span class="sxs-lookup"><span data-stu-id="0392b-143">**IWMWriterFileSink3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[<span data-ttu-id="0392b-144">**寫入器檔案接收物件**</span><span class="sxs-lookup"><span data-stu-id="0392b-144">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="0392b-145">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="0392b-145">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




