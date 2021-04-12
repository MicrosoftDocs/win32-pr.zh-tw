---
title: 使用同步讀取器依框架編號搜尋
description: 使用同步讀取器依框架編號搜尋
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF) ，依框架編號搜尋
- ASF (Advanced Systems Format) ，依框架編號搜尋
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 同步讀取器，依框架編號搜尋
- 影片串流，依畫面格編號搜尋
- 影片串流，同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314268"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a><span data-ttu-id="5927e-110">使用同步讀取器依框架編號搜尋</span><span class="sxs-lookup"><span data-stu-id="5927e-110">To Seek By Frame Number Using the Synchronous Reader</span></span>

<span data-ttu-id="5927e-111">若要使用同步讀取器依框架編號搜尋資料，您可以指定播放範圍。</span><span class="sxs-lookup"><span data-stu-id="5927e-111">To seek for data by frame number using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="5927e-112">範圍是由特定影片串流中的起始畫面格編號，以及要播放的一些畫面格所定義。</span><span class="sxs-lookup"><span data-stu-id="5927e-112">A range is defined by a starting frame number in a specific video stream and a number of frames to play.</span></span>

<span data-ttu-id="5927e-113">若要使用同步讀取器依框架號碼在 ASF 檔案中搜尋資料，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="5927e-113">To seek data in an ASF file by frame number using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="5927e-114">藉由呼叫 [**IWMSyncReader：： SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)，設定要讀取範例傳遞的起始畫面格數目和框架數目。</span><span class="sxs-lookup"><span data-stu-id="5927e-114">Set the starting frame number and number of frames to read for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="5927e-115">您必須指定框架索引影片資料流程的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="5927e-115">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="5927e-116">讀取器會將輸出的其餘部分與指定之資料流程的指定框架的呈現時間進行同步處理，並開始傳遞輸出範例。</span><span class="sxs-lookup"><span data-stu-id="5927e-116">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
2.  <span data-ttu-id="5927e-117">開始使用 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)的呼叫來抓取範例。</span><span class="sxs-lookup"><span data-stu-id="5927e-117">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="5927e-118">以您平常使用同步讀取器的方式繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5927e-118">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5927e-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="5927e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5927e-120">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="5927e-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="5927e-121">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="5927e-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




