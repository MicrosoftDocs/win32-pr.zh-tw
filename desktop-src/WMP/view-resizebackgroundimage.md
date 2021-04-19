---
title: ResizeBackgroundImage
description: ResizeBackgroundImage 屬性會指定或抓取值，指出背景影像是否可以調整大小。
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- ResizeBackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974911"
---
# <a name="viewresizebackgroundimage"></a><span data-ttu-id="72140-104">ResizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="72140-104">VIEW.resizeBackgroundImage</span></span>

<span data-ttu-id="72140-105">**ResizeBackgroundImage** 屬性會指定或抓取值，指出背景影像是否可以調整大小。</span><span class="sxs-lookup"><span data-stu-id="72140-105">The **resizeBackgroundImage** attribute specifies or retrieves a value indicating whether the background image can be resized.</span></span>

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="72140-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="72140-106">Possible Values</span></span>

<span data-ttu-id="72140-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="72140-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="72140-108">值</span><span class="sxs-lookup"><span data-stu-id="72140-108">Values</span></span> | <span data-ttu-id="72140-109">描述</span><span class="sxs-lookup"><span data-stu-id="72140-109">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="72140-110">true</span><span class="sxs-lookup"><span data-stu-id="72140-110">true</span></span>   | <span data-ttu-id="72140-111">背景影像可以調整大小。</span><span class="sxs-lookup"><span data-stu-id="72140-111">The background image can be resized.</span></span>             |
| <span data-ttu-id="72140-112">false</span><span class="sxs-lookup"><span data-stu-id="72140-112">false</span></span>  | <span data-ttu-id="72140-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="72140-113">Default.</span></span> <span data-ttu-id="72140-114">背景影像無法調整大小。</span><span class="sxs-lookup"><span data-stu-id="72140-114">The background image cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="72140-115">備註</span><span class="sxs-lookup"><span data-stu-id="72140-115">Remarks</span></span>

<span data-ttu-id="72140-116">如果您將此屬性設定為 true，背景影像會調整大小以符合 **width** 和 **height** 屬性的目前值。</span><span class="sxs-lookup"><span data-stu-id="72140-116">If you set this attribute to true, the background image will resize to fit the current values of the **width** and **height** attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="72140-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="72140-117">Requirements</span></span>



| <span data-ttu-id="72140-118">需求</span><span class="sxs-lookup"><span data-stu-id="72140-118">Requirement</span></span> | <span data-ttu-id="72140-119">值</span><span class="sxs-lookup"><span data-stu-id="72140-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="72140-120">版本</span><span class="sxs-lookup"><span data-stu-id="72140-120">Version</span></span><br/> | <span data-ttu-id="72140-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="72140-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72140-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72140-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72140-123">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="72140-123">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="72140-124">**BackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="72140-124">**VIEW.backgroundImage**</span></span>](view-backgroundimage.md)
</dt> </dl>

 

 





