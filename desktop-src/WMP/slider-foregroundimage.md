---
title: 滑杆. foregroundImage
description: ForegroundImage 屬性會指定或抓取滑杆的前景影像。
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- ForegroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987926"
---
# <a name="sliderforegroundimage"></a><span data-ttu-id="528ca-104">滑杆. foregroundImage</span><span class="sxs-lookup"><span data-stu-id="528ca-104">SLIDER.foregroundImage</span></span>

<span data-ttu-id="528ca-105">**ForegroundImage** 屬性會指定或抓取滑杆的前景影像。</span><span class="sxs-lookup"><span data-stu-id="528ca-105">The **foregroundImage** attribute specifies or retrieves the foreground image of the slider.</span></span>

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a><span data-ttu-id="528ca-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="528ca-106">Possible Values</span></span>

<span data-ttu-id="528ca-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="528ca-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="528ca-108">備註</span><span class="sxs-lookup"><span data-stu-id="528ca-108">Remarks</span></span>

<span data-ttu-id="528ca-109">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="528ca-109">This attribute is optional.</span></span> <span data-ttu-id="528ca-110">使用影像來建立滑杆控制項時， **backgroundImage** 會用於主要滑杆影像。</span><span class="sxs-lookup"><span data-stu-id="528ca-110">When using images to construct a slider control, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="528ca-111">**ThumbImage** 代表實際的滑杆，而且可以使用滑鼠移動。</span><span class="sxs-lookup"><span data-stu-id="528ca-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="528ca-112">在 **thumbImage** 滑杆有一個不可見的行，其中的背景影像會顯示在一行的一端，而前景影像會顯示在另一端。</span><span class="sxs-lookup"><span data-stu-id="528ca-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="528ca-113">當您以滑鼠移動 **thumbImage** 滑杆時，如果投影 **片** 設為 true，則前景影像會沿著滑杆拉出以涵蓋背景影像的方式滑出。</span><span class="sxs-lookup"><span data-stu-id="528ca-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="528ca-114">如果投影 **片** 設為 false，則前景影像不會移動，但會顯示在原處，如同滑杆將背景影像移出前景影像。</span><span class="sxs-lookup"><span data-stu-id="528ca-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="528ca-115">如果並排顯示 **的屬性設** 為 true，且前景影像小於滑杆控制項的前景區域，則會以水準或垂直方式並排顯示影像，視 **方向** 屬性而定，填滿可用的空間。</span><span class="sxs-lookup"><span data-stu-id="528ca-115">If the **tiled** attribute is set to true and the foreground image is smaller than the foreground area of the slider control, the image will be tiled either horizontally or vertically, depending on the **direction** attribute, to fill the available space.</span></span>

<span data-ttu-id="528ca-116">支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="528ca-116">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="528ca-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="528ca-117">Requirements</span></span>



| <span data-ttu-id="528ca-118">需求</span><span class="sxs-lookup"><span data-stu-id="528ca-118">Requirement</span></span> | <span data-ttu-id="528ca-119">值</span><span class="sxs-lookup"><span data-stu-id="528ca-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="528ca-120">版本</span><span class="sxs-lookup"><span data-stu-id="528ca-120">Version</span></span><br/> | <span data-ttu-id="528ca-121">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="528ca-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="528ca-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="528ca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528ca-123">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="528ca-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="528ca-124">**滑杆. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="528ca-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="528ca-125">**滑杆。投影片**</span><span class="sxs-lookup"><span data-stu-id="528ca-125">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="528ca-126">**滑杆. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="528ca-126">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="528ca-127">**滑杆。值**</span><span class="sxs-lookup"><span data-stu-id="528ca-127">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





