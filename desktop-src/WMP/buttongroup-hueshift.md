---
title: BUTTONGROUP. hueShift
description: HueShift 屬性會指定或抓取 BUTTONGROUP 影像的色調要移位的量。
ms.assetid: 156256ef-ec24-40c4-ad23-064e38c79e69
keywords:
- BUTTONGROUP. hueShift Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf77faea27ecc5adee6525c4ee8d8ff1541aac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977146"
---
# <a name="buttongrouphueshift"></a><span data-ttu-id="134ed-104">BUTTONGROUP. hueShift</span><span class="sxs-lookup"><span data-stu-id="134ed-104">BUTTONGROUP.hueShift</span></span>

<span data-ttu-id="134ed-105">**HueShift** 屬性會指定或抓取 **BUTTONGROUP** 影像的色調要移位的量。</span><span class="sxs-lookup"><span data-stu-id="134ed-105">The **hueShift** attribute specifies or retrieves the amount by which the hue of the **BUTTONGROUP** images is shifted.</span></span>

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a><span data-ttu-id="134ed-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="134ed-106">Possible Values</span></span>

<span data-ttu-id="134ed-107">這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到360.0，預設值為0.0。</span><span class="sxs-lookup"><span data-stu-id="134ed-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 360.0 with a default value of 0.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="134ed-108">備註</span><span class="sxs-lookup"><span data-stu-id="134ed-108">Remarks</span></span>

<span data-ttu-id="134ed-109">這個屬性會變更 **disabledImage**、 **downImage**、 **hoverDownImage**、 **hoverImage** 和 **image** 屬性所指定之影像的色調值（如果已指定），而且它們參考的是8位的 BMP 影像。</span><span class="sxs-lookup"><span data-stu-id="134ed-109">This attribute changes the hue value of the images specified by the **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage**, and **image** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="134ed-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="134ed-110">Requirements</span></span>



| <span data-ttu-id="134ed-111">需求</span><span class="sxs-lookup"><span data-stu-id="134ed-111">Requirement</span></span> | <span data-ttu-id="134ed-112">值</span><span class="sxs-lookup"><span data-stu-id="134ed-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="134ed-113">版本</span><span class="sxs-lookup"><span data-stu-id="134ed-113">Version</span></span><br/> | <span data-ttu-id="134ed-114">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="134ed-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="134ed-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="134ed-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134ed-116">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="134ed-116">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="134ed-117">**BUTTONGROUP. disabledImage**</span><span class="sxs-lookup"><span data-stu-id="134ed-117">**BUTTONGROUP.disabledImage**</span></span>](buttongroup-disabledimage.md)
</dt> <dt>

[<span data-ttu-id="134ed-118">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="134ed-118">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="134ed-119">**BUTTONGROUP. hoverDownImage**</span><span class="sxs-lookup"><span data-stu-id="134ed-119">**BUTTONGROUP.hoverDownImage**</span></span>](buttongroup-hoverdownimage.md)
</dt> <dt>

[<span data-ttu-id="134ed-120">**BUTTONGROUP. hoverImage**</span><span class="sxs-lookup"><span data-stu-id="134ed-120">**BUTTONGROUP.hoverImage**</span></span>](buttongroup-hoverimage.md)
</dt> <dt>

[<span data-ttu-id="134ed-121">**BUTTONGROUP 影像**</span><span class="sxs-lookup"><span data-stu-id="134ed-121">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="134ed-122">**BUTTONGROUP 飽和度**</span><span class="sxs-lookup"><span data-stu-id="134ed-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





