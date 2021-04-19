---
title: 滑杆。投影片
description: 投影片屬性會指定或抓取值，指出前景影像是否滑在背景影像上，或是在背景影像的靜態位置中逐漸顯示。
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- 滑杆。投影片 Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984356"
---
# <a name="sliderslide"></a><span data-ttu-id="eaa98-104">滑杆。投影片</span><span class="sxs-lookup"><span data-stu-id="eaa98-104">SLIDER.slide</span></span>

<span data-ttu-id="eaa98-105">投影 **片** 屬性會指定或抓取值，指出前景影像是否滑在背景影像上，或是在背景影像的靜態位置中逐漸顯示。</span><span class="sxs-lookup"><span data-stu-id="eaa98-105">The **slide** attribute specifies or retrieves a value indicating whether the foreground image slides over the background image or is gradually revealed in a static position over the background image.</span></span>

``` syntax
        elementID.slide
```

## <a name="possible-values"></a><span data-ttu-id="eaa98-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="eaa98-106">Possible Values</span></span>

<span data-ttu-id="eaa98-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="eaa98-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="eaa98-108">值</span><span class="sxs-lookup"><span data-stu-id="eaa98-108">Value</span></span> | <span data-ttu-id="eaa98-109">描述</span><span class="sxs-lookup"><span data-stu-id="eaa98-109">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="eaa98-110">true</span><span class="sxs-lookup"><span data-stu-id="eaa98-110">true</span></span>  | <span data-ttu-id="eaa98-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="eaa98-111">Default.</span></span> <span data-ttu-id="eaa98-112">前景影像會滑到背景影像上方。</span><span class="sxs-lookup"><span data-stu-id="eaa98-112">The foreground image slides over the background image.</span></span>      |
| <span data-ttu-id="eaa98-113">false</span><span class="sxs-lookup"><span data-stu-id="eaa98-113">false</span></span> | <span data-ttu-id="eaa98-114">前景影像會顯示在背景影像上。</span><span class="sxs-lookup"><span data-stu-id="eaa98-114">The foreground image is revealed in place over the background image.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eaa98-115">備註</span><span class="sxs-lookup"><span data-stu-id="eaa98-115">Remarks</span></span>

<span data-ttu-id="eaa98-116">當您以滑鼠移動 **thumbImage** 滑杆時，如果投影 **片** 設為 true，則前景影像會沿著滑杆拉出以涵蓋背景影像的方式滑出。</span><span class="sxs-lookup"><span data-stu-id="eaa98-116">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="eaa98-117">如果投影 **片** 設為 false，則前景影像不會移動，但會顯示在原處，如同滑杆將背景影像移出前景影像。</span><span class="sxs-lookup"><span data-stu-id="eaa98-117">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa98-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaa98-118">Requirements</span></span>



| <span data-ttu-id="eaa98-119">需求</span><span class="sxs-lookup"><span data-stu-id="eaa98-119">Requirement</span></span> | <span data-ttu-id="eaa98-120">值</span><span class="sxs-lookup"><span data-stu-id="eaa98-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="eaa98-121">版本</span><span class="sxs-lookup"><span data-stu-id="eaa98-121">Version</span></span><br/> | <span data-ttu-id="eaa98-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="eaa98-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eaa98-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaa98-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa98-124">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="eaa98-124">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="eaa98-125">**滑杆. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="eaa98-125">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="eaa98-126">**滑杆. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="eaa98-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





