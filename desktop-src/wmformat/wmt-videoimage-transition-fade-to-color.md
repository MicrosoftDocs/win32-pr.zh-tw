---
title: 'WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl) '
description: 淡化至色彩的轉換是從影像溶解到純色的框架。
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR windows Media 格式
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000777"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a><span data-ttu-id="1df2d-104">WMT \_ VIDEOIMAGE \_ 轉換 \_ 淡化 \_ 成 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="1df2d-104">WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR</span></span>

<span data-ttu-id="1df2d-105">淡化至色彩的轉換是從影像溶解到純色的框架。</span><span class="sxs-lookup"><span data-stu-id="1df2d-105">The fade-to-color transition dissolves from the image to a frame of solid color.</span></span>

## <a name="parameters"></a><span data-ttu-id="1df2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1df2d-106">Parameters</span></span>

<span data-ttu-id="1df2d-107">下表描述此轉換所使用的參數，並列出指派給它們的 [**WMT \_ VIDEOIMAGE \_ sample2.xml**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="1df2d-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



| <span data-ttu-id="1df2d-108">參數</span><span class="sxs-lookup"><span data-stu-id="1df2d-108">Parameter</span></span>         | <span data-ttu-id="1df2d-109">結構成員</span><span class="sxs-lookup"><span data-stu-id="1df2d-109">Structure member</span></span> | <span data-ttu-id="1df2d-110">Description</span><span class="sxs-lookup"><span data-stu-id="1df2d-110">Description</span></span>                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df2d-111">紅色</span><span class="sxs-lookup"><span data-stu-id="1df2d-111">Red</span></span>               | <span data-ttu-id="1df2d-112">**fEffectPara0**</span><span class="sxs-lookup"><span data-stu-id="1df2d-112">**fEffectPara0**</span></span> | <span data-ttu-id="1df2d-113">背景色彩的紅色值。</span><span class="sxs-lookup"><span data-stu-id="1df2d-113">Red value of the background color.</span></span> <span data-ttu-id="1df2d-114">設定為介於0和255之間的數位。</span><span class="sxs-lookup"><span data-stu-id="1df2d-114">Set to a number between 0 and 255.</span></span>                                                                                                                                                     |
| <span data-ttu-id="1df2d-115">綠色</span><span class="sxs-lookup"><span data-stu-id="1df2d-115">Green</span></span>             | <span data-ttu-id="1df2d-116">**fEffectPara1**</span><span class="sxs-lookup"><span data-stu-id="1df2d-116">**fEffectPara1**</span></span> | <span data-ttu-id="1df2d-117">背景色彩的綠色值。</span><span class="sxs-lookup"><span data-stu-id="1df2d-117">Green value of the background color.</span></span> <span data-ttu-id="1df2d-118">設定為介於0和255之間的數位。</span><span class="sxs-lookup"><span data-stu-id="1df2d-118">Set to a number between 0 and 255.</span></span>                                                                                                                                                   |
| <span data-ttu-id="1df2d-119">藍色</span><span class="sxs-lookup"><span data-stu-id="1df2d-119">Blue</span></span>              | <span data-ttu-id="1df2d-120">**fEffectPara2**</span><span class="sxs-lookup"><span data-stu-id="1df2d-120">**fEffectPara2**</span></span> | <span data-ttu-id="1df2d-121">背景色彩的藍色值。</span><span class="sxs-lookup"><span data-stu-id="1df2d-121">Blue value of the background color.</span></span> <span data-ttu-id="1df2d-122">設定為介於0和255之間的數位。</span><span class="sxs-lookup"><span data-stu-id="1df2d-122">Set to a number between 0 and 255.</span></span>                                                                                                                                                    |
| <span data-ttu-id="1df2d-123">背景權數</span><span class="sxs-lookup"><span data-stu-id="1df2d-123">Background weight</span></span> | <span data-ttu-id="1df2d-124">**fEffectPara3**</span><span class="sxs-lookup"><span data-stu-id="1df2d-124">**fEffectPara3**</span></span> | <span data-ttu-id="1df2d-125">背景色彩的加權。</span><span class="sxs-lookup"><span data-stu-id="1df2d-125">Weight of the background color.</span></span> <span data-ttu-id="1df2d-126">此參數會將混合中的背景色彩百分比表示為小數。</span><span class="sxs-lookup"><span data-stu-id="1df2d-126">This parameter expresses the percentage of the background color in the mix as a decimal.</span></span> <span data-ttu-id="1df2d-127">例如，若要將背景色彩 blend 為30%，請將影像70% 的混合設定為0.30。</span><span class="sxs-lookup"><span data-stu-id="1df2d-127">For example, to blend the background color at 30%, making the image 70% of the mix, set to 0.30.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1df2d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1df2d-128">Requirements</span></span>



| <span data-ttu-id="1df2d-129">需求</span><span class="sxs-lookup"><span data-stu-id="1df2d-129">Requirement</span></span> | <span data-ttu-id="1df2d-130">值</span><span class="sxs-lookup"><span data-stu-id="1df2d-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1df2d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="1df2d-131">Header</span></span><br/> | <dl> <span data-ttu-id="1df2d-132"><dt>Wmsdkidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1df2d-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df2d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1df2d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df2d-134">**影片影像轉換**</span><span class="sxs-lookup"><span data-stu-id="1df2d-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





