---
title: 滑杆. thumbImage
description: ThumbImage 屬性會指定或抓取將用來表示滑杆目前位置的影像。
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- ThumbImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994829"
---
# <a name="sliderthumbimage"></a><span data-ttu-id="a5479-104">滑杆. thumbImage</span><span class="sxs-lookup"><span data-stu-id="a5479-104">SLIDER.thumbImage</span></span>

<span data-ttu-id="a5479-105">**ThumbImage** 屬性會指定或抓取將用來表示滑杆目前位置的影像。</span><span class="sxs-lookup"><span data-stu-id="a5479-105">The **thumbImage** attribute specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a><span data-ttu-id="a5479-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="a5479-106">Possible Values</span></span>

<span data-ttu-id="a5479-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="a5479-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5479-108">備註</span><span class="sxs-lookup"><span data-stu-id="a5479-108">Remarks</span></span>

<span data-ttu-id="a5479-109">**ThumbImage** 會指定要用來代表目前位置的影像，以及表示使用者可以對控制項採取動作。</span><span class="sxs-lookup"><span data-stu-id="a5479-109">The **thumbImage** specifies the image that will be used to represent current position, as well as indicate that the user can take action with the control.</span></span> <span data-ttu-id="a5479-110">如果未指定任何 thumb 影像，則滑杆為非互動式。</span><span class="sxs-lookup"><span data-stu-id="a5479-110">If no thumb image is specified, the slider is non-interactive.</span></span>

<span data-ttu-id="a5479-111">捲動方塊的影像會以滑杆控制項的窄維度為中心。</span><span class="sxs-lookup"><span data-stu-id="a5479-111">The thumb image is centered in the narrow dimension of the slider control.</span></span> <span data-ttu-id="a5479-112">如果 thumb 影像比控制項窄，則影像會出現在背景的中間。</span><span class="sxs-lookup"><span data-stu-id="a5479-112">If the thumb image is narrower than the control, the image appears in the middle of the background.</span></span> <span data-ttu-id="a5479-113">如果 thumb 影像大於控制項，則會將影像的末端剪下。</span><span class="sxs-lookup"><span data-stu-id="a5479-113">If the thumb image is larger than the control, the ends of the image are cut off.</span></span>

<span data-ttu-id="a5479-114">滑杆的位置是由 thumb 影像的中心所指定。</span><span class="sxs-lookup"><span data-stu-id="a5479-114">The position of the slider is specified by the center of the thumb image.</span></span> <span data-ttu-id="a5479-115">如果 **borderSize** 為零，則只有一半的 thumb 影像會顯示在開頭和結束滑杆的位置。</span><span class="sxs-lookup"><span data-stu-id="a5479-115">If **borderSize** is zero, only half the thumb image will be visible at the beginning and end slider positions.</span></span> <span data-ttu-id="a5479-116">若要避免這種情況，請將 **borderSize** 設定為大於或等於 thumb (影像寬度一半的值，如果 **方向** 設為「垂直」 ) ，則為一半的高度。</span><span class="sxs-lookup"><span data-stu-id="a5479-116">To prevent this, set **borderSize** to a value greater than or equal to half the width of the thumb image (or half the height if **direction** is set to "vertical").</span></span>

<span data-ttu-id="a5479-117">支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="a5479-117">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

<span data-ttu-id="a5479-118">請參閱 **CUSTOMSLIDER**。說明如何使用 **滑杆** 元素屬性之範例的 [positionImage](customslider-positionimage.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="a5479-118">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5479-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5479-119">Requirements</span></span>



| <span data-ttu-id="a5479-120">需求</span><span class="sxs-lookup"><span data-stu-id="a5479-120">Requirement</span></span> | <span data-ttu-id="a5479-121">值</span><span class="sxs-lookup"><span data-stu-id="a5479-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a5479-122">版本</span><span class="sxs-lookup"><span data-stu-id="a5479-122">Version</span></span><br/> | <span data-ttu-id="a5479-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="a5479-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5479-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5479-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5479-125">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="a5479-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="a5479-126">**滑杆. borderSize**</span><span class="sxs-lookup"><span data-stu-id="a5479-126">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="a5479-127">**滑杆。方向**</span><span class="sxs-lookup"><span data-stu-id="a5479-127">**SLIDER.direction**</span></span>](slider-direction.md)
</dt> </dl>

 

 





