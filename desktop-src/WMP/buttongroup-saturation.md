---
title: BUTTONGROUP 飽和度
description: 飽和度屬性會指定或抓取 BUTTONGROUP 影像的飽和度值。
ms.assetid: bfd957f0-8201-4a4f-9162-a397ed97c747
keywords:
- BUTTONGROUP 飽和度 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8de7dd39eb0b1a9e3f24031e24851eba22c6c6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999354"
---
# <a name="buttongroupsaturation"></a><span data-ttu-id="02f08-104">BUTTONGROUP 飽和度</span><span class="sxs-lookup"><span data-stu-id="02f08-104">BUTTONGROUP.saturation</span></span>

<span data-ttu-id="02f08-105">**飽和度** 屬性會指定或抓取 **BUTTONGROUP** 影像的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="02f08-105">The **saturation** attribute specifies or retrieves the saturation value of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a><span data-ttu-id="02f08-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="02f08-106">Possible Values</span></span>

<span data-ttu-id="02f08-107">這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到2.0，預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="02f08-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 2.0 with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f08-108">備註</span><span class="sxs-lookup"><span data-stu-id="02f08-108">Remarks</span></span>

<span data-ttu-id="02f08-109">這個屬性會變更 **disabledImage**、 **downImage**、 **hoverDownImage**、 **hoverImage** 和 **image** 屬性所指定之影像的飽和度值（如果已指定），而且它們參考的是8位的 BMP 影像。</span><span class="sxs-lookup"><span data-stu-id="02f08-109">This attribute changes the saturation value of the images specified by the **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage**, and **image** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f08-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="02f08-110">Requirements</span></span>



| <span data-ttu-id="02f08-111">需求</span><span class="sxs-lookup"><span data-stu-id="02f08-111">Requirement</span></span> | <span data-ttu-id="02f08-112">值</span><span class="sxs-lookup"><span data-stu-id="02f08-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="02f08-113">版本</span><span class="sxs-lookup"><span data-stu-id="02f08-113">Version</span></span><br/> | <span data-ttu-id="02f08-114">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="02f08-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02f08-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02f08-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f08-116">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="02f08-116">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="02f08-117">**BUTTONGROUP. disabledImage**</span><span class="sxs-lookup"><span data-stu-id="02f08-117">**BUTTONGROUP.disabledImage**</span></span>](buttongroup-disabledimage.md)
</dt> <dt>

[<span data-ttu-id="02f08-118">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="02f08-118">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="02f08-119">**BUTTONGROUP. hoverDownImage**</span><span class="sxs-lookup"><span data-stu-id="02f08-119">**BUTTONGROUP.hoverDownImage**</span></span>](buttongroup-hoverdownimage.md)
</dt> <dt>

[<span data-ttu-id="02f08-120">**BUTTONGROUP. hoverImage**</span><span class="sxs-lookup"><span data-stu-id="02f08-120">**BUTTONGROUP.hoverImage**</span></span>](buttongroup-hoverimage.md)
</dt> <dt>

[<span data-ttu-id="02f08-121">**BUTTONGROUP. hueShift**</span><span class="sxs-lookup"><span data-stu-id="02f08-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="02f08-122">**BUTTONGROUP 影像**</span><span class="sxs-lookup"><span data-stu-id="02f08-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> </dl>

 

 





