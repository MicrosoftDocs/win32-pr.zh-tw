---
title: 使用同步讀取器依 SMPTE 時間碼進行搜尋
description: 使用同步讀取器依 SMPTE 時間碼進行搜尋
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF) ，以 SMPTE 時間碼搜尋
- ASF (Advanced Systems Format) ，以 SMPTE 時間碼搜尋
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- Advanced Systems Format (ASF) 、SMPTE 時間碼
- ASF (Advanced Systems Format) ，SMPTE 時間碼
- 同步讀取器，依 SMPTE 時間碼搜尋
- 同步讀取器，SMPTE 時間碼
- SMPTE 時間代碼，搜尋
- SMPTE 時間代碼，同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314328"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a><span data-ttu-id="fee63-113">使用同步讀取器依 SMPTE 時間碼進行搜尋</span><span class="sxs-lookup"><span data-stu-id="fee63-113">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>

<span data-ttu-id="fee63-114">同步讀取器物件可以根據與影片資料流程相關聯的 SMPTE 時間代碼，來搜尋檔案中的某個點。</span><span class="sxs-lookup"><span data-stu-id="fee63-114">The synchronous reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="fee63-115">時間碼資料會封裝在以資料單位延伸的形式附加至影片範例的 [**WMT 時間 \_ 碼 \_ 延伸模組 \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) 結構中。</span><span class="sxs-lookup"><span data-stu-id="fee63-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="fee63-116">SMPTE 時間代碼是由範圍和該範圍內的時間代碼所定義。</span><span class="sxs-lookup"><span data-stu-id="fee63-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="fee63-117">範圍是連續的時間序列代碼。</span><span class="sxs-lookup"><span data-stu-id="fee63-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="fee63-118">每次程式碼都是以小時、分鐘、秒和框架來定義。</span><span class="sxs-lookup"><span data-stu-id="fee63-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="fee63-119">若要使用同步讀取器以 SMPTE 時間代碼在 ASF 檔案中搜尋資料，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="fee63-119">To seek data in an ASF file by SMPTE time code using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="fee63-120">藉由呼叫 [**IWMSyncReader：： SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)，設定範例傳遞的開始時間碼和結束時間碼。</span><span class="sxs-lookup"><span data-stu-id="fee63-120">Set the starting time code and ending time code for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="fee63-121">您必須指定依時間代碼編制索引之影片串流的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="fee63-121">You must specify the stream number of a video stream indexed by time code.</span></span> <span data-ttu-id="fee63-122">同步讀取器會將輸出的其餘部分，同步處理至指定資料流程之指定框架的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="fee63-122">The synchronous reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream.</span></span>
2.  <span data-ttu-id="fee63-123">開始使用 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)的呼叫來抓取範例。</span><span class="sxs-lookup"><span data-stu-id="fee63-123">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="fee63-124">以您平常使用同步讀取器的方式繼續進行。</span><span class="sxs-lookup"><span data-stu-id="fee63-124">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fee63-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="fee63-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fee63-126">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="fee63-126">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="fee63-127">**SMPTE 時間代碼支援**</span><span class="sxs-lookup"><span data-stu-id="fee63-127">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> <dt>

[<span data-ttu-id="fee63-128">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="fee63-128">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




