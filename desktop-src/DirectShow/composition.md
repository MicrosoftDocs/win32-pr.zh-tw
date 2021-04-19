---
description: Composition
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972922"
---
# <a name="composition"></a><span data-ttu-id="156c6-103">Composition</span><span class="sxs-lookup"><span data-stu-id="156c6-103">Composition</span></span>

> [!Note]  
> <span data-ttu-id="156c6-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="156c6-104">\[Deprecated.</span></span> <span data-ttu-id="156c6-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="156c6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="156c6-106">組合物件是用於追蹤的容器。</span><span class="sxs-lookup"><span data-stu-id="156c6-106">The composition object is a container for tracks.</span></span> <span data-ttu-id="156c6-107">它也可以保存追蹤的其他組合 () 、效果和轉換。</span><span class="sxs-lookup"><span data-stu-id="156c6-107">It can also hold other compositions (for nesting of tracks), effects, and transitions.</span></span> <span data-ttu-id="156c6-108">若要建立這個物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="156c6-108">To create this object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

<span data-ttu-id="156c6-109">組合物件會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="156c6-109">The composition object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="156c6-110">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="156c6-110">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)
-   [<span data-ttu-id="156c6-111">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="156c6-111">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)
-   [<span data-ttu-id="156c6-112">**IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="156c6-112">**IAMTimelineObj**</span></span>](iamtimelineobj.md)
-   [<span data-ttu-id="156c6-113">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="156c6-113">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)
-   [<span data-ttu-id="156c6-114">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="156c6-114">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a><span data-ttu-id="156c6-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="156c6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="156c6-116">時間軸模型</span><span class="sxs-lookup"><span data-stu-id="156c6-116">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="156c6-117">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="156c6-117">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



