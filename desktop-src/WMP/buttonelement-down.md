---
title: BUTTONELEMENT 向下
description: 向下屬性會指定或抓取值，指出 button 元素在上或下移位置。
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987163"
---
# <a name="buttonelementdown"></a><span data-ttu-id="5638c-104">BUTTONELEMENT 向下</span><span class="sxs-lookup"><span data-stu-id="5638c-104">BUTTONELEMENT.down</span></span>

<span data-ttu-id="5638c-105">**向下** 屬性會指定或抓取值，指出 button 元素在上或下移位置。</span><span class="sxs-lookup"><span data-stu-id="5638c-105">The **down** attribute specifies or retrieves a value indicating whether the button element is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="5638c-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="5638c-106">Possible Values</span></span>

<span data-ttu-id="5638c-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="5638c-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="5638c-108">值</span><span class="sxs-lookup"><span data-stu-id="5638c-108">Value</span></span> | <span data-ttu-id="5638c-109">描述</span><span class="sxs-lookup"><span data-stu-id="5638c-109">Description</span></span>                                                     |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="5638c-110">true</span><span class="sxs-lookup"><span data-stu-id="5638c-110">true</span></span>  | <span data-ttu-id="5638c-111">表示 **BUTTONELEMENT** 在下的位置。</span><span class="sxs-lookup"><span data-stu-id="5638c-111">Indicates the **BUTTONELEMENT** is in the down position.</span></span>        |
| <span data-ttu-id="5638c-112">false</span><span class="sxs-lookup"><span data-stu-id="5638c-112">false</span></span> | <span data-ttu-id="5638c-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="5638c-113">Default.</span></span> <span data-ttu-id="5638c-114">表示 **BUTTONELEMENT** 在上的位置。</span><span class="sxs-lookup"><span data-stu-id="5638c-114">Indicates the **BUTTONELEMENT** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5638c-115">備註</span><span class="sxs-lookup"><span data-stu-id="5638c-115">Remarks</span></span>

<span data-ttu-id="5638c-116">若要讓按鈕元素保持在關閉位置，必須將 [ **粘滯** ] 設定為 [true]。</span><span class="sxs-lookup"><span data-stu-id="5638c-116">For a button element to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="5638c-117">依預設，[ **粘滯** ] 為 false，而任何設定為 [true **] 的嘗試** 都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="5638c-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="5638c-118">如果指定了不正確值，則會維護先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="5638c-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="5638c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5638c-119">Requirements</span></span>



| <span data-ttu-id="5638c-120">需求</span><span class="sxs-lookup"><span data-stu-id="5638c-120">Requirement</span></span> | <span data-ttu-id="5638c-121">值</span><span class="sxs-lookup"><span data-stu-id="5638c-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5638c-122">版本</span><span class="sxs-lookup"><span data-stu-id="5638c-122">Version</span></span><br/> | <span data-ttu-id="5638c-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="5638c-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5638c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5638c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5638c-125">**BUTTONELEMENT 元素**</span><span class="sxs-lookup"><span data-stu-id="5638c-125">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="5638c-126">**BUTTONELEMENT.downToolTip**</span><span class="sxs-lookup"><span data-stu-id="5638c-126">**BUTTONELEMENT.downToolTip**</span></span>](buttonelement-downtooltip.md)
</dt> </dl>

 

 





