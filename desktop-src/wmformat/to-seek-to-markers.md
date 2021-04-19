---
title: 搜尋標記
description: 搜尋標記
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Advanced Systems Format (ASF) ，搜尋標記
- ASF (Advanced Systems Format) ，搜尋標記
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，標記
- ASF (Advanced Systems Format) ，標記
- 非同步讀取器，搜尋標記
- 非同步讀取器，標記
- 標記，搜尋
- 標記，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106980273"
---
# <a name="to-seek-to-markers"></a><span data-ttu-id="78d70-113">搜尋標記</span><span class="sxs-lookup"><span data-stu-id="78d70-113">To Seek to Markers</span></span>

<span data-ttu-id="78d70-114">標記是 ASF 檔案中的命名位置。</span><span class="sxs-lookup"><span data-stu-id="78d70-114">A marker is a named location in an ASF file.</span></span> <span data-ttu-id="78d70-115">您只能使用非同步讀取器，從標記的位置開始播放。</span><span class="sxs-lookup"><span data-stu-id="78d70-115">You can only start playback from the location of a marker by using the asynchronous reader.</span></span> <span data-ttu-id="78d70-116">您可以遵循下列步驟，開始在標記上播放。</span><span class="sxs-lookup"><span data-stu-id="78d70-116">You can begin playback at a marker by following these steps.</span></span>

1.  <span data-ttu-id="78d70-117">呼叫 **IWMReader：： QueryInterface** 以取得 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="78d70-117">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span>
2.  <span data-ttu-id="78d70-118">藉由呼叫 [**IWMHeaderInfo：： GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount)，以取出檔案中的標記總數。</span><span class="sxs-lookup"><span data-stu-id="78d70-118">Retrieve the total number of markers in the file by calling [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span></span>
3.  <span data-ttu-id="78d70-119">使用步驟2中取出的標記計數，逐一查看標記。</span><span class="sxs-lookup"><span data-stu-id="78d70-119">Loop through the markers, using the marker count retrieved in step 2.</span></span> <span data-ttu-id="78d70-120">針對每個標記呼叫 [**IWMHeaderInfo：： GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) ，以抓取每個標記的名稱和時間。</span><span class="sxs-lookup"><span data-stu-id="78d70-120">Retrieve the name and time of each marker by calling [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) for each.</span></span> <span data-ttu-id="78d70-121">儲存所需標記的索引。</span><span class="sxs-lookup"><span data-stu-id="78d70-121">Save the index of the desired marker.</span></span>
4.  <span data-ttu-id="78d70-122">呼叫 **IWMReader：： QueryInterface** 以取得 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="78d70-122">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface.</span></span>
5.  <span data-ttu-id="78d70-123">藉由呼叫 [**IWMReaderAdvanced2：： StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)，指定要開始播放的標記。</span><span class="sxs-lookup"><span data-stu-id="78d70-123">Specify the marker at which to start playback by calling [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span></span> <span data-ttu-id="78d70-124">您必須傳遞所需標記的索引，這是您在步驟3中儲存的標記。</span><span class="sxs-lookup"><span data-stu-id="78d70-124">You must pass the index of the desired marker, which you saved in step 3.</span></span>
6.  <span data-ttu-id="78d70-125">如同您在 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 方法的實中一般地處理範例。</span><span class="sxs-lookup"><span data-stu-id="78d70-125">Handle the samples as you normally would in your implementation of the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78d70-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="78d70-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78d70-127">**標記**</span><span class="sxs-lookup"><span data-stu-id="78d70-127">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="78d70-128">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="78d70-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="78d70-129">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="78d70-129">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




