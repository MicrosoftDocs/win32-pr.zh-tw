---
title: 滑杆. backgroundImage
description: BackgroundImage 屬性會指定或抓取滑杆的背景影像。
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- BackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982930"
---
# <a name="sliderbackgroundimage"></a><span data-ttu-id="cd0dd-104">滑杆. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="cd0dd-104">SLIDER.backgroundImage</span></span>

<span data-ttu-id="cd0dd-105">**BackgroundImage** 屬性會指定或抓取滑杆的背景影像。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-105">The **backgroundImage** attribute specifies or retrieves the background image of the slider.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="cd0dd-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="cd0dd-106">Possible Values</span></span>

<span data-ttu-id="cd0dd-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd0dd-108">備註</span><span class="sxs-lookup"><span data-stu-id="cd0dd-108">Remarks</span></span>

<span data-ttu-id="cd0dd-109">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-109">This attribute is optional.</span></span> <span data-ttu-id="cd0dd-110">使用影像來建立滑杆時， **backgroundImage** 會用於主要滑杆影像。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-110">When using images to construct a slider, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="cd0dd-111">**ThumbImage** 代表實際的滑杆，而且可以使用滑鼠移動。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="cd0dd-112">在 **thumbImage** 滑杆有一個不可見的行，其中的背景影像會顯示在一行的一端，而前景影像會顯示在另一端。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="cd0dd-113">當您以滑鼠移動 **thumbImage** 滑杆時，如果投影 **片** 設為 true，則前景影像會沿著滑杆拉出以涵蓋背景影像的方式滑出。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="cd0dd-114">如果投影 **片** 設為 false，則前景影像不會移動，但會顯示在原處，如同滑杆將背景影像移出前景影像。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="cd0dd-115">如果 [並排顯示 **] 屬性設定** 為 [true]，而且背景影像小於滑杆控制項，則會根據 [ **方向** ] 屬性，以水準或垂直方式並排顯示影像。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-115">If the **tiled** attribute is set to true and the background image is smaller than the slider control, the image will be tiled either horizontally or vertically depending on the **direction** attribute.</span></span> <span data-ttu-id="cd0dd-116">如果 [ **borderSize** ] 屬性設定為大於零的值，則指定的數位將會是從影像左邊、右邊或頂端和底部開始 (的圖元數，視將保留給滑杆控制項框線的 **方向** 屬性) 而定。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-116">If the **borderSize** attribute is set to a value greater than zero, the number specified will be the number of pixels from the left and right or top and bottom of the image (again, depending on the **direction** attribute) that will be reserved for the borders of the slider control.</span></span> <span data-ttu-id="cd0dd-117">在此情況下，只有影像的中央部分會用來將其餘的控制項平平鋪。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-117">In this case, only the central portion of the image is used for tiling the remainder of the control.</span></span>

<span data-ttu-id="cd0dd-118">支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="cd0dd-118">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0dd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd0dd-119">Requirements</span></span>



| <span data-ttu-id="cd0dd-120">需求</span><span class="sxs-lookup"><span data-stu-id="cd0dd-120">Requirement</span></span> | <span data-ttu-id="cd0dd-121">值</span><span class="sxs-lookup"><span data-stu-id="cd0dd-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cd0dd-122">版本</span><span class="sxs-lookup"><span data-stu-id="cd0dd-122">Version</span></span><br/> | <span data-ttu-id="cd0dd-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="cd0dd-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd0dd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd0dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0dd-125">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="cd0dd-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="cd0dd-126">**滑杆. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="cd0dd-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="cd0dd-127">**滑杆。投影片**</span><span class="sxs-lookup"><span data-stu-id="cd0dd-127">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="cd0dd-128">**滑杆. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="cd0dd-128">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> </dl>

 

 





