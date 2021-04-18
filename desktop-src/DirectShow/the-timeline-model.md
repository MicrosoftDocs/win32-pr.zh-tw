---
description: 時間軸模型
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: 時間軸模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558118"
---
# <a name="the-timeline-model"></a><span data-ttu-id="20037-103">時間軸模型</span><span class="sxs-lookup"><span data-stu-id="20037-103">The Timeline Model</span></span>

<span data-ttu-id="20037-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="20037-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="20037-105">*時間軸* 是一種物件，可 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 用來代表影片編輯專案。</span><span class="sxs-lookup"><span data-stu-id="20037-105">A *timeline* is an object that [DirectShow Editing Services](directshow-editing-services.md) (DES) uses to represent a video editing project.</span></span> <span data-ttu-id="20037-106">編輯專案會以來源剪輯集合的形式啟動，其取自影片檔案、音效檔或仍為影像檔案。</span><span class="sxs-lookup"><span data-stu-id="20037-106">An editing project starts as a collection of source clips, taken from video files, sound files, or still image files.</span></span> <span data-ttu-id="20037-107">剪輯的線性序列會形成 *軌跡*。在 [DirectShow 編輯服務 (DES) 中，音訊和影片都會放在不同的曲目中。</span><span class="sxs-lookup"><span data-stu-id="20037-107">A linear sequence of clips forms a *track*. In DirectShow Editing Services (DES), audio and video are placed in separate tracks.</span></span>

<span data-ttu-id="20037-108">曲目也可以分層。</span><span class="sxs-lookup"><span data-stu-id="20037-108">Tracks can also be layered.</span></span> <span data-ttu-id="20037-109">多個音訊曲目會混合在一起，而且可能包含音訊效果，例如淡化或回音。</span><span class="sxs-lookup"><span data-stu-id="20037-109">Multiple audio tracks are mixed together, and might include audio effects, such as fades or reverb.</span></span> <span data-ttu-id="20037-110">使用多個影片曲目來建立轉換。</span><span class="sxs-lookup"><span data-stu-id="20037-110">Multiple video tracks are used to create transitions.</span></span> <span data-ttu-id="20037-111">例如，您可以建立從一個剪輯到另一個剪輯的抹除。</span><span class="sxs-lookup"><span data-stu-id="20037-111">For example, you can create a wipe from one clip to another.</span></span> <span data-ttu-id="20037-112">另一個範例是色度鍵，其中一個剪輯的背景會以不同的播放軌來進行索引。 (satelite 影像前面的氣象預測器是一種色度加密範例。 ) </span><span class="sxs-lookup"><span data-stu-id="20037-112">Another example is a chroma key, in which the background of one clip is keyed out and replaced by a different track. (The weather forecaster in front of a satelite image is an example of chroma keying.)</span></span>

<span data-ttu-id="20037-113">DES 使用樹狀結構來代表編輯：</span><span class="sxs-lookup"><span data-stu-id="20037-113">DES uses a tree structure to represent an editing:</span></span>

-   <span data-ttu-id="20037-114">音訊和影片剪輯會形成分葉節點或 *來源* 物件。</span><span class="sxs-lookup"><span data-stu-id="20037-114">Audio and video clips form the leaf nodes, or *source* objects.</span></span>
-   <span data-ttu-id="20037-115">具有統一媒體類型 (音訊或影片) 的來源集合是一份播放 *軌*。</span><span class="sxs-lookup"><span data-stu-id="20037-115">A collection of sources with a uniform media type (audio or video) is a *track*.</span></span>
-   <span data-ttu-id="20037-116">追蹤的集合是 *組合*。</span><span class="sxs-lookup"><span data-stu-id="20037-116">A collection of tracks is a *composition*.</span></span> <span data-ttu-id="20037-117">組合會轉譯成它所包含之所有追蹤的複合。</span><span class="sxs-lookup"><span data-stu-id="20037-117">A composition is rendered as the composite of all the tracks it contains.</span></span> <span data-ttu-id="20037-118">組合可以包含其他組合，以允許追蹤的複雜排列。</span><span class="sxs-lookup"><span data-stu-id="20037-118">Compositions can contain other compositions, which allows for complex arrangements of tracks.</span></span>
-   <span data-ttu-id="20037-119">組合的最上層集合和追蹤 (全都代表相同的媒體類型) 為 *群組*。</span><span class="sxs-lookup"><span data-stu-id="20037-119">A top-level collection of compositions and tracks (all representing the same media type) is a *group*.</span></span>
-   <span data-ttu-id="20037-120">一或多個群組形成 *時間軸*。</span><span class="sxs-lookup"><span data-stu-id="20037-120">A set of one or more groups forms a *timeline*.</span></span> <span data-ttu-id="20037-121">時間軸是樹狀結構中的根節點。</span><span class="sxs-lookup"><span data-stu-id="20037-121">The timeline is the root node in the tree.</span></span>

<span data-ttu-id="20037-122">時間軸必須包含至少一個群組。</span><span class="sxs-lookup"><span data-stu-id="20037-122">A timeline must contain at least one group.</span></span> <span data-ttu-id="20037-123">每個群組都代表最終生產環境中的單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="20037-123">Each group represents a single stream in the final production.</span></span> <span data-ttu-id="20037-124">一般專案包含一個影片群組和一個音訊群組。</span><span class="sxs-lookup"><span data-stu-id="20037-124">A typical project includes one video group and one audio group.</span></span> <span data-ttu-id="20037-125">組合是選擇性的;如果有需要，則會提供更多結構。</span><span class="sxs-lookup"><span data-stu-id="20037-125">Compositions are optional; they exist to provide more structure if needed.</span></span>

<span data-ttu-id="20037-126">下圖顯示組成時間軸的子父代關聯性：</span><span class="sxs-lookup"><span data-stu-id="20037-126">The following illustration shows the child-parent relations that make up a timeline:</span></span>

![節點結構](images/timeline1.png)

<span data-ttu-id="20037-128">以下顯示時間軸作為時態順序：</span><span class="sxs-lookup"><span data-stu-id="20037-128">The following shows a timeline as a temporal sequence:</span></span>

![時間軸圖例](images/timeline2.png)

<span data-ttu-id="20037-130">頂端的箭號代表時間軸的方向，從零開始。</span><span class="sxs-lookup"><span data-stu-id="20037-130">The arrow at the top represents the direction of the timeline, starting from time zero.</span></span> <span data-ttu-id="20037-131">在「影片」群組中，「追蹤1」的優先順序高於「追蹤0」。</span><span class="sxs-lookup"><span data-stu-id="20037-131">Within the video group, track 1 has a higher priority than track 0.</span></span> <span data-ttu-id="20037-132">追蹤1中的來源物件會遮蔽追蹤0中的來源物件。</span><span class="sxs-lookup"><span data-stu-id="20037-132">The source objects in track 1 obscure those in track 0.</span></span> <span data-ttu-id="20037-133">其中的 track 1 是空的，track 0 「顯示于」。</span><span class="sxs-lookup"><span data-stu-id="20037-133">Where track 1 is empty, track 0 "shows through."</span></span> <span data-ttu-id="20037-134">如先前所述，曲目只會一起混合在一起。</span><span class="sxs-lookup"><span data-stu-id="20037-134">As mentioned earlier, audio tracks are simply mixed together.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20037-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="20037-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20037-136">使用 DirectShow 編輯服務開始使用</span><span class="sxs-lookup"><span data-stu-id="20037-136">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="20037-137">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="20037-137">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



