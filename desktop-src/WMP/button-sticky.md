---
title: 按鈕。粘滯
description: 「粘滯」屬性（attribute）會指定或抓取值，指出按鈕是否為切換，也就是是否為雙狀態或單一狀態按鈕。
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- 按鈕。粘滯 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990034"
---
# <a name="buttonsticky"></a><span data-ttu-id="b1c4a-104">按鈕。粘滯</span><span class="sxs-lookup"><span data-stu-id="b1c4a-104">BUTTON.sticky</span></span>

<span data-ttu-id="b1c4a-105">「 **粘滯** 」屬性（attribute）會指定或抓取值，指出 **按鈕** 是否為切換，也就是是否為雙狀態或單一狀態 **按鈕**。</span><span class="sxs-lookup"><span data-stu-id="b1c4a-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTON** is a toggle, that is, whether it is a two-state or single-state **BUTTON**.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="b1c4a-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="b1c4a-106">Possible Values</span></span>

<span data-ttu-id="b1c4a-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="b1c4a-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b1c4a-108">值</span><span class="sxs-lookup"><span data-stu-id="b1c4a-108">Value</span></span> | <span data-ttu-id="b1c4a-109">描述</span><span class="sxs-lookup"><span data-stu-id="b1c4a-109">Description</span></span>                        |
|-------|------------------------------------|
| <span data-ttu-id="b1c4a-110">true</span><span class="sxs-lookup"><span data-stu-id="b1c4a-110">true</span></span>  | <span data-ttu-id="b1c4a-111">**按鈕** 為粘滯。</span><span class="sxs-lookup"><span data-stu-id="b1c4a-111">**BUTTON** is sticky.</span></span>              |
| <span data-ttu-id="b1c4a-112">false</span><span class="sxs-lookup"><span data-stu-id="b1c4a-112">false</span></span> | <span data-ttu-id="b1c4a-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="b1c4a-113">Default.</span></span> <span data-ttu-id="b1c4a-114">**按鈕** 不是相黏鍵。</span><span class="sxs-lookup"><span data-stu-id="b1c4a-114">**BUTTON** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b1c4a-115">備註</span><span class="sxs-lookup"><span data-stu-id="b1c4a-115">Remarks</span></span>

<span data-ttu-id="b1c4a-116">如果 [ **粘滯** ] 設定為 [true]，當您按下按鈕時， **按鈕** 將會變更為 [關閉] 狀態，直到再次按一下為止。</span><span class="sxs-lookup"><span data-stu-id="b1c4a-116">If **sticky** is set to true, the **BUTTON** will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="b1c4a-117">當 **按鈕** 處於關閉狀態時， **向下** 屬性會是 true，而且會顯示 **downImage** 。</span><span class="sxs-lookup"><span data-stu-id="b1c4a-117">When the **BUTTON** is in the down state, the **down** attribute will be true and the **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1c4a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1c4a-118">Requirements</span></span>



| <span data-ttu-id="b1c4a-119">需求</span><span class="sxs-lookup"><span data-stu-id="b1c4a-119">Requirement</span></span> | <span data-ttu-id="b1c4a-120">值</span><span class="sxs-lookup"><span data-stu-id="b1c4a-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b1c4a-121">版本</span><span class="sxs-lookup"><span data-stu-id="b1c4a-121">Version</span></span><br/> | <span data-ttu-id="b1c4a-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b1c4a-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1c4a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1c4a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1c4a-124">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="b1c4a-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="b1c4a-125">**按鈕。向下鍵**</span><span class="sxs-lookup"><span data-stu-id="b1c4a-125">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="b1c4a-126">**按鈕. downImage**</span><span class="sxs-lookup"><span data-stu-id="b1c4a-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





