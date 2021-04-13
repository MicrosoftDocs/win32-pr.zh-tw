---
title: 撰寫範例
description: 撰寫範例
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Advanced Systems Format (ASF) 、撰寫範例
- ASF (Advanced Systems Format) ，撰寫範例
- Advanced Systems Format (ASF) ，將範例傳遞給寫入器
- ASF (Advanced Systems Format) ，將範例傳遞給寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374426"
---
# <a name="to-write-samples"></a><span data-ttu-id="73d98-107">撰寫範例</span><span class="sxs-lookup"><span data-stu-id="73d98-107">To Write Samples</span></span>

<span data-ttu-id="73d98-108">當您識別並設定所撰寫之檔案的輸入時，可以開始將範例傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="73d98-108">When you have identified and configured the inputs for the file you are writing, you can begin passing samples to the writer.</span></span> <span data-ttu-id="73d98-109">您應盡可能以表示階段的順序傳遞範例，以使撰寫程式更有效率。</span><span class="sxs-lookup"><span data-stu-id="73d98-109">You should pass samples in presentation-time order, if possible, to make the writing process more efficient.</span></span>

<span data-ttu-id="73d98-110">在傳遞任何範例之前，您必須藉由呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)，將寫入器設定為接受這些範例。</span><span class="sxs-lookup"><span data-stu-id="73d98-110">Before passing any samples, you must set the writer to accept them by calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="73d98-111">若要將範例傳遞給寫入器，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="73d98-111">To pass a sample to the writer, perform the following steps:</span></span>

1.  <span data-ttu-id="73d98-112">藉由呼叫 [**IWMWriter：： AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)，配置緩衝區並取出 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="73d98-112">Allocate a buffer and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="73d98-113">藉由呼叫 [**INSSBuffer：： GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer)，取出在步驟1中建立的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="73d98-113">Retrieve the address of the buffer created in step 1 by calling [**INSSBuffer::GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span></span>
3.  <span data-ttu-id="73d98-114">將範例資料複製到緩衝區位置，確定傳遞的範例符合配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="73d98-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="73d98-115">您可以使用任何記憶體複製函數來複製您的資料。</span><span class="sxs-lookup"><span data-stu-id="73d98-115">You can use any memory copying function to copy your data.</span></span> <span data-ttu-id="73d98-116">常見的選擇是 memcpy，它包含在 standard C 執行時間程式庫中。</span><span class="sxs-lookup"><span data-stu-id="73d98-116">A common choice is memcpy, which is included in the standard C run-time library.</span></span>
4.  <span data-ttu-id="73d98-117">藉由呼叫 [**INSSBuffer：： SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)來更新緩衝區中使用的資料量，以反映樣本的實際大小。</span><span class="sxs-lookup"><span data-stu-id="73d98-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="73d98-118">使用 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 方法，將緩衝區介面傳遞至寫入器以及輸入編號和取樣時間。</span><span class="sxs-lookup"><span data-stu-id="73d98-118">Pass the buffer interface to the writer along with the input number and sample time using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="73d98-119">輸入的所有音訊範例都代表相同的內容持續時間，因此您可以藉由將範例持續時間新增至執行總計來找出範例時間。</span><span class="sxs-lookup"><span data-stu-id="73d98-119">All audio samples for an input represent the same duration of content, so you can figure the sample time by adding the sample duration to a running total.</span></span> <span data-ttu-id="73d98-120">針對影片，您需要根據畫面播放速率來計算時間。</span><span class="sxs-lookup"><span data-stu-id="73d98-120">For video, you need to calculate the time based on the frame rate.</span></span>

<span data-ttu-id="73d98-121">**WriteSample** 會以非同步方式運作，而且在您的應用程式準備好再次呼叫方法之前，可能不會完成從緩衝區寫入資料的作業。</span><span class="sxs-lookup"><span data-stu-id="73d98-121">**WriteSample** works asynchronously and might not finish writing the data from the buffer before your application is ready to call the method again.</span></span> <span data-ttu-id="73d98-122">因此，請務必針對 **WriteSample** 的每個呼叫呼叫 **AllocateSample** 一次。</span><span class="sxs-lookup"><span data-stu-id="73d98-122">Therefore, it is important to call **AllocateSample** once for each call to **WriteSample**.</span></span> <span data-ttu-id="73d98-123">不過，您可以在呼叫 **WriteSample** 之後立即釋放 **INSSBuffer** 介面。</span><span class="sxs-lookup"><span data-stu-id="73d98-123">However, you can release the **INSSBuffer** interface immediately after calling **WriteSample**.</span></span>

<span data-ttu-id="73d98-124">當您完成傳遞範例時，請呼叫 [**IWMWriter：： EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting)。</span><span class="sxs-lookup"><span data-stu-id="73d98-124">When you have finished passing samples, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span></span>

<span data-ttu-id="73d98-125">**注意** 很重要的是，檔案中所有資料流程的範例都必須在同步處理之間傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="73d98-125">**Note** It is important that samples from all streams in the file are passed to the writer in synchronization with one another.</span></span> <span data-ttu-id="73d98-126">也就是說，您應該盡可能在 [**IWMWriterAdvanced：： SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)指定的同步容錯內，將範例以展示時間順序傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="73d98-126">That is, whenever possible you should pass samples to the writer in presentation-time order within the sync tolerance specified in [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span> <span data-ttu-id="73d98-127">當資料以一秒或更少的單位傳遞至每個資料流程時，就可以達到最佳效果。</span><span class="sxs-lookup"><span data-stu-id="73d98-127">Best results are achieved when data is delivered to each stream in units of one second or less.</span></span>

<span data-ttu-id="73d98-128">資料流程也應該在大約相同的時間結束。</span><span class="sxs-lookup"><span data-stu-id="73d98-128">Streams should also end at approximately the same time.</span></span> <span data-ttu-id="73d98-129">例如，您不應該使用長度為45秒的音訊串流，以及長度為50秒的影片串流來寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="73d98-129">For example, you should not write a file with an audio stream that is 45 seconds long and a video stream that is 50 seconds long.</span></span> <span data-ttu-id="73d98-130">如果您使用未改變的輸入將這類檔案編碼，則會卸載資料流程結尾的某些音訊資料 (即使它是較短的資料流程) 也是一樣。</span><span class="sxs-lookup"><span data-stu-id="73d98-130">If you encode such a file with unaltered inputs, some of the audio data at the end of the stream will be dropped (even though it is the shorter stream).</span></span> <span data-ttu-id="73d98-131">若要讓檔案編碼正常運作，您應該將5秒的靜音新增至音訊輸入，讓一個資料流程不會在另一個串流之前結束數秒鐘。</span><span class="sxs-lookup"><span data-stu-id="73d98-131">To make the file encoding work, you should add 5 seconds of silence to the audio input so that one stream does not end several seconds before another.</span></span> <span data-ttu-id="73d98-132">具有間歇樣本（例如文字或影像資料流程）的資料流程類型不需要以這種方式填補。</span><span class="sxs-lookup"><span data-stu-id="73d98-132">It is not necessary for stream types with intermittent samples, like text or image streams, to be padded in this way.</span></span> <span data-ttu-id="73d98-133">指令碼命令資料流程也應遵循所有這些規則。</span><span class="sxs-lookup"><span data-stu-id="73d98-133">Script command streams should also follow all these rules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73d98-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="73d98-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d98-135">**INSSBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="73d98-135">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="73d98-136">**IWMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="73d98-136">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="73d98-137">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="73d98-137">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




