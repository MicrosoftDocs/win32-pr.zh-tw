---
title: AmbientAttributes. >horizontalalignment
description: '>horizontalalignment 屬性會指定或抓取值，指出調整視圖或父子視圖大小時，控制項的水準位置。'
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- AmbientAttributes. >horizontalalignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994579"
---
# <a name="ambientattributeshorizontalalignment"></a><span data-ttu-id="9d38d-104">AmbientAttributes. >horizontalalignment</span><span class="sxs-lookup"><span data-stu-id="9d38d-104">AmbientAttributes.horizontalAlignment</span></span>

<span data-ttu-id="9d38d-105">**>horizontalalignment** 屬性會指定或抓取值，指出調整 **視圖** 或父子 **視圖** 大小時，控制項的水準位置。</span><span class="sxs-lookup"><span data-stu-id="9d38d-105">The **horizontalAlignment** attribute specifies or retrieves a value that indicates the horizontal placement of the control when the **VIEW** or parent **SUBVIEW** is resized.</span></span>

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="9d38d-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="9d38d-106">Possible Values</span></span>

<span data-ttu-id="9d38d-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="9d38d-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="9d38d-108">值</span><span class="sxs-lookup"><span data-stu-id="9d38d-108">Value</span></span>   | <span data-ttu-id="9d38d-109">描述</span><span class="sxs-lookup"><span data-stu-id="9d38d-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d38d-110">left</span><span class="sxs-lookup"><span data-stu-id="9d38d-110">left</span></span>    | <span data-ttu-id="9d38d-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="9d38d-111">Default.</span></span> <span data-ttu-id="9d38d-112">當調整視圖大小時，會維護控制項相對於 **view** 或 parent 子 **視圖左邊** 的位置。</span><span class="sxs-lookup"><span data-stu-id="9d38d-112">Maintains the placement of the control relative to the left of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9d38d-113">向右</span><span class="sxs-lookup"><span data-stu-id="9d38d-113">right</span></span>   | <span data-ttu-id="9d38d-114">當調整視圖大小時，會維護控制項相對於 **view** 或 Parent 子 **視圖** 右邊的位置。</span><span class="sxs-lookup"><span data-stu-id="9d38d-114">Maintains the placement of the control relative to the right of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="9d38d-115">中心</span><span class="sxs-lookup"><span data-stu-id="9d38d-115">center</span></span>  | <span data-ttu-id="9d38d-116">當調整視圖大小時，會維護控制項相對於 **視圖** 或父子 **視圖** 水準中心的位置。</span><span class="sxs-lookup"><span data-stu-id="9d38d-116">Maintains the placement of the control relative to the horizontal center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="9d38d-117">Stretch - 自動縮放</span><span class="sxs-lookup"><span data-stu-id="9d38d-117">stretch</span></span> | <span data-ttu-id="9d38d-118">當調整大小時，會維護控制項相對於 **視圖** 或父子 **視圖** 左右邊界的位置。</span><span class="sxs-lookup"><span data-stu-id="9d38d-118">Maintains the placement of the control relative to both the left and right margins of the **VIEW** or parent **SUBVIEW** when resized.</span></span> <span data-ttu-id="9d38d-119">當 **視圖** 或子 **視圖** 伸展時，控制項會擴展至適當的大小。</span><span class="sxs-lookup"><span data-stu-id="9d38d-119">The control stretches to fit when the **VIEW** or **SUBVIEW** is stretched.</span></span> <span data-ttu-id="9d38d-120">實際的影像除非可以調整大小，否則不會增加或縮小，但如果未受 **clippingImage** 限制，可按一下的區域會擴大或縮小。</span><span class="sxs-lookup"><span data-stu-id="9d38d-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9d38d-121">備註</span><span class="sxs-lookup"><span data-stu-id="9d38d-121">Remarks</span></span>

<span data-ttu-id="9d38d-122">除非 **>horizontalalignment** 設為 "center"，否則控制項會保留其與指定邊緣之間的原始距離，如果指定了 "stretch" 且控制項可以調整大小，則會從兩個邊緣保留原始距離。</span><span class="sxs-lookup"><span data-stu-id="9d38d-122">Unless **horizontalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="9d38d-123">如果無法調整控制項的大小，且指定了「延展」，則會改為按一下可按一下的區域。</span><span class="sxs-lookup"><span data-stu-id="9d38d-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="9d38d-124">您可以設定 **>horizontalalignment** 和 **verticalAlignment** 的任何組合。</span><span class="sxs-lookup"><span data-stu-id="9d38d-124">You can set any combination of **horizontalAlignment** and **verticalAlignment**.</span></span> <span data-ttu-id="9d38d-125">例如，如果您想要以水準和垂直方式置中控制項，請設定 >horizontalalignment = "center" verticalAlignment = "center"。</span><span class="sxs-lookup"><span data-stu-id="9d38d-125">For example, if you want to center a control both horizontally and vertically, set horizontalAlignment="center" verticalAlignment="center".</span></span>

## <a name="requirements"></a><span data-ttu-id="9d38d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d38d-126">Requirements</span></span>



| <span data-ttu-id="9d38d-127">需求</span><span class="sxs-lookup"><span data-stu-id="9d38d-127">Requirement</span></span> | <span data-ttu-id="9d38d-128">值</span><span class="sxs-lookup"><span data-stu-id="9d38d-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9d38d-129">版本</span><span class="sxs-lookup"><span data-stu-id="9d38d-129">Version</span></span><br/> | <span data-ttu-id="9d38d-130">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="9d38d-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d38d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d38d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d38d-132">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="9d38d-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="9d38d-133">**AmbientAttributes. verticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="9d38d-133">**AmbientAttributes.verticalAlignment**</span></span>](ambientattributes-verticalalignment.md)
</dt> <dt>

[<span data-ttu-id="9d38d-134">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="9d38d-134">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





