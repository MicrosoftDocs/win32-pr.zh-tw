---
description: 轉換
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: 轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852147"
---
# <a name="transitions"></a><span data-ttu-id="150ba-103">轉換</span><span class="sxs-lookup"><span data-stu-id="150ba-103">Transitions</span></span>

<span data-ttu-id="150ba-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="150ba-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="150ba-105">轉換是一種從某個影片播放軌 segue 至另一個影片播放軌的方式，使用淡出或抹除等視覺效果。</span><span class="sxs-lookup"><span data-stu-id="150ba-105">A transition is a way to segue from one video track to another, using a visual effect such as a fade or a wipe.</span></span> <span data-ttu-id="150ba-106">下圖顯示具有轉換的時程表：</span><span class="sxs-lookup"><span data-stu-id="150ba-106">The following illustration shows a timeline with a transition:</span></span>

![具有轉換的時程表](images/timeline3.png)

<span data-ttu-id="150ba-108">轉換物件是在 track 1，它代表從 track 0 到 track 1 的轉換。</span><span class="sxs-lookup"><span data-stu-id="150ba-108">The transition object is on track 1, and it represents a transition from track 0 to track 1.</span></span> <span data-ttu-id="150ba-109">在轉換開始時，轉譯的影片完全取自追蹤 0 (來源 A) 。</span><span class="sxs-lookup"><span data-stu-id="150ba-109">At the start of the transition, the rendered video is entirely from Track 0 (source A).</span></span> <span data-ttu-id="150ba-110">最後，影片完全取自追蹤 1 (來源 C) 。</span><span class="sxs-lookup"><span data-stu-id="150ba-110">At the end, the video is entirely from Track 1 (source C).</span></span> <span data-ttu-id="150ba-111">從開始，輸出會從來源 A 轉換成來源 C。例如，在淡化轉換中，有一個來源會逐漸淡化為另一個來源。</span><span class="sxs-lookup"><span data-stu-id="150ba-111">In between, the output transitions from source A to source C. For example, in a fade transition, one source progressively fades to the other.</span></span> <span data-ttu-id="150ba-112">最後的輸出會沿著圖底部架構化。</span><span class="sxs-lookup"><span data-stu-id="150ba-112">The final output is schematized along the bottom of the illustration.</span></span>

<span data-ttu-id="150ba-113">轉換無法在相同的播放軌內重迭，但您可以使用組合物件建立重迭的轉換，如 [撰寫和分層](composition-and-layering.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="150ba-113">Transitions cannot overlap in time within the same track, but you can create overlapping transitions by using the composition object, as described in [Composition and Layering](composition-and-layering.md).</span></span>

<span data-ttu-id="150ba-114">轉換有方向。</span><span class="sxs-lookup"><span data-stu-id="150ba-114">A transition has a direction.</span></span> <span data-ttu-id="150ba-115">根據預設，它會從較低優先順序的追蹤開始， (來源 A （在先前的範例中）。 ) ，並以較高優先順序的播放軌 (來源 C) 。</span><span class="sxs-lookup"><span data-stu-id="150ba-115">By default, it starts from the lower priority track (source A, in the previous example.) and ends at the higher-priority track (source C).</span></span> <span data-ttu-id="150ba-116">在兩者之間，影片是兩個來源的混合。</span><span class="sxs-lookup"><span data-stu-id="150ba-116">In between, the video is a mixture of the two sources.</span></span> <span data-ttu-id="150ba-117">不過，您可以指定相對的行為，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="150ba-117">However, you can specify the opposite behavior, as shown in the following illustration:</span></span>

![具有兩個轉換的 ntrack](images/fade.png)

<span data-ttu-id="150ba-119">在這裡，第一個轉換會淡出曲目0淡化 track 1，這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="150ba-119">Here, the first transition fades from track 0 fades track 1, which is the default behavior.</span></span> <span data-ttu-id="150ba-120">第二個轉換會從曲目1淡回以追蹤0。</span><span class="sxs-lookup"><span data-stu-id="150ba-120">The second transition fades from track 1 back to Track 0.</span></span> <span data-ttu-id="150ba-121">請注意，這兩個轉換都位於曲目1上。</span><span class="sxs-lookup"><span data-stu-id="150ba-121">Note that both transitions are located on track 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="150ba-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="150ba-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="150ba-123">使用 DirectShow 編輯服務開始使用</span><span class="sxs-lookup"><span data-stu-id="150ba-123">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="150ba-124">轉換和效果</span><span class="sxs-lookup"><span data-stu-id="150ba-124">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> <dt>

[<span data-ttu-id="150ba-125">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="150ba-125">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



