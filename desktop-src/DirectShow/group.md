---
description: Group
ms.assetid: d1391664-df1d-4b2f-9625-d3be09cc1110
title: '群組 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed716c9e2564273db20afb7a21b40fe2ff56a83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509772"
---
# <a name="group-directshow"></a><span data-ttu-id="c550d-103">群組 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="c550d-103">Group (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="c550d-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c550d-104">\[Deprecated.</span></span> <span data-ttu-id="c550d-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c550d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c550d-106">群組物件代表最上層的組合。</span><span class="sxs-lookup"><span data-stu-id="c550d-106">The group object represents a top-level composition.</span></span> <span data-ttu-id="c550d-107">每個群組會在最後一個專案中定義一個影片或音訊串流。</span><span class="sxs-lookup"><span data-stu-id="c550d-107">Each group defines one video or audio stream in the final project.</span></span> <span data-ttu-id="c550d-108">若要建立這個物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c550d-108">To create this object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

<span data-ttu-id="c550d-109">群組物件會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="c550d-109">The group object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="c550d-110">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="c550d-110">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)
-   [<span data-ttu-id="c550d-111">**IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="c550d-111">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)
-   [<span data-ttu-id="c550d-112">**IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="c550d-112">**IAMTimelineObj**</span></span>](iamtimelineobj.md)

## <a name="related-topics"></a><span data-ttu-id="c550d-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="c550d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c550d-114">時間軸模型</span><span class="sxs-lookup"><span data-stu-id="c550d-114">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="c550d-115">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="c550d-115">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



