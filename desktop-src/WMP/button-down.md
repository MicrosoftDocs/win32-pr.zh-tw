---
title: 按鈕。向下鍵
description: 向下屬性會指定或抓取值，指出按鈕是否在上或向下位置。
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- 按鈕。關閉 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979440"
---
# <a name="buttondown"></a><span data-ttu-id="1e9fb-104">按鈕。向下鍵</span><span class="sxs-lookup"><span data-stu-id="1e9fb-104">BUTTON.down</span></span>

<span data-ttu-id="1e9fb-105">**向下** 屬性會指定或抓取值，指出 **按鈕** 是否在上或向下位置。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-105">The **down** attribute specifies or retrieves a value indicating whether the **BUTTON** is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="1e9fb-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="1e9fb-106">Possible Values</span></span>

<span data-ttu-id="1e9fb-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1e9fb-108">值</span><span class="sxs-lookup"><span data-stu-id="1e9fb-108">Value</span></span> | <span data-ttu-id="1e9fb-109">描述</span><span class="sxs-lookup"><span data-stu-id="1e9fb-109">Description</span></span>                                                   |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="1e9fb-110">true</span><span class="sxs-lookup"><span data-stu-id="1e9fb-110">true</span></span>  | <span data-ttu-id="1e9fb-111">指出 **按鈕** 位於下位置。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-111">Indicates that the **BUTTON** is in the down position.</span></span>        |
| <span data-ttu-id="1e9fb-112">false</span><span class="sxs-lookup"><span data-stu-id="1e9fb-112">false</span></span> | <span data-ttu-id="1e9fb-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-113">Default.</span></span> <span data-ttu-id="1e9fb-114">指出 **按鈕** 在上的位置。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-114">Indicates that the **BUTTON** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1e9fb-115">備註</span><span class="sxs-lookup"><span data-stu-id="1e9fb-115">Remarks</span></span>

<span data-ttu-id="1e9fb-116">若要讓 **按鈕** 保持在關閉位置，必須將 [ **粘滯** ] 設定為 [true]。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-116">For a **BUTTON** to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="1e9fb-117">依預設，[ **粘滯** ] 為 false，而任何設定為 [true **] 的嘗試** 都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="1e9fb-118">如果指定了不正確值，則會維護先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="1e9fb-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9fb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e9fb-119">Requirements</span></span>



| <span data-ttu-id="1e9fb-120">需求</span><span class="sxs-lookup"><span data-stu-id="1e9fb-120">Requirement</span></span> | <span data-ttu-id="1e9fb-121">值</span><span class="sxs-lookup"><span data-stu-id="1e9fb-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1e9fb-122">版本</span><span class="sxs-lookup"><span data-stu-id="1e9fb-122">Version</span></span><br/> | <span data-ttu-id="1e9fb-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="1e9fb-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e9fb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e9fb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9fb-125">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="1e9fb-125">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="1e9fb-126">**按鈕. downImage**</span><span class="sxs-lookup"><span data-stu-id="1e9fb-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> <dt>

[<span data-ttu-id="1e9fb-127">**按鈕. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="1e9fb-127">**BUTTON.downToolTip**</span></span>](button-downtooltip.md)
</dt> </dl>

 

 





