---
title: ScrollingAmount
description: ScrollingAmount 屬性會指定或抓取文字在每個滾動移動期間移動的圖元數。
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- ScrollingAmount Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989623"
---
# <a name="textscrollingamount"></a><span data-ttu-id="8a804-104">ScrollingAmount</span><span class="sxs-lookup"><span data-stu-id="8a804-104">TEXT.scrollingAmount</span></span>

<span data-ttu-id="8a804-105">**ScrollingAmount** 屬性會指定或抓取文字在每個滾動移動期間移動的圖元數。</span><span class="sxs-lookup"><span data-stu-id="8a804-105">The **scrollingAmount** attribute specifies or retrieves the number of pixels that the text moves during each scrolling movement.</span></span>

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a><span data-ttu-id="8a804-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="8a804-106">Possible Values</span></span>

<span data-ttu-id="8a804-107">這個屬性是 (**int**) 的正數讀/寫 **數位**，預設值是6。</span><span class="sxs-lookup"><span data-stu-id="8a804-107">This attribute is a positive read/write **Number** (**int**) with a default value of 6.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a804-108">備註</span><span class="sxs-lookup"><span data-stu-id="8a804-108">Remarks</span></span>

<span data-ttu-id="8a804-109">若要順暢地滾動， **scrollingAmount** 應該很小。</span><span class="sxs-lookup"><span data-stu-id="8a804-109">For smooth scrolling, **scrollingAmount** should be small.</span></span> <span data-ttu-id="8a804-110">針對具有顯著間距的快速繪圖， **scrollingAmount** 應該更大。</span><span class="sxs-lookup"><span data-stu-id="8a804-110">For fast drawing with big gaps, the **scrollingAmount** should be larger.</span></span> <span data-ttu-id="8a804-111">如果 **滾動** = "false"，則會忽略 **scrollingAmount** 。</span><span class="sxs-lookup"><span data-stu-id="8a804-111">If **scrolling** ="false", **scrollingAmount** is ignored.</span></span>

<span data-ttu-id="8a804-112">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="8a804-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a804-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a804-113">Requirements</span></span>



| <span data-ttu-id="8a804-114">需求</span><span class="sxs-lookup"><span data-stu-id="8a804-114">Requirement</span></span> | <span data-ttu-id="8a804-115">值</span><span class="sxs-lookup"><span data-stu-id="8a804-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8a804-116">版本</span><span class="sxs-lookup"><span data-stu-id="8a804-116">Version</span></span><br/> | <span data-ttu-id="8a804-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8a804-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a804-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a804-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a804-119">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="8a804-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="8a804-120">**文字。滾動**</span><span class="sxs-lookup"><span data-stu-id="8a804-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





