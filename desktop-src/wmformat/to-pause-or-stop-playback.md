---
title: 暫停或停止播放
description: 暫停或停止播放
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF) ，暫停播放
- ASF (Advanced Systems Format) ，暫停播放
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，停止播放
- ASF (Advanced 系統格式) ，停止播放
- Advanced Systems Format (ASF) 、播放暫停或停止
- ASF (Advanced 系統格式) 、播放暫停或停止
- 非同步讀取器，暫停播放
- 非同步讀取器，停止播放
- 非同步讀取器，播放暫停或停止
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507788"
---
# <a name="to-pause-or-stop-playback"></a><span data-ttu-id="a6f20-114">暫停或停止播放</span><span class="sxs-lookup"><span data-stu-id="a6f20-114">To Pause or Stop Playback</span></span>

<span data-ttu-id="a6f20-115">當您呼叫 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) 來開始播放檔案時，非同步讀取器將會在其本身的個別執行緒中繼續處理，直到到達檔案結尾為止。</span><span class="sxs-lookup"><span data-stu-id="a6f20-115">When you call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) to begin playing a file, the asynchronous reader will continue processing in its own separate threads until the end of the file is reached.</span></span> <span data-ttu-id="a6f20-116">您可以使用 [**IWMReader：:P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) 或 [**IWMReader：： stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) 方法，分別暫停或停止傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="a6f20-116">You can pause or stop the delivery of samples using the [**IWMReader::Pause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) or [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) methods respectively.</span></span>

## <a name="pausing"></a><span data-ttu-id="a6f20-117">正在暫停</span><span class="sxs-lookup"><span data-stu-id="a6f20-117">Pausing</span></span>

<span data-ttu-id="a6f20-118">當您呼叫 **IWMReader：:P ause** 來暫停檔案的播放時，讀取器會持續追蹤檔案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a6f20-118">When you call **IWMReader::Pause** to pause playback of a file, the reader keeps track of the current position in the file.</span></span> <span data-ttu-id="a6f20-119">若要在暫停之後繼續播放，請呼叫 [**IWMReader：： resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume)。</span><span class="sxs-lookup"><span data-stu-id="a6f20-119">To resume playing after pausing, call [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span></span> <span data-ttu-id="a6f20-120">播放將從暫停的點繼續。</span><span class="sxs-lookup"><span data-stu-id="a6f20-120">Playback will resume from the point at which it paused.</span></span>

## <a name="stopping"></a><span data-ttu-id="a6f20-121">停止中</span><span class="sxs-lookup"><span data-stu-id="a6f20-121">Stopping</span></span>

<span data-ttu-id="a6f20-122">當您呼叫 **IWMReader：： Stop** 以停止播放檔案時，讀取器不會追蹤播放進度的任何相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a6f20-122">When you call **IWMReader::Stop** to halt playback of a file, the reader does not keep track of any information about the progress of playback.</span></span> <span data-ttu-id="a6f20-123">若要使用 **Stop** 和更新版本返回停止點，您必須儲存最後一個範例所提供的呈現時間，並將它用於您對 **IWMReader：： Start** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a6f20-123">To use **Stop** and later return to the stopping point you must save the presentation time of the last sample delivered and use it in your call to **IWMReader::Start**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6f20-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6f20-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6f20-125">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="a6f20-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="a6f20-126">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="a6f20-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




