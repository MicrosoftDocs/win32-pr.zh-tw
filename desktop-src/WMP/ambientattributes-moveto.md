---
title: AmbientAttributes
description: MoveTo 方法會以線性速度將控制項移至新的位置。
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992886"
---
# <a name="ambientattributesmoveto"></a><span data-ttu-id="d731a-104">AmbientAttributes</span><span class="sxs-lookup"><span data-stu-id="d731a-104">AmbientAttributes.moveTo</span></span>

<span data-ttu-id="d731a-105">**MoveTo** 方法會以線性速度將控制項移至新的位置。</span><span class="sxs-lookup"><span data-stu-id="d731a-105">The **moveTo** method moves the control to a new location at a linear speed.</span></span>

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a><span data-ttu-id="d731a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d731a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d731a-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span><span class="sxs-lookup"><span data-stu-id="d731a-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span></span>
</dt> <dd>

<span data-ttu-id="d731a-108">**數值** (**long**) 指定控制項 **左方** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="d731a-108">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d731a-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span><span class="sxs-lookup"><span data-stu-id="d731a-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span></span>
</dt> <dd>

<span data-ttu-id="d731a-110">**數值** (**long**) 指定控制項 **頂端** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="d731a-110">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d731a-111"><span id="time"></span><span id="TIME"></span>*時間*</span><span class="sxs-lookup"><span data-stu-id="d731a-111"><span id="time"></span><span id="TIME"></span>*time*</span></span>
</dt> <dd>

<span data-ttu-id="d731a-112">**Number** (**long**) 指定控制項移至新位置所需的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d731a-112">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d731a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d731a-113">Return Value</span></span>

<span data-ttu-id="d731a-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d731a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d731a-115">備註</span><span class="sxs-lookup"><span data-stu-id="d731a-115">Remarks</span></span>

<span data-ttu-id="d731a-116">這種方法適用于動畫的子 **視圖** 專案 (例如，如果使用者按一下紙匣，而控制項向下滑) 。</span><span class="sxs-lookup"><span data-stu-id="d731a-116">This method is useful for animated **SUBVIEW** elements (for example, if the user clicks a tray and the controls slide down).</span></span>

<span data-ttu-id="d731a-117">這個方法會在移動控制項時建立線性動作。</span><span class="sxs-lookup"><span data-stu-id="d731a-117">This method creates a linear motion when moving the control.</span></span> <span data-ttu-id="d731a-118">這不同于 **slideTo**，它會建立非線性的動畫。</span><span class="sxs-lookup"><span data-stu-id="d731a-118">This differs from **slideTo**, which creates a non-linear motion.</span></span>

## <a name="requirements"></a><span data-ttu-id="d731a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d731a-119">Requirements</span></span>



| <span data-ttu-id="d731a-120">需求</span><span class="sxs-lookup"><span data-stu-id="d731a-120">Requirement</span></span> | <span data-ttu-id="d731a-121">值</span><span class="sxs-lookup"><span data-stu-id="d731a-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d731a-122">版本</span><span class="sxs-lookup"><span data-stu-id="d731a-122">Version</span></span><br/> | <span data-ttu-id="d731a-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="d731a-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d731a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d731a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d731a-125">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="d731a-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="d731a-126">**AmbientAttributes left**</span><span class="sxs-lookup"><span data-stu-id="d731a-126">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="d731a-127">**AmbientAttributes.slideTo**</span><span class="sxs-lookup"><span data-stu-id="d731a-127">**AmbientAttributes.slideTo**</span></span>](ambientattributes-slideto.md)
</dt> <dt>

[<span data-ttu-id="d731a-128">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="d731a-128">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





