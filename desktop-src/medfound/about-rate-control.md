---
description: 關於速率控制
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: 關於速率控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977014"
---
# <a name="about-rate-control"></a><span data-ttu-id="56175-103">關於速率控制</span><span class="sxs-lookup"><span data-stu-id="56175-103">About Rate Control</span></span>

<span data-ttu-id="56175-104">在媒體基礎中， *播放速率* 會以目前播放速率與正常播放速率的比率表示。</span><span class="sxs-lookup"><span data-stu-id="56175-104">In Media Foundation, the *playback rate* is expressed as the ratio of the current playback rate to the normal playback rate.</span></span> <span data-ttu-id="56175-105">例如，速率2.0 是兩倍的一般速度，而0.5 是半一般的速度。</span><span class="sxs-lookup"><span data-stu-id="56175-105">For example, a rate of 2.0 is twice normal speed, and 0.5 is half normal speed.</span></span> <span data-ttu-id="56175-106">負數值表示反向播放。</span><span class="sxs-lookup"><span data-stu-id="56175-106">Negative values indicate reverse playback.</span></span> <span data-ttu-id="56175-107">播放速率為-2.0，會以正常速度的兩倍向前播放資料流程。</span><span class="sxs-lookup"><span data-stu-id="56175-107">A playback rate of -2.0 plays backward through the stream at twice the normal speed.</span></span> <span data-ttu-id="56175-108">速率為零會導致一個框架呈現;之後，表示時鐘不會前進。</span><span class="sxs-lookup"><span data-stu-id="56175-108">A rate of zero causes one frame to be rendered; after that, the presentation clock does not advance.</span></span> <span data-ttu-id="56175-109">若要取得零速率的另一個畫面格，應用程式必須搜尋至新的位置。</span><span class="sxs-lookup"><span data-stu-id="56175-109">To get another frame at the rate of zero, the application must seek to a new position.</span></span>

<span data-ttu-id="56175-110">應用程式會使用下列介面來控制播放速率。</span><span class="sxs-lookup"><span data-stu-id="56175-110">Applications use the following interfaces to control the playback rate.</span></span>

-   <span data-ttu-id="56175-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)。</span><span class="sxs-lookup"><span data-stu-id="56175-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="56175-112">用來找出可能最快且最慢的播放速率。</span><span class="sxs-lookup"><span data-stu-id="56175-112">Used to find out the fastest and slowest playback rates that are possible.</span></span>
-   <span data-ttu-id="56175-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。</span><span class="sxs-lookup"><span data-stu-id="56175-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="56175-114">用來變更播放速率。</span><span class="sxs-lookup"><span data-stu-id="56175-114">Used to change the playback rate.</span></span>

<span data-ttu-id="56175-115">若要取得這兩個介面，請呼叫媒體會話上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 。</span><span class="sxs-lookup"><span data-stu-id="56175-115">To get these two interfaces, call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the Media Session.</span></span> <span data-ttu-id="56175-116">服務識別碼為 MF \_ 速率 \_ 控制 \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="56175-116">The service identifier is MF\_RATE\_CONTROL\_SERVICE.</span></span>

<span data-ttu-id="56175-117">藉由使用速率控制服務，應用程式可以執行向前快轉和反向播放。</span><span class="sxs-lookup"><span data-stu-id="56175-117">By using the rate control service, an application can implement fast forward and reverse playback.</span></span>

## <a name="thinning"></a><span data-ttu-id="56175-118">細化</span><span class="sxs-lookup"><span data-stu-id="56175-118">Thinning</span></span>

<span data-ttu-id="56175-119">*Thinning* 是可減少資料流程中樣本數的任何程式，以降低整體的位元速率。</span><span class="sxs-lookup"><span data-stu-id="56175-119">*Thinning* is any process that reduces the number of samples in a stream, to reduce the overall bit rate.</span></span> <span data-ttu-id="56175-120">針對影片，通常會藉由卸載 delta 框架並只傳遞主要畫面格來完成 thinning。</span><span class="sxs-lookup"><span data-stu-id="56175-120">For video, thinning is generally accomplished by dropping the delta frames and delivering only the key frames.</span></span> <span data-ttu-id="56175-121">管線通常可以使用 thinned 播放支援更快速的播放率，因為資料速率較低，因為差異畫面格未解碼。</span><span class="sxs-lookup"><span data-stu-id="56175-121">Often the pipeline can support faster playback rates using thinned playback, because the data rate is lower because delta frames are not decoded.</span></span>

<span data-ttu-id="56175-122">Thinning 不會變更樣本上的時間戳記或持續時間。</span><span class="sxs-lookup"><span data-stu-id="56175-122">Thinning does not change the time stamps or durations on the samples.</span></span> <span data-ttu-id="56175-123">例如，如果影片資料流程的名義費率為每秒25個畫面格，則每個畫面格的持續時間仍會標示為40毫秒，即使媒體來源正在卸載所有的 delta 框架也一樣。</span><span class="sxs-lookup"><span data-stu-id="56175-123">For example, if the nominal rate of the video stream is 25 frames per second, the duration of each frame is still marked as 40 milliseconds, even if the media source is dropping all of the delta frames.</span></span> <span data-ttu-id="56175-124">這表示一個畫面尾和下一個畫面格的開頭之間會有時間間距。</span><span class="sxs-lookup"><span data-stu-id="56175-124">That means there will be a time gap between the end of one frame and the start of the next.</span></span>

## <a name="scrubbing"></a><span data-ttu-id="56175-125">Scrubbing</span><span class="sxs-lookup"><span data-stu-id="56175-125">Scrubbing</span></span>

<span data-ttu-id="56175-126">清除 *程式是透過* 與捲軸、時間軸或其他視覺標記法的互動，立即搜尋資料流程中的特定點。</span><span class="sxs-lookup"><span data-stu-id="56175-126">*Scrubbing* is the process of instantaneously seeking to specific points in the stream by interacting with a scrollbar, timeline, or other visual representation of time.</span></span> <span data-ttu-id="56175-127">這一期來自于來回滾輪一個磁片區以找出一個區段，就像是使用磁帶來清除播放標頭一樣。</span><span class="sxs-lookup"><span data-stu-id="56175-127">The term comes from the era of reel-to-reel tape players when rocking a reel back and forth to locate a section was like scrubbing the playback head with the tape.</span></span>

<span data-ttu-id="56175-128">藉由將播放速率設定為零，在媒體基礎中執行清除。</span><span class="sxs-lookup"><span data-stu-id="56175-128">Scrubbing is implemented in Media Foundation by setting the playback rate to zero.</span></span> <span data-ttu-id="56175-129">如需詳細資訊，請參閱 [如何執行](how-to-perform-scrubbing.md)清除。</span><span class="sxs-lookup"><span data-stu-id="56175-129">For more information, see [How to Perform Scrubbing](how-to-perform-scrubbing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56175-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="56175-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56175-131">速率控制</span><span class="sxs-lookup"><span data-stu-id="56175-131">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="56175-132">搜尋、向前快轉及反向播放</span><span class="sxs-lookup"><span data-stu-id="56175-132">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[<span data-ttu-id="56175-133">服務介面</span><span class="sxs-lookup"><span data-stu-id="56175-133">Service Interfaces</span></span>](service-interfaces.md)
</dt> </dl>

 

 



