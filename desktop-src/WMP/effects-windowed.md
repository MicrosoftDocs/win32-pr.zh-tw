---
title: 效果。視窗化
description: 視窗型屬性會指定或抓取值，指出視覺效果是否為視窗化或無視窗，也就是控制項的整個矩形是否會在任何時間顯示，或是是否可以裁剪。
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- 效果。視窗化 Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984463"
---
# <a name="effectswindowed"></a><span data-ttu-id="abb1c-104">效果。視窗化</span><span class="sxs-lookup"><span data-stu-id="abb1c-104">EFFECTS.windowed</span></span>

<span data-ttu-id="abb1c-105">**視窗** 型屬性會指定或抓取值，指出視覺效果是否為視窗化或無視窗，也就是控制項的整個矩形是否會在任何時間顯示，或是是否可以裁剪。</span><span class="sxs-lookup"><span data-stu-id="abb1c-105">The **windowed** attribute specifies or retrieves a value indicating whether the visualization will be windowed or windowless, that is, whether the entire rectangle of the control will be visible at all times, or whether it can be clipped.</span></span> <span data-ttu-id="abb1c-106">這個屬性只能在設計階段設定。</span><span class="sxs-lookup"><span data-stu-id="abb1c-106">This attribute can only be set at design time.</span></span>

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a><span data-ttu-id="abb1c-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="abb1c-107">Possible Values</span></span>

<span data-ttu-id="abb1c-108">這個屬性是在設計階段指定的 **布林值** ，之後是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="abb1c-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="abb1c-109">值</span><span class="sxs-lookup"><span data-stu-id="abb1c-109">Value</span></span> | <span data-ttu-id="abb1c-110">描述</span><span class="sxs-lookup"><span data-stu-id="abb1c-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="abb1c-111">true</span><span class="sxs-lookup"><span data-stu-id="abb1c-111">true</span></span>  | <span data-ttu-id="abb1c-112">控制項將會是視窗化。</span><span class="sxs-lookup"><span data-stu-id="abb1c-112">The control will be windowed.</span></span>            |
| <span data-ttu-id="abb1c-113">false</span><span class="sxs-lookup"><span data-stu-id="abb1c-113">false</span></span> | <span data-ttu-id="abb1c-114">預設值。</span><span class="sxs-lookup"><span data-stu-id="abb1c-114">Default.</span></span> <span data-ttu-id="abb1c-115">控制項將會是無視窗的。</span><span class="sxs-lookup"><span data-stu-id="abb1c-115">The control will be windowless.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="abb1c-116">備註</span><span class="sxs-lookup"><span data-stu-id="abb1c-116">Remarks</span></span>

<span data-ttu-id="abb1c-117">如果需要非矩形的視覺效果視窗，或是任何部分的視窗包含在影像中，則此屬性必須設定為 false。</span><span class="sxs-lookup"><span data-stu-id="abb1c-117">If a non-rectangular visualization window is desired, or if any part of the window is covered by an image, this attribute must be set to false.</span></span> <span data-ttu-id="abb1c-118">這會犧牲一些執行必要裁剪的效能。</span><span class="sxs-lookup"><span data-stu-id="abb1c-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="abb1c-119">如果 **視窗** 設定為 true，則會忽略涵蓋視覺效果視窗的任何影像，而視覺效果視窗會具有最高層級的迭置順序。</span><span class="sxs-lookup"><span data-stu-id="abb1c-119">If **windowed** is set to true, any image covering the visualization window is ignored, and the visualization window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb1c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="abb1c-120">Requirements</span></span>



| <span data-ttu-id="abb1c-121">需求</span><span class="sxs-lookup"><span data-stu-id="abb1c-121">Requirement</span></span> | <span data-ttu-id="abb1c-122">值</span><span class="sxs-lookup"><span data-stu-id="abb1c-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="abb1c-123">版本</span><span class="sxs-lookup"><span data-stu-id="abb1c-123">Version</span></span><br/> | <span data-ttu-id="abb1c-124">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="abb1c-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abb1c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abb1c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb1c-126">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="abb1c-126">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





