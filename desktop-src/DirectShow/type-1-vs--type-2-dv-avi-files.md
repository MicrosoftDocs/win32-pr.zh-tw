---
description: 類型-1 與
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: 類型1與類型 2 DV AVI 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944435"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a><span data-ttu-id="e9ea7-103">類型1與類型 2 DV AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="e9ea7-103">Type-1 vs. Type-2 DV AVI Files</span></span>

<span data-ttu-id="e9ea7-104">DV 攝影機產生交錯式音訊-影片;影片的每個畫面格也都包含音訊資訊。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-104">DV cameras produce interleaved audio-video; each frame of video also contains the audio information.</span></span> <span data-ttu-id="e9ea7-105">如果您將 DV 資料儲存至 AVI 檔案，您可以選擇：</span><span class="sxs-lookup"><span data-stu-id="e9ea7-105">If you save DV data to an AVI file, you have a choice:</span></span>

-   <span data-ttu-id="e9ea7-106">將交錯的資料儲存為 AVI 檔案中的一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-106">Store the interleaved data as one stream in the AVI file.</span></span> <span data-ttu-id="e9ea7-107">這就是所謂的型別1檔。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-107">This is known as a type-1 file.</span></span>
-   <span data-ttu-id="e9ea7-108">將交錯的資料分割成不同的音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-108">Split the interleaved data into separate audio and video streams.</span></span> <span data-ttu-id="e9ea7-109">這就是所謂的2型別。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-109">This is known as a type-2 file.</span></span>

<span data-ttu-id="e9ea7-110">針對影片捕獲（最大輸送量很重要），最好使用類型1檔案，因為類型2檔案攜帶了重複的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-110">For video capture, where maximum throughput is crucial, it is better to use a type-1 file, because type-2 files carry redundant audio data.</span></span> <span data-ttu-id="e9ea7-111"> (視頻串流仍包含音訊資料。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-111">(The video stream still has the audio data.</span></span> <span data-ttu-id="e9ea7-112">音訊是藉由將資料流程標示為影片來隱藏。 ) 另外，撰寫型別2檔案需要額外的處理器時間來分割交錯的資料流程。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-112">The audio is simply hidden by labeling the stream as video.) Also, writing a type-2 file requires some additional processor time to split the interleaved stream.</span></span>

<span data-ttu-id="e9ea7-113">另一方面，如果是即時編輯，則類型1檔案的效率較低。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-113">On the other hand, type-1 files are less efficient for real-time editing.</span></span> <span data-ttu-id="e9ea7-114">應用程式必須從交錯的資料流程解壓縮音訊、進行編輯，然後再次交錯資料。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-114">The application must extract the audio from the interleaved stream, make the edits, and interleave the data again.</span></span> <span data-ttu-id="e9ea7-115">此外，類型1格式與 Microsoft® Video for Windows® (VFW) 不相容。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-115">Also, the type-1 format is not compatible with Microsoft® Video for Windows® (VFW).</span></span> <span data-ttu-id="e9ea7-116">DirectShow 可以處理這兩種類型的檔案。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-116">DirectShow can handle both types of files.</span></span>

<span data-ttu-id="e9ea7-117">您可以使用 [DV Muxer](dv-muxer-filter.md) 篩選器，將類型2檔案轉換成類型1。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-117">A type-2 file can be converted to type-1 using the [DV Muxer](dv-muxer-filter.md) filter.</span></span> <span data-ttu-id="e9ea7-118">您可以使用 [DV 分隔](dv-splitter-filter.md) 器篩選器，將類型1檔案轉換成2型別。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-118">A type-1 file can be converted to type-2 using the [DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="e9ea7-119">下圖說明這兩種格式之間的差異。</span><span class="sxs-lookup"><span data-stu-id="e9ea7-119">The following diagram illustrates the difference between the two formats.</span></span>

![類型1和類型 2 dv 之間的轉換](images/dv-filters3.png)

## <a name="related-topics"></a><span data-ttu-id="e9ea7-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9ea7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ea7-122">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="e9ea7-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="e9ea7-123">AVI 檔案格式的 DV 資料</span><span class="sxs-lookup"><span data-stu-id="e9ea7-123">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



