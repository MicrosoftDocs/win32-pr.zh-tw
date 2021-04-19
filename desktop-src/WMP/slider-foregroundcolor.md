---
title: 滑杆. foregroundColor
description: ForegroundColor 屬性會指定或抓取滑杆控制項的前景色彩。
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- ForegroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995054"
---
# <a name="sliderforegroundcolor"></a><span data-ttu-id="c795b-104">滑杆. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="c795b-104">SLIDER.foregroundColor</span></span>

<span data-ttu-id="c795b-105">**ForegroundColor** 屬性會指定或抓取滑杆控制項的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="c795b-105">The **foregroundColor** attribute specifies or retrieves the foreground color of the slider control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="c795b-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="c795b-106">Possible Values</span></span>

<span data-ttu-id="c795b-107">這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="c795b-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="c795b-108">預設值為 "白色"。</span><span class="sxs-lookup"><span data-stu-id="c795b-108">The default value is "white".</span></span>

## <a name="remarks"></a><span data-ttu-id="c795b-109">備註</span><span class="sxs-lookup"><span data-stu-id="c795b-109">Remarks</span></span>

<span data-ttu-id="c795b-110">您可以指定兩組屬性的其中一個來建立基本滑杆控制項： **backgroundColor** 和 **ForegroundColor**，或 **backgroundImage** 和 **foregroundImage**。</span><span class="sxs-lookup"><span data-stu-id="c795b-110">A basic slider control can be constructed by specifying one of two pairs of attributes: the **backgroundColor** and **foregroundColor**, or the **backgroundImage** and **foregroundImage**.</span></span>

<span data-ttu-id="c795b-111">當您使用 [色彩] 屬性來建立滑杆控制項時，滑杆控制項的維度會定義以背景色彩填滿的區域。</span><span class="sxs-lookup"><span data-stu-id="c795b-111">When you construct a slider control using the color attributes, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="c795b-112">前景色彩會包含滑杆位置增加時的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="c795b-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="c795b-113">若要將漸層填滿背景或前景色彩所佔用的區域，請指定 **backgroundEndColor** 或 **foregroundEndColor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c795b-113">To make a gradient fill in the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="c795b-114">請參閱 *CUSTOMSLIDER*。說明如何使用 **滑杆** 元素屬性之範例的 [positionImage](customslider-positionimage.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="c795b-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c795b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c795b-115">Requirements</span></span>



| <span data-ttu-id="c795b-116">需求</span><span class="sxs-lookup"><span data-stu-id="c795b-116">Requirement</span></span> | <span data-ttu-id="c795b-117">值</span><span class="sxs-lookup"><span data-stu-id="c795b-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c795b-118">版本</span><span class="sxs-lookup"><span data-stu-id="c795b-118">Version</span></span><br/> | <span data-ttu-id="c795b-119">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c795b-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c795b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c795b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c795b-121">**色彩參考**</span><span class="sxs-lookup"><span data-stu-id="c795b-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="c795b-122">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="c795b-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="c795b-123">**滑杆. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="c795b-123">**SLIDER.backgroundColor**</span></span>](slider-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="c795b-124">**滑杆. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="c795b-124">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="c795b-125">**滑杆. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="c795b-125">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="c795b-126">**滑杆. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="c795b-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





