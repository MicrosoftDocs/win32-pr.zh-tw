---
title: 滑杆. backgroundColor
description: BackgroundColor 屬性會指定或抓取滑杆控制項的背景色彩。
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- BackgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986191"
---
# <a name="sliderbackgroundcolor"></a><span data-ttu-id="c1964-104">滑杆. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="c1964-104">SLIDER.backgroundColor</span></span>

<span data-ttu-id="c1964-105">**BackgroundColor** 屬性會指定或抓取滑杆控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="c1964-105">The **backgroundColor** attribute specifies or retrieves the background color of the slider control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="c1964-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="c1964-106">Possible Values</span></span>

<span data-ttu-id="c1964-107">這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="c1964-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="c1964-108">它沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="c1964-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1964-109">備註</span><span class="sxs-lookup"><span data-stu-id="c1964-109">Remarks</span></span>

<span data-ttu-id="c1964-110">您可以藉由指定 **backgroundColor** 或 **BackgroundImage**，以及 **foregroundColor** 或 **foregroundImage** 來建立基本滑杆控制項。</span><span class="sxs-lookup"><span data-stu-id="c1964-110">A basic slider control can be constructed by specifying **backgroundColor** or **backgroundImage**, and **foregroundColor** or **foregroundImage**.</span></span>

<span data-ttu-id="c1964-111">使用色彩時，滑杆控制項的維度會定義以背景色彩填滿的區域。</span><span class="sxs-lookup"><span data-stu-id="c1964-111">When using the colors, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="c1964-112">前景色彩會包含滑杆位置增加時的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="c1964-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="c1964-113">若要為背景或前景色彩所佔用的區域進行漸層填滿，請指定 **backgroundEndColor** 或 **foregroundEndColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c1964-113">To make a gradient fill of the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="c1964-114">請參閱 *CUSTOMSLIDER*。說明如何使用 **滑杆** 元素屬性之範例的 [positionImage](customslider-positionimage.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="c1964-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1964-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1964-115">Requirements</span></span>



| <span data-ttu-id="c1964-116">需求</span><span class="sxs-lookup"><span data-stu-id="c1964-116">Requirement</span></span> | <span data-ttu-id="c1964-117">值</span><span class="sxs-lookup"><span data-stu-id="c1964-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c1964-118">版本</span><span class="sxs-lookup"><span data-stu-id="c1964-118">Version</span></span><br/> | <span data-ttu-id="c1964-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1964-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1964-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1964-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1964-121">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="c1964-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="c1964-122">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="c1964-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="c1964-123">**滑杆. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="c1964-123">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="c1964-124">**滑杆. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="c1964-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="c1964-125">**滑杆. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="c1964-125">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="c1964-126">**滑杆. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="c1964-126">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="c1964-127">**滑杆. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="c1964-127">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





