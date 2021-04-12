---
description: 預覽效果和轉換
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: 預覽效果和轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109553"
---
# <a name="previewing-effects-and-transitions"></a><span data-ttu-id="e7bff-103">預覽效果和轉換</span><span class="sxs-lookup"><span data-stu-id="e7bff-103">Previewing Effects and Transitions</span></span>

<span data-ttu-id="e7bff-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e7bff-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e7bff-105">某些效果和轉換需要相對較長的時間才能呈現。</span><span class="sxs-lookup"><span data-stu-id="e7bff-105">Some effects and transitions take a relatively long time to render.</span></span> <span data-ttu-id="e7bff-106">在預覽期間，這可能會導致影片不穩定或與音訊同步。</span><span class="sxs-lookup"><span data-stu-id="e7bff-106">During preview this can cause the video to become choppy or out of sync with the audio.</span></span> <span data-ttu-id="e7bff-107">您可以停用效果或轉換來提高預覽速度：</span><span class="sxs-lookup"><span data-stu-id="e7bff-107">You can increase preview speed by disabling effects or transitions:</span></span>

-   <span data-ttu-id="e7bff-108">若要停用所有效果，請呼叫 [**IAMTimeline：： EnableEffects**](iamtimeline-enableeffects.md)。</span><span class="sxs-lookup"><span data-stu-id="e7bff-108">To disable all effects, call [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).</span></span>
-   <span data-ttu-id="e7bff-109">若要停用所有轉換，請呼叫 [**IAMTimeline：： EnableTransitions**](iamtimeline-enabletransitions.md)。</span><span class="sxs-lookup"><span data-stu-id="e7bff-109">To disable all transitions, call [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).</span></span>
-   <span data-ttu-id="e7bff-110">若要停用特定轉換，請呼叫 [**IAMTimelineTrans：： SetCutsOnly**](iamtimelinetrans-setcutsonly.md)。</span><span class="sxs-lookup"><span data-stu-id="e7bff-110">To disable a particular transition, call [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span></span>

<span data-ttu-id="e7bff-111">當效果停用時，不會在預覽期間轉譯。</span><span class="sxs-lookup"><span data-stu-id="e7bff-111">When effects are disabled, they are not rendered during preview.</span></span> <span data-ttu-id="e7bff-112">當轉換停用時，它會轉譯為跳躍點剪下。</span><span class="sxs-lookup"><span data-stu-id="e7bff-112">When a transition is disabled, it is rendered as a jump cut.</span></span> <span data-ttu-id="e7bff-113">Segue 之間仍會進行追蹤，但不會轉譯視覺效果。</span><span class="sxs-lookup"><span data-stu-id="e7bff-113">The segue between tracks still occurs, but the visual effect is not rendered.</span></span>

<span data-ttu-id="e7bff-114">如果無法轉譯效果或轉換，轉譯引擎會替代預設效果或轉換。</span><span class="sxs-lookup"><span data-stu-id="e7bff-114">If an effect or transition cannot be rendered, the render engine substitutes a default effect or transition.</span></span> <span data-ttu-id="e7bff-115">呼叫 [**IAMTimeline：： SetDefaultEffect**](iamtimeline-setdefaulteffect.md) 方法來設定預設效果，並呼叫 [**IAMTimeline：： SetDefaultTransition**](iamtimeline-setdefaulttransition.md) 方法來設定預設轉換。</span><span class="sxs-lookup"><span data-stu-id="e7bff-115">Call the [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) method to set the default effect, and the [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) method to set the default transition.</span></span> <span data-ttu-id="e7bff-116">如果您未指定預設值，或您指定的也會造成錯誤，DES 會使用它自己的預設值。</span><span class="sxs-lookup"><span data-stu-id="e7bff-116">If you do not specify a default, or if the one you specify also causes an error, DES uses its own default.</span></span>

> [!Note]  
> <span data-ttu-id="e7bff-117">您也可以藉由增加框架緩衝量來改善預覽品質。</span><span class="sxs-lookup"><span data-stu-id="e7bff-117">You can also improve preview quality by increasing the amount of frame buffering.</span></span> <span data-ttu-id="e7bff-118">請參閱 [**IAMTimelineGroup：： SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)。</span><span class="sxs-lookup"><span data-stu-id="e7bff-118">See [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e7bff-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7bff-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7bff-120">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="e7bff-120">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



