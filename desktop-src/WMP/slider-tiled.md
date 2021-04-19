---
title: 滑杆。磚
description: 並排顯示的屬性會指定或抓取值，指出是否要將滑杆影像並排顯示。
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- 滑杆。磚 Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987124"
---
# <a name="slidertiled"></a><span data-ttu-id="b02b1-104">滑杆。磚</span><span class="sxs-lookup"><span data-stu-id="b02b1-104">SLIDER.tiled</span></span>

<span data-ttu-id="b02b1-105">並排顯示 **的屬性會** 指定或抓取值，指出是否要將滑杆影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="b02b1-105">The **tiled** attribute specifies or retrieves a value indicating whether the slider image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="b02b1-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="b02b1-106">Possible Values</span></span>

<span data-ttu-id="b02b1-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="b02b1-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b02b1-108">值</span><span class="sxs-lookup"><span data-stu-id="b02b1-108">Value</span></span> | <span data-ttu-id="b02b1-109">描述</span><span class="sxs-lookup"><span data-stu-id="b02b1-109">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02b1-110">true</span><span class="sxs-lookup"><span data-stu-id="b02b1-110">true</span></span>  | <span data-ttu-id="b02b1-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="b02b1-111">Default.</span></span> <span data-ttu-id="b02b1-112">影像點陣圖會重複，直到填滿控制項的整個區域為止。</span><span class="sxs-lookup"><span data-stu-id="b02b1-112">The image bitmap will be repeated until it fills the entire region of the control.</span></span> |
| <span data-ttu-id="b02b1-113">false</span><span class="sxs-lookup"><span data-stu-id="b02b1-113">false</span></span> | <span data-ttu-id="b02b1-114">影像將不會並排顯示。</span><span class="sxs-lookup"><span data-stu-id="b02b1-114">The image will not be tiled.</span></span>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="b02b1-115">備註</span><span class="sxs-lookup"><span data-stu-id="b02b1-115">Remarks</span></span>

<span data-ttu-id="b02b1-116">只有當您使用前景和背景影像來定義滑杆控制項時，才適用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b02b1-116">This attribute applies only if you are using foreground and background images to define a slider control.</span></span> <span data-ttu-id="b02b1-117">如果影像小於滑杆的定義區域，而且 **已將並排顯示的** 屬性設為 true，則影像將會重複，直到填滿控制項的整個長度為止。</span><span class="sxs-lookup"><span data-stu-id="b02b1-117">If the images are smaller than the defined area of the slider, and the **tiled** attribute is set to true, the images will be repeated until they fill the entire length of the control.</span></span>

<span data-ttu-id="b02b1-118">您可能會想要搭配使用此屬性與 **borderSize** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b02b1-118">You may wish to use this attribute in conjunction with the **borderSize** attribute.</span></span> <span data-ttu-id="b02b1-119">**BorderSize** 屬性可讓您定義在平鋪期間不重複的框線。</span><span class="sxs-lookup"><span data-stu-id="b02b1-119">The **borderSize** attribute allows you to define a border that is not repeated during tiling.</span></span>

## <a name="requirements"></a><span data-ttu-id="b02b1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b02b1-120">Requirements</span></span>



| <span data-ttu-id="b02b1-121">需求</span><span class="sxs-lookup"><span data-stu-id="b02b1-121">Requirement</span></span> | <span data-ttu-id="b02b1-122">值</span><span class="sxs-lookup"><span data-stu-id="b02b1-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b02b1-123">版本</span><span class="sxs-lookup"><span data-stu-id="b02b1-123">Version</span></span><br/> | <span data-ttu-id="b02b1-124">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b02b1-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b02b1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b02b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02b1-126">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="b02b1-126">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="b02b1-127">**滑杆. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="b02b1-127">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="b02b1-128">**滑杆. borderSize**</span><span class="sxs-lookup"><span data-stu-id="b02b1-128">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="b02b1-129">**滑杆. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="b02b1-129">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





