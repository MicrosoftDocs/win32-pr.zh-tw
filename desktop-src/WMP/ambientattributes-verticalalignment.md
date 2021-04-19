---
title: AmbientAttributes. verticalAlignment
description: VerticalAlignment 屬性會指定或抓取值，指出當視圖或父子視圖伸展時，控制項的垂直位置。
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- AmbientAttributes. verticalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996458"
---
# <a name="ambientattributesverticalalignment"></a><span data-ttu-id="383b2-104">AmbientAttributes. verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="383b2-104">AmbientAttributes.verticalAlignment</span></span>

<span data-ttu-id="383b2-105">**VerticalAlignment** 屬性會指定或抓取值，指出當 **視圖** 或父子 **視圖** 伸展時，控制項的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="383b2-105">The **verticalAlignment** attribute specifies or retrieves a value indicating the vertical placement of the control when the **VIEW** or parent **SUBVIEW** is stretched.</span></span>

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="383b2-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="383b2-106">Possible Values</span></span>

<span data-ttu-id="383b2-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="383b2-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="383b2-108">值</span><span class="sxs-lookup"><span data-stu-id="383b2-108">Value</span></span>   | <span data-ttu-id="383b2-109">描述</span><span class="sxs-lookup"><span data-stu-id="383b2-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="383b2-110">top</span><span class="sxs-lookup"><span data-stu-id="383b2-110">top</span></span>     | <span data-ttu-id="383b2-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="383b2-111">Default.</span></span> <span data-ttu-id="383b2-112">當調整視圖大小時，會維護控制項相對於 **view** 或 parent 子 **視圖頂端** 的位置。</span><span class="sxs-lookup"><span data-stu-id="383b2-112">Maintains the placement of the control relative to the top of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="383b2-113">下</span><span class="sxs-lookup"><span data-stu-id="383b2-113">bottom</span></span>  | <span data-ttu-id="383b2-114">當調整視圖大小時，會維護控制項相對於 **視圖** 或父子 **視圖** 底部的位置。</span><span class="sxs-lookup"><span data-stu-id="383b2-114">Maintains the placement of the control relative to the bottom of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="383b2-115">中心</span><span class="sxs-lookup"><span data-stu-id="383b2-115">center</span></span>  | <span data-ttu-id="383b2-116">當調整視圖大小時，會維護控制項相對於 **view** 或 parent **子視圖垂直** 中心的位置。</span><span class="sxs-lookup"><span data-stu-id="383b2-116">Maintains the placement of the control relative to the vertical center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="383b2-117">Stretch - 自動縮放</span><span class="sxs-lookup"><span data-stu-id="383b2-117">stretch</span></span> | <span data-ttu-id="383b2-118">將控制項的放置位置維持在調整大小時，相對於視圖的上邊界和下邊界。</span><span class="sxs-lookup"><span data-stu-id="383b2-118">Maintains the placement of the control relative to both the top and bottom margins of the View when resized.</span></span> <span data-ttu-id="383b2-119">當 **視圖** 或父項子 **視圖** 伸展時，控制項會延展到適當的大小。</span><span class="sxs-lookup"><span data-stu-id="383b2-119">The control stretches to fit when the **VIEW** or parent **SUBVIEW** is stretched.</span></span> <span data-ttu-id="383b2-120">實際的影像除非可以調整大小，否則不會增加或縮小，但如果未受 **clippingImage** 限制，可按一下的區域會擴大或縮小。</span><span class="sxs-lookup"><span data-stu-id="383b2-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="383b2-121">備註</span><span class="sxs-lookup"><span data-stu-id="383b2-121">Remarks</span></span>

<span data-ttu-id="383b2-122">除非 **verticalAlignment** 設為 "center"，否則控制項會保留其與指定邊緣之間的原始距離，如果指定了 "stretch" 且控制項可以調整大小，則會從兩個邊緣保留原始距離。</span><span class="sxs-lookup"><span data-stu-id="383b2-122">Unless **verticalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="383b2-123">如果無法調整控制項的大小，且指定了「延展」，則會改為按一下可按一下的區域。</span><span class="sxs-lookup"><span data-stu-id="383b2-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="383b2-124">您可以設定 **>horizontalalignment** 和 **verticalAlignment** 屬性的任何組合。</span><span class="sxs-lookup"><span data-stu-id="383b2-124">You can set any combination of the **horizontalAlignment** and **verticalAlignment** attributes.</span></span> <span data-ttu-id="383b2-125">例如，如果您想要以水準和垂直方式置中控制項，請將 **>horizontalalignment** 設定為 "center"，並將 **verticalAlignment** 設為 "center"。</span><span class="sxs-lookup"><span data-stu-id="383b2-125">For example, if you want a control to be centered both horizontally and vertically, set **horizontalAlignment** to "center" and **verticalAlignment** to "center".</span></span>

## <a name="requirements"></a><span data-ttu-id="383b2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="383b2-126">Requirements</span></span>



| <span data-ttu-id="383b2-127">需求</span><span class="sxs-lookup"><span data-stu-id="383b2-127">Requirement</span></span> | <span data-ttu-id="383b2-128">值</span><span class="sxs-lookup"><span data-stu-id="383b2-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="383b2-129">版本</span><span class="sxs-lookup"><span data-stu-id="383b2-129">Version</span></span><br/> | <span data-ttu-id="383b2-130">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="383b2-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="383b2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="383b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383b2-132">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="383b2-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="383b2-133">**AmbientAttributes. >horizontalalignment**</span><span class="sxs-lookup"><span data-stu-id="383b2-133">**AmbientAttributes.horizontalAlignment**</span></span>](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





