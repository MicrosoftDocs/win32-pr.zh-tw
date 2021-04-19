---
title: BUTTONELEMENT。
description: 「粘滯」屬性（attribute）會指定或抓取值，指出 BUTTONELEMENT 是否為切換，也就是是否為雙狀態或單一狀態按鈕。
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT Windows Media Player 的不乾膠
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987168"
---
# <a name="buttonelementsticky"></a><span data-ttu-id="e395a-104">BUTTONELEMENT。</span><span class="sxs-lookup"><span data-stu-id="e395a-104">BUTTONELEMENT.sticky</span></span>

<span data-ttu-id="e395a-105">「 **粘滯** 」屬性（attribute）會指定或抓取值，指出 **BUTTONELEMENT** 是否為切換，也就是是否為雙狀態或單一狀態按鈕。</span><span class="sxs-lookup"><span data-stu-id="e395a-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="e395a-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="e395a-106">Possible Values</span></span>

<span data-ttu-id="e395a-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="e395a-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="e395a-108">值</span><span class="sxs-lookup"><span data-stu-id="e395a-108">Value</span></span> | <span data-ttu-id="e395a-109">描述</span><span class="sxs-lookup"><span data-stu-id="e395a-109">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="e395a-110">true</span><span class="sxs-lookup"><span data-stu-id="e395a-110">true</span></span>  | <span data-ttu-id="e395a-111">**BUTTONELEMENT** 為粘滯。</span><span class="sxs-lookup"><span data-stu-id="e395a-111">**BUTTONELEMENT** is sticky.</span></span>              |
| <span data-ttu-id="e395a-112">false</span><span class="sxs-lookup"><span data-stu-id="e395a-112">false</span></span> | <span data-ttu-id="e395a-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="e395a-113">Default.</span></span> <span data-ttu-id="e395a-114">**BUTTONELEMENT** 不是粘滯。</span><span class="sxs-lookup"><span data-stu-id="e395a-114">**BUTTONELEMENT** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e395a-115">備註</span><span class="sxs-lookup"><span data-stu-id="e395a-115">Remarks</span></span>

<span data-ttu-id="e395a-116">如果 [ **粘滯** ] 屬性設定為 [true]，當您按下按鈕時，按鈕元素將會變更為 [關閉] 狀態，且會維持在該狀態中，直到再次按一下為止。</span><span class="sxs-lookup"><span data-stu-id="e395a-116">If the **sticky** attribute is set to true, the button element will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="e395a-117">當 button 專案處於關閉狀態時， **向下** 屬性會是 true，而且會顯示按鈕群組 **downImage** 的適當部分。</span><span class="sxs-lookup"><span data-stu-id="e395a-117">When the button element is in the down state, the **down** attribute will be true and the appropriate portion of the button group **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e395a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e395a-118">Requirements</span></span>



| <span data-ttu-id="e395a-119">需求</span><span class="sxs-lookup"><span data-stu-id="e395a-119">Requirement</span></span> | <span data-ttu-id="e395a-120">值</span><span class="sxs-lookup"><span data-stu-id="e395a-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e395a-121">版本</span><span class="sxs-lookup"><span data-stu-id="e395a-121">Version</span></span><br/> | <span data-ttu-id="e395a-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="e395a-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e395a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e395a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e395a-124">**BUTTONELEMENT 元素**</span><span class="sxs-lookup"><span data-stu-id="e395a-124">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="e395a-125">**BUTTONELEMENT 向下**</span><span class="sxs-lookup"><span data-stu-id="e395a-125">**BUTTONELEMENT.down**</span></span>](buttonelement-down.md)
</dt> <dt>

[<span data-ttu-id="e395a-126">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="e395a-126">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> </dl>

 

 





