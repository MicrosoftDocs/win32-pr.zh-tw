---
title: 滑杆. borderSize
description: BorderSize 屬性會指定或抓取框線寬度（以圖元為單位）。
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- BorderSize Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994155"
---
# <a name="sliderbordersize"></a><span data-ttu-id="24162-104">滑杆. borderSize</span><span class="sxs-lookup"><span data-stu-id="24162-104">SLIDER.borderSize</span></span>

<span data-ttu-id="24162-105">**BorderSize** 屬性會指定或抓取框線寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="24162-105">The **borderSize** attribute specifies or retrieves the border width in pixels.</span></span>

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a><span data-ttu-id="24162-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="24162-106">Possible Values</span></span>

<span data-ttu-id="24162-107">此屬性是讀取/寫入 **數位** (**長**) 表示框線寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="24162-107">This attribute is a read/write **Number** (**long**) representing the border width in pixels.</span></span> <span data-ttu-id="24162-108">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="24162-108">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24162-109">備註</span><span class="sxs-lookup"><span data-stu-id="24162-109">Remarks</span></span>

<span data-ttu-id="24162-110">這個屬性會定義從滑杆控制項的開頭和結尾算起的位移，也就是當 **direction** 屬性設定為 "水準" 時，從左至右，如果設定為「垂直」，則是從上到下。</span><span class="sxs-lookup"><span data-stu-id="24162-110">This attribute defines an offset from the beginning and end of the slider control that is, from the left and right if the **direction** attribute is set to "horizontal", and from the top and bottom if it is set to "vertical".</span></span> <span data-ttu-id="24162-111">這些位移位置會指示滑杆捲動方塊的最小和最大位置，而不會套用前景色彩或影像。</span><span class="sxs-lookup"><span data-stu-id="24162-111">These offset positions dictate the minimum and maximum positions of the slider thumb, beyond which the foreground color or image will not be applied.</span></span>

<span data-ttu-id="24162-112">如果使用背景影像 **並將 [並排屬性]** 設定為 [true]，則會將位移套用至影像，並將影像的數量 (從左邊和右邊，或從頂端和底部) 用於滑杆控制項的開始和結束框線，並在其餘部分並排顯示影像的中央部分。</span><span class="sxs-lookup"><span data-stu-id="24162-112">If a background image is used with the **tiled** attribute set to true, the offset is applied to the image, dictating the amount of the image (either from the left and right or from the top and bottom) to be used for the beginning and end borders of the slider control, with the central portion of the image being tiled throughout the remainder.</span></span> <span data-ttu-id="24162-113">如此一來，小型背景影像就可以用來涵蓋較大滑杆控制項的完整長度。</span><span class="sxs-lookup"><span data-stu-id="24162-113">In this way, a small background image can be used to cover the full length of a larger slider control.</span></span>

## <a name="requirements"></a><span data-ttu-id="24162-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="24162-114">Requirements</span></span>



| <span data-ttu-id="24162-115">需求</span><span class="sxs-lookup"><span data-stu-id="24162-115">Requirement</span></span> | <span data-ttu-id="24162-116">值</span><span class="sxs-lookup"><span data-stu-id="24162-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="24162-117">版本</span><span class="sxs-lookup"><span data-stu-id="24162-117">Version</span></span><br/> | <span data-ttu-id="24162-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="24162-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24162-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24162-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24162-120">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="24162-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="24162-121">**滑杆. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="24162-121">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="24162-122">**滑杆. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="24162-122">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="24162-123">**滑杆. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="24162-123">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="24162-124">**滑杆。磚**</span><span class="sxs-lookup"><span data-stu-id="24162-124">**SLIDER.tiled**</span></span>](slider-tiled.md)
</dt> </dl>

 

 





