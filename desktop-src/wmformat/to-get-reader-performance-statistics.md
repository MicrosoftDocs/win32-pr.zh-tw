---
title: 取得讀取器效能統計資料
description: 取得讀取器效能統計資料
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF) ，讀取器效能統計資料
- ASF (Advanced 系統格式) ，讀取器效能統計資料
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，效能統計資料
- ASF (Advanced Systems Format) ，效能統計資料
- 非同步讀取器，效能統計資料
- 效能，讀取器統計資料
- 效能，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841888"
---
# <a name="to-get-reader-performance-statistics"></a><span data-ttu-id="77ce1-112">取得讀取器效能統計資料</span><span class="sxs-lookup"><span data-stu-id="77ce1-112">To Get Reader Performance Statistics</span></span>

<span data-ttu-id="77ce1-113">使用非同步讀取器在本機讀取檔案時，不需要檢查讀取作業的效能。</span><span class="sxs-lookup"><span data-stu-id="77ce1-113">When reading files locally with the asynchronous reader, it is not necessary to check the performance of reading operations.</span></span> <span data-ttu-id="77ce1-114">但是，如果您的應用程式是從串流來源讀取，則效能統計資料可能很重要。</span><span class="sxs-lookup"><span data-stu-id="77ce1-114">If your application is reading from a streaming source however, performance statistics can be very important.</span></span> <span data-ttu-id="77ce1-115">您的應用程式可以回應播放效能的變更，以確保能獲得最佳的終端使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="77ce1-115">Your application can respond to changes in playback performance to ensure the best possible end-user experience.</span></span>

<span data-ttu-id="77ce1-116">您可以從讀取器中取出的效能資訊包括下列統計資料：</span><span class="sxs-lookup"><span data-stu-id="77ce1-116">The performance information you can retrieve from the reader includes the following statistics:</span></span>

-   <span data-ttu-id="77ce1-117">連接目前的頻寬。</span><span class="sxs-lookup"><span data-stu-id="77ce1-117">The current bandwidth of the connection.</span></span>
-   <span data-ttu-id="77ce1-118">從伺服器收到的封包數目。</span><span class="sxs-lookup"><span data-stu-id="77ce1-118">The number of packets received from the server.</span></span>
-   <span data-ttu-id="77ce1-119">已復原之遺失的封包數目。</span><span class="sxs-lookup"><span data-stu-id="77ce1-119">The number of lost packets that were recovered.</span></span>
-   <span data-ttu-id="77ce1-120">未復原之遺失的封包數目。</span><span class="sxs-lookup"><span data-stu-id="77ce1-120">The number of lost packets that were not recovered.</span></span>
-   <span data-ttu-id="77ce1-121">已接收之已傳送封包總數的百分比。</span><span class="sxs-lookup"><span data-stu-id="77ce1-121">The percentage of the total number of packets sent that have been received.</span></span>

<span data-ttu-id="77ce1-122">若要取得讀取器效能統計資料，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="77ce1-122">To get reader performance statistics, perform the following steps.</span></span>

1.  <span data-ttu-id="77ce1-123">開始播放之前，請先建立 [**WM \_ 讀取器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) 結構。</span><span class="sxs-lookup"><span data-stu-id="77ce1-123">Before starting playback, create a [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure.</span></span> <span data-ttu-id="77ce1-124">您必須將 **cbSize** 成員設定為 SIZEOF (WM \_ 讀取器 \_ 統計資料) 。</span><span class="sxs-lookup"><span data-stu-id="77ce1-124">You must set the **cbSize** member to sizeof(WM\_READER\_STATISTICS).</span></span>
2.  <span data-ttu-id="77ce1-125">藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="77ce1-125">Obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="77ce1-126">在播放期間，請經常呼叫 [**IWMReaderAdvanced：： GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) 來監視效能。</span><span class="sxs-lookup"><span data-stu-id="77ce1-126">During playback, make calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) frequently to monitor performance.</span></span> <span data-ttu-id="77ce1-127">在每次呼叫時傳遞您的 **WM \_ 讀取器 \_ 統計資料** 結構，並檢查適當的成員。</span><span class="sxs-lookup"><span data-stu-id="77ce1-127">Pass your **WM\_READER\_STATISTICS** structure with each call and examine the appropriate members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77ce1-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="77ce1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ce1-129">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="77ce1-129">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




