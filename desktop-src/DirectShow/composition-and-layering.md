---
description: 撰寫和分層
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: 撰寫和分層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967005"
---
# <a name="composition-and-layering"></a><span data-ttu-id="b328f-103">撰寫和分層</span><span class="sxs-lookup"><span data-stu-id="b328f-103">Composition and Layering</span></span>

<span data-ttu-id="b328f-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b328f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b328f-105">在一組追蹤的集合中，第一個軌的優先順序最低 (優先順序 0) ，而且每個後續的播放軌都有一個較高的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="b328f-105">In a collection of tracks, the first track has the lowest priority (priority 0) and each subsequent track has a priority one level higher.</span></span> <span data-ttu-id="b328f-106">在每個優先權層級，該追蹤中的來源剪輯會隱藏其下追蹤中的來源剪輯，除非該圖層也包含轉換。</span><span class="sxs-lookup"><span data-stu-id="b328f-106">At each priority level, the source clips in that track hide the source clips in the tracks below it, unless that layer also contains a transition.</span></span> <span data-ttu-id="b328f-107">因此，您可以想像 DES 在轉譯時進行數次傳遞。</span><span class="sxs-lookup"><span data-stu-id="b328f-107">Thus you can imagine DES making several passes when it renders.</span></span>

<span data-ttu-id="b328f-108">首先，它會呈現 track 0。</span><span class="sxs-lookup"><span data-stu-id="b328f-108">First, it renders track 0.</span></span> <span data-ttu-id="b328f-109">在「追蹤0」底下沒有任何專案，因此空白區域會轉譯為實心黑色影像。</span><span class="sxs-lookup"><span data-stu-id="b328f-109">There is nothing "under" Track 0, so empty regions are rendered as a solid black image.</span></span> <span data-ttu-id="b328f-110">此圖層中的轉換會在黑色影像和軌0之間進行，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b328f-110">Transitions in this layer occur between the black image and track 0 or vice versa.</span></span> <span data-ttu-id="b328f-111">DES 會在曲目0的上方配置追蹤1，在兩個曲目之間產生任何轉換。</span><span class="sxs-lookup"><span data-stu-id="b328f-111">DES lays track 1 on top of track 0, generating any transitions between the two tracks.</span></span> <span data-ttu-id="b328f-112">結果就是兩個追蹤的複合。</span><span class="sxs-lookup"><span data-stu-id="b328f-112">The result is the composite of the two tracks.</span></span> <span data-ttu-id="b328f-113">接下來，它會將追蹤2放到這個複合。</span><span class="sxs-lookup"><span data-stu-id="b328f-113">Next, it places track 2 onto this composite.</span></span> <span data-ttu-id="b328f-114">這一層的轉換會在複合和 track 2 之間進行。</span><span class="sxs-lookup"><span data-stu-id="b328f-114">Transitions at this layer occur between the composite and track 2.</span></span> <span data-ttu-id="b328f-115">此程式會繼續進行，直到最後一個 (最高優先順序的) 追蹤為止。</span><span class="sxs-lookup"><span data-stu-id="b328f-115">The process continues until the last (highest-priority) track is put down.</span></span>

<span data-ttu-id="b328f-116">當有多個追蹤組合在一起時，它們的行為就像是單一追蹤 (稱為「虛擬追蹤) 」。</span><span class="sxs-lookup"><span data-stu-id="b328f-116">When several tracks are composited together, they behave like a single track (called a virtual track).</span></span> <span data-ttu-id="b328f-117">組合物件會封裝此行為，因此可以進行複雜的轉換。</span><span class="sxs-lookup"><span data-stu-id="b328f-117">The composition object encapsulates this behavior, making complex transitions possible.</span></span> <span data-ttu-id="b328f-118">例如，一個影片剪輯可以抹除至第二個剪輯，而複合 (兩個剪輯加上抹除) 淡化為第三個剪輯。</span><span class="sxs-lookup"><span data-stu-id="b328f-118">For example, one video clip can wipe to a second clip, while the composite (both clips plus the wipe) fades to a third clip.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b328f-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b328f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b328f-120">使用 DirectShow 編輯服務開始使用</span><span class="sxs-lookup"><span data-stu-id="b328f-120">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



