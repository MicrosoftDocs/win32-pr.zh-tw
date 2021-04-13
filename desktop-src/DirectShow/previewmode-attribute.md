---
description: Previewmode 屬性會指定群組的預覽模式。 如果此值為 TRUE，則框架可能會在預覽期間中斷。 否則，預覽期間不會卸載任何框架。 預設值為 TRUE。
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: previewmode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385695"
---
# <a name="previewmode-attribute"></a><span data-ttu-id="970ee-106">previewmode 屬性</span><span class="sxs-lookup"><span data-stu-id="970ee-106">previewmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="970ee-107">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="970ee-107">\[Deprecated.</span></span> <span data-ttu-id="970ee-108">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="970ee-108">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="970ee-109">`previewmode`屬性會指定群組的預覽模式。</span><span class="sxs-lookup"><span data-stu-id="970ee-109">The `previewmode` attribute specifies the preview mode for the group.</span></span> <span data-ttu-id="970ee-110">如果此值為 **TRUE**，則框架可能會在預覽期間中斷。</span><span class="sxs-lookup"><span data-stu-id="970ee-110">If the value is **TRUE**, frames might be dropped during preview.</span></span> <span data-ttu-id="970ee-111">否則，預覽期間不會卸載任何框架。</span><span class="sxs-lookup"><span data-stu-id="970ee-111">Otherwise, no frames are dropped during preview.</span></span> <span data-ttu-id="970ee-112">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="970ee-112">The default value is **TRUE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="970ee-113">可能的值</span><span class="sxs-lookup"><span data-stu-id="970ee-113">Possible Values</span></span>

<span data-ttu-id="970ee-114">下列值定義為 TRUE： y、Y、t、T、1。</span><span class="sxs-lookup"><span data-stu-id="970ee-114">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="970ee-115">下列值定義為 FALSE： n、N、f、F、0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="970ee-115">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="970ee-116">套用至</span><span class="sxs-lookup"><span data-stu-id="970ee-116">Applies To</span></span>

[<span data-ttu-id="970ee-117">**組**</span><span class="sxs-lookup"><span data-stu-id="970ee-117">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="970ee-118">備註</span><span class="sxs-lookup"><span data-stu-id="970ee-118">Remarks</span></span>

<span data-ttu-id="970ee-119">在預設設定下，預覽緩慢效果或轉換時，會卸載框架，讓影片與音訊保持同步。</span><span class="sxs-lookup"><span data-stu-id="970ee-119">Under the default setting, frames are dropped while previewing slow effects or transitions, to keep the video synchronized with the audio.</span></span> <span data-ttu-id="970ee-120">這樣的影片看起來可能不穩定。</span><span class="sxs-lookup"><span data-stu-id="970ee-120">The video might look choppy as a result.</span></span> <span data-ttu-id="970ee-121">將此屬性設定為 **FALSE** ，會強制每個框架在預覽期間轉譯，可能導致影片與音訊同步。</span><span class="sxs-lookup"><span data-stu-id="970ee-121">Setting this attribute to **FALSE** forces every frame to render during preview, possibly resulting in the video becoming out of sync with the audio.</span></span> <span data-ttu-id="970ee-122">寫入檔案時，不會卸載框架。</span><span class="sxs-lookup"><span data-stu-id="970ee-122">Frames are never dropped when writing to a file.</span></span>

## <a name="see-also"></a><span data-ttu-id="970ee-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="970ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970ee-124">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="970ee-124">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="970ee-125">**IAMTimelineGroup::SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="970ee-125">**IAMTimelineGroup::SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



