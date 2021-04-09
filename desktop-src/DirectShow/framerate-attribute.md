---
description: 畫面播放速率屬性指定畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: " (DirectShow) 的畫面播放速率屬性"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935812"
---
# <a name="framerate-attribute-directshow"></a><span data-ttu-id="28a92-103"> (DirectShow) 的畫面播放速率屬性</span><span class="sxs-lookup"><span data-stu-id="28a92-103">framerate Attribute (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="28a92-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="28a92-104">\[Deprecated.</span></span> <span data-ttu-id="28a92-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="28a92-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="28a92-106">`framerate`屬性指定畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="28a92-106">The `framerate` attribute specifies a framerate, in frames per second.</span></span>

## <a name="possible-values"></a><span data-ttu-id="28a92-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="28a92-107">Possible Values</span></span>

<span data-ttu-id="28a92-108">浮點值。</span><span class="sxs-lookup"><span data-stu-id="28a92-108">Floating-point value.</span></span> <span data-ttu-id="28a92-109">值必須在小數點之前包含前置零。</span><span class="sxs-lookup"><span data-stu-id="28a92-109">The value must include the leading zero before the decimal place.</span></span> <span data-ttu-id="28a92-110">例如，0.3，而不是. 3。</span><span class="sxs-lookup"><span data-stu-id="28a92-110">For example, 0.3, not .3.</span></span> <span data-ttu-id="28a92-111">請勿使用超過7個小數位數。</span><span class="sxs-lookup"><span data-stu-id="28a92-111">Do not use more than seven decimal digits.</span></span>

## <a name="applies-to"></a><span data-ttu-id="28a92-112">套用至</span><span class="sxs-lookup"><span data-stu-id="28a92-112">Applies To</span></span>

<span data-ttu-id="28a92-113">[**剪輯**](clip-element.md)、 [**群組**](group-element.md)、 [**時間軸**](timeline-element.md)</span><span class="sxs-lookup"><span data-stu-id="28a92-113">[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)</span></span>

## <a name="remarks"></a><span data-ttu-id="28a92-114">備註</span><span class="sxs-lookup"><span data-stu-id="28a92-114">Remarks</span></span>

<span data-ttu-id="28a92-115">若為 **剪切** 元素，這個屬性會指定來源的預設畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="28a92-115">For the **clip** element, this attribute specifies the default frame rate of the source.</span></span> <span data-ttu-id="28a92-116">指定 [靜止影像 andDIB 順序] 的屬性。</span><span class="sxs-lookup"><span data-stu-id="28a92-116">Specify the attribute for still images andDIB sequences.</span></span> <span data-ttu-id="28a92-117">若為靜止影像，請將值設定為零。</span><span class="sxs-lookup"><span data-stu-id="28a92-117">For a still image, set the value to zero.</span></span> <span data-ttu-id="28a92-118">若為 DIB 順序，請使用非零值。</span><span class="sxs-lookup"><span data-stu-id="28a92-118">For a DIB sequence, use a nonzero value.</span></span> <span data-ttu-id="28a92-119">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="28a92-119">The default value is zero.</span></span>

<span data-ttu-id="28a92-120">針對 **群組** 專案，這個屬性會指定群組的輸出畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="28a92-120">For the **group** element, this attribute specifies the output frame rate for the group.</span></span>

<span data-ttu-id="28a92-121">若為 **時間軸** 元素，這個屬性會指定所有群組的預設畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="28a92-121">For the **timeline** element, this attribute specifies the default frame rate for all groups.</span></span>

## <a name="see-also"></a><span data-ttu-id="28a92-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28a92-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a92-123">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="28a92-123">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="28a92-124">**IAMTimelineSrc::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="28a92-124">**IAMTimelineSrc::SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[<span data-ttu-id="28a92-125">**IAMTimelineGroup::SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="28a92-125">**IAMTimelineGroup::SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[<span data-ttu-id="28a92-126">**IAMTimeline::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="28a92-126">**IAMTimeline::SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



