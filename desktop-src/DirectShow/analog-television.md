---
description: 類比電視
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: 類比電視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109001"
---
# <a name="analog-television"></a><span data-ttu-id="1f7e2-103">類比電視</span><span class="sxs-lookup"><span data-stu-id="1f7e2-103">Analog Television</span></span>

<span data-ttu-id="1f7e2-104">類比電視與其他影片捕獲案例有數種不同之處：</span><span class="sxs-lookup"><span data-stu-id="1f7e2-104">Analog television differs from other video capture scenarios in several ways:</span></span>

-   <span data-ttu-id="1f7e2-105">調諧器卡會調整為類比信號，然後進行數位化。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-105">The tuner card tunes to an analog signal, which is then digitized.</span></span>
-   <span data-ttu-id="1f7e2-106">音訊會攜帶在類比信號中。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-106">Audio is carried in the analog signal.</span></span> <span data-ttu-id="1f7e2-107">音訊觸達音效卡的方式，會隨著硬體而異。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-107">How the audio reaches the sound card varies depending on the hardware.</span></span>
-   <span data-ttu-id="1f7e2-108">信號可能會以垂直空白間隔包含額外的資料 (VBI) ，例如隱藏式輔助字幕 (副本) 、World Standard Teletext (WST) 和外延資料服務 (XDS) 。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-108">The signal may contain additional data in the vertical blanking interval (VBI), such as closed captions (CC), World Standard Teletext (WST), and extended data services (XDS).</span></span>

<span data-ttu-id="1f7e2-109">下圖顯示電視 preview 的一般篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-109">The following diagram shows a typical filter graph for television preview.</span></span>

![類比電視圖](images/vidcap06.png)

-   <span data-ttu-id="1f7e2-111">[電視調諧器](tv-tuner-filter.md)篩選器會控制微調。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-111">The [TV Tuner](tv-tuner-filter.md) filter controls tuning.</span></span>
-   <span data-ttu-id="1f7e2-112">[電視音訊](tv-audio-filter.md)篩選器會控制音訊解碼。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-112">The [TV Audio](tv-audio-filter.md) filter controls the audio decoding.</span></span>
-   <span data-ttu-id="1f7e2-113">如果調諧器卡有一個以上的實體輸入，則 [類比視頻縱橫](analog-video-crossbar-filter.md) 條篩選器可讓應用程式選取已解碼和轉譯的輸入。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-113">If the tuner card has more than one physical input, the [Analog Video Crossbar](analog-video-crossbar-filter.md) filter enables the application to select which input is decoded and rendered.</span></span>
-   <span data-ttu-id="1f7e2-114">[WDM 影片捕獲](wdm-video-capture-filter.md)篩選器會傳遞數位化的影片串流。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-114">The [WDM Video Capture](wdm-video-capture-filter.md) filter delivers the digitized video stream.</span></span>

<span data-ttu-id="1f7e2-115">「捕獲圖形產生器」會自動從「捕捉」篩選器中插入任何需要上游的篩選。</span><span class="sxs-lookup"><span data-stu-id="1f7e2-115">The Capture Graph Builder automatically inserts any filters that are required upstream from the capture filter.</span></span>

<span data-ttu-id="1f7e2-116">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="1f7e2-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1f7e2-117">類比電視微調</span><span class="sxs-lookup"><span data-stu-id="1f7e2-117">Analog Television Tuning</span></span>](analog-television-tuning.md)
-   [<span data-ttu-id="1f7e2-118">類比電視音訊</span><span class="sxs-lookup"><span data-stu-id="1f7e2-118">Analog Television Audio</span></span>](analog-television-audio.md)
-   [<span data-ttu-id="1f7e2-119">隱藏式輔助字幕和 Teletext</span><span class="sxs-lookup"><span data-stu-id="1f7e2-119">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)

## <a name="related-topics"></a><span data-ttu-id="1f7e2-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f7e2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f7e2-121">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="1f7e2-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



