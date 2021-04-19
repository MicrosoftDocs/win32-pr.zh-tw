---
title: 使用手動資料流程選取
description: 使用手動資料流程選取
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Advanced Systems Format (ASF) 、手動資料流程選取
- ASF (Advanced Systems Format) ，手動資料流程選取
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，資料流程選取範圍
- ASF (Advanced 系統格式) ，資料流程選取範圍
- Advanced Systems Format (ASF) ，相互排除
- ASF (Advanced Systems Format) ，相互排除
- 非同步讀取器，手動資料流程選取
- 非同步讀取器，資料流程選取
- 資料流程，手動選取
- 相互排除，手動資料流程選取
- 資料流程，非同步讀取器
- 相互排除，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966441"
---
# <a name="to-use-manual-stream-selection"></a><span data-ttu-id="63bc4-117">使用手動資料流程選取</span><span class="sxs-lookup"><span data-stu-id="63bc4-117">To Use Manual Stream Selection</span></span>

<span data-ttu-id="63bc4-118">使用 reader 物件傳遞未壓縮的範例時，您只能透過輸出編號傳遞這些範例。</span><span class="sxs-lookup"><span data-stu-id="63bc4-118">When delivering uncompressed samples with the reader object, you can deliver them only by output number.</span></span> <span data-ttu-id="63bc4-119">在互斥資料流程的情況下，這表示您只可以從一次互斥的資料流程接收樣本。</span><span class="sxs-lookup"><span data-stu-id="63bc4-119">In the case of mutually exclusive streams, this means that you can receive samples only from one stream in the mutual exclusion at a time.</span></span> <span data-ttu-id="63bc4-120">選擇要傳遞之互斥資料流程的處理方式，稱為資料流程選取。</span><span class="sxs-lookup"><span data-stu-id="63bc4-120">The process of choosing which mutually exclusive stream to deliver is called stream selection.</span></span>

<span data-ttu-id="63bc4-121">針對位元速率互斥，讀取器會根據播放時主機電腦上的條件自動選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="63bc4-121">For bit-rate mutual exclusion, the reader makes stream selections automatically based on the conditions on the host machine at playback.</span></span> <span data-ttu-id="63bc4-122">對於其他類型的互斥，除非您自行手動選取不同的資料流程，否則讀取器將會從預設資料流程傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="63bc4-122">For other types of mutual exclusion, the reader will deliver samples from the default stream unless you manually select a different stream yourself.</span></span> <span data-ttu-id="63bc4-123">當您想要從位元速率互斥中手動選取資料流程時，也可能會有實例。</span><span class="sxs-lookup"><span data-stu-id="63bc4-123">There may also be instances when you want to select a stream manually from a bit-rate mutual exclusion.</span></span>

<span data-ttu-id="63bc4-124">針對整個檔案，手動選取的資料流程為開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="63bc4-124">Manual stream selection is either on or off for the entire file.</span></span> <span data-ttu-id="63bc4-125">如果檔案包含位元速率互斥，以及一些其他互斥類型，您必須手動選取以位速率為基礎的資料流程。</span><span class="sxs-lookup"><span data-stu-id="63bc4-125">If a file contains bit-rate mutual exclusion and some other mutual exclusion type, you must select the bit rate based streams manually.</span></span>

<span data-ttu-id="63bc4-126">若要以手動方式選取互斥的資料流程，您必須執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="63bc4-126">To select a mutually exclusive stream manually, you must perform the following steps.</span></span>

1.  <span data-ttu-id="63bc4-127">藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="63bc4-127">Retrieve a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="63bc4-128">藉由呼叫 [**IWMReaderAdvanced：： SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection)來啟用手動資料流程選取。</span><span class="sxs-lookup"><span data-stu-id="63bc4-128">Enable manual stream selection by calling [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span></span>
3.  <span data-ttu-id="63bc4-129">若要找出特定的資料流程是否已選取，請呼叫 [**IWMReaderAdvanced：： GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected)。</span><span class="sxs-lookup"><span data-stu-id="63bc4-129">To find out if a particular stream is selected, call [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span></span> <span data-ttu-id="63bc4-130">您必須將指標傳遞至 [**WMT \_ 資料流程 \_ 選取**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) 列舉型別的變數。</span><span class="sxs-lookup"><span data-stu-id="63bc4-130">You must pass a pointer to a variable of the [**WMT\_STREAM\_SELECTION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) enumeration type.</span></span> <span data-ttu-id="63bc4-131">當呼叫傳回時，變數中的值將會描述資料流程目前的選取類型。</span><span class="sxs-lookup"><span data-stu-id="63bc4-131">When the call returns, the value in the variable will describe the current selection type of the stream.</span></span>
4.  <span data-ttu-id="63bc4-132">若要選取資料流程，請呼叫 [**IWMReaderAdvanced：： SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected)。</span><span class="sxs-lookup"><span data-stu-id="63bc4-132">To select a stream, call [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span></span> <span data-ttu-id="63bc4-133">這個方法可讓您同時為同步處理的資料流程切換指定多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="63bc4-133">This method enables you to specify multiple streams at the same time for synchronized stream switching.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63bc4-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="63bc4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63bc4-135">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="63bc4-135">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




