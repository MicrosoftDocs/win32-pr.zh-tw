---
title: 選取設定檔功能
description: 選取設定檔功能
ms.assetid: 5e09000d-1417-43aa-9e9c-0aff536d52b7
keywords:
- 設定檔，特徵選取
- 設定檔，選取功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769b10387bb4fb660c31678b406090cfc7e42743
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968424"
---
# <a name="selecting-profile-features"></a><span data-ttu-id="9260d-105">選取設定檔功能</span><span class="sxs-lookup"><span data-stu-id="9260d-105">Selecting Profile Features</span></span>

<span data-ttu-id="9260d-106">下表列出設定檔功能，並說明何時或不想要使用它們。</span><span class="sxs-lookup"><span data-stu-id="9260d-106">The following table lists the profile features and describes when you would or would not want to use them.</span></span>



| <span data-ttu-id="9260d-107">功能</span><span class="sxs-lookup"><span data-stu-id="9260d-107">Feature</span></span>                            | <span data-ttu-id="9260d-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="9260d-108">When to use</span></span>                                                                                                                                                                                                                                                                                                                | <span data-ttu-id="9260d-109">不使用時</span><span class="sxs-lookup"><span data-stu-id="9260d-109">When not to use</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9260d-110">依位元速率 (MBR) 相互排除</span><span class="sxs-lookup"><span data-stu-id="9260d-110">Mutual exclusion by bit rate (MBR)</span></span> | <span data-ttu-id="9260d-111">檔案將會串流處理至物件，其連線速度會因使用者而異 (例如，透過網際網路) 傳遞的檔案。</span><span class="sxs-lookup"><span data-stu-id="9260d-111">The file will be streamed to an audience with connection speeds that vary from user to user (for example, files delivered over the Internet).</span></span>                                                                                                                                                                              | <span data-ttu-id="9260d-112">檔案不會透過網路進行資料流程處理。檔案會透過具有一致可靠可用頻寬的網路進行串流處理 (例如，透過公司區域網路提供的檔案) 。</span><span class="sxs-lookup"><span data-stu-id="9260d-112">The file will not be streamed over a network.The file will be streamed over a network with a consistently reliable available bandwidth (for example, files delivered over a corporate local area network).</span></span><br/>                                                              |
| <span data-ttu-id="9260d-113">依語言的相互排除</span><span class="sxs-lookup"><span data-stu-id="9260d-113">Mutual exclusion by language</span></span>       | <span data-ttu-id="9260d-114">檔案包含以不同語言複製相同資料的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9260d-114">The file contains streams that duplicate the same data in different languages.</span></span> <span data-ttu-id="9260d-115"> (例如，以數種語言來配音的電影會有以「互斥」資料流程的形式編碼的聲段。 ) </span><span class="sxs-lookup"><span data-stu-id="9260d-115">(For example, a movie dubbed in several languages would have the soundtrack encoded as mutually exclusive streams.)</span></span>                                                                                                                         | <span data-ttu-id="9260d-116">檔案只包含單一語言的資料流程。如果檔案只包含必須針對個別語言變更的資料流程，則為每種語言建立新檔案可能會比較簡單 (例如，針對影片串流中有大量文字的定型電影) 。</span><span class="sxs-lookup"><span data-stu-id="9260d-116">The file contains only streams in a single language.If the file contains only streams that must be changed for individual languages, it may be simpler to create a new file for each language (for example, for a training film with lots of text in the video stream).</span></span><br/> |
| <span data-ttu-id="9260d-117">依簡報的相互排除</span><span class="sxs-lookup"><span data-stu-id="9260d-117">Mutual exclusion by presentation</span></span>   | <span data-ttu-id="9260d-118">您想要以一個以上的外觀比例提供影片。</span><span class="sxs-lookup"><span data-stu-id="9260d-118">You want to provide video in more than one aspect ratio.</span></span> <span data-ttu-id="9260d-119">例如，檔案可能包含針對電視格式化的相同影片，以及適用于原始電影全螢幕格式的影片。</span><span class="sxs-lookup"><span data-stu-id="9260d-119">For example, a file might contain the same video formatted for television and for the original theatrical wide-screen format.</span></span>                                                                                                                                     | <span data-ttu-id="9260d-120">每個影片串流只有一個版本。</span><span class="sxs-lookup"><span data-stu-id="9260d-120">There is only one version of each video stream.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="9260d-121">頻寬共用</span><span class="sxs-lookup"><span data-stu-id="9260d-121">Bandwidth sharing</span></span>                  | <span data-ttu-id="9260d-122">檔案將會進行串流處理，並有兩個或多個資料流程（合併時）使用較少的可用頻寬，而這兩個數據流的位元速率值會加在一起。</span><span class="sxs-lookup"><span data-stu-id="9260d-122">The file will be streamed and has two or more streams that, when combined, use less available bandwidth than the bit rate values of both streams added together.</span></span> <span data-ttu-id="9260d-123">因為資料流程的位元速率基本上是資料流程所需的最大頻寬，所以某些資料流程可能會有一些較低的資料傳輸時間。</span><span class="sxs-lookup"><span data-stu-id="9260d-123">Because the bit rate of a stream is essentially the maximum required bandwidth for the stream, some streams may have some periods of lower data transfer.</span></span> | <span data-ttu-id="9260d-124">檔案不會透過網路進行資料流程處理。所有串流都具有一致的位元速率。</span><span class="sxs-lookup"><span data-stu-id="9260d-124">The file will not be streamed over a network.All streams have consistent bit rates.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="9260d-125">資料流程優先順序</span><span class="sxs-lookup"><span data-stu-id="9260d-125">Stream prioritization</span></span>              | <span data-ttu-id="9260d-126">檔案會經過資料流程處理，有些資料流程比其他串流更重要。</span><span class="sxs-lookup"><span data-stu-id="9260d-126">The file will be streamed and some streams are more important than others.</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="9260d-127">檔案不會透過網路進行資料流程處理。所有串流都有相等的重要性。</span><span class="sxs-lookup"><span data-stu-id="9260d-127">The file will not be streamed over a network.All streams are of equal importance.</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="9260d-128">資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="9260d-128">Data Unit Extensions</span></span>               | <span data-ttu-id="9260d-129">資料流程中的範例必須與範例保持相關的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="9260d-129">There is important information related to the samples in a stream that must be kept with the samples.</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="9260d-130">此檔案的目的是要透過受限制的頻寬進行傳遞。</span><span class="sxs-lookup"><span data-stu-id="9260d-130">The file is intended for delivery through a restricted bandwidth.</span></span> <span data-ttu-id="9260d-131">在此情況下，資料單位延伸可能會使用太多額外負荷。</span><span class="sxs-lookup"><span data-stu-id="9260d-131">In this case, data unit extensions may use too much overhead.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="9260d-132">在建立設定檔時，請務必考慮您想要搭配檔案使用的編解碼器功能。</span><span class="sxs-lookup"><span data-stu-id="9260d-132">It is also important to consider the codec features that you want to use with your file when creating a profile.</span></span> <span data-ttu-id="9260d-133">如需詳細資訊，請參閱 [編解碼器功能](codec-features.md)。</span><span class="sxs-lookup"><span data-stu-id="9260d-133">For more information see [Codec Features](codec-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9260d-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="9260d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9260d-135">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="9260d-135">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="9260d-136">**設計設定檔**</span><span class="sxs-lookup"><span data-stu-id="9260d-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 





