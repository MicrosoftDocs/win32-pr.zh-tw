---
title: BUTTONGROUP. showBackground
description: ShowBackground 屬性會指定或抓取值，指出 BUTTONGROUP 是否只顯示按鈕，或顯示影像屬性中指定的完整點陣圖。
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP. showBackground Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994233"
---
# <a name="buttongroupshowbackground"></a><span data-ttu-id="a4909-104">BUTTONGROUP. showBackground</span><span class="sxs-lookup"><span data-stu-id="a4909-104">BUTTONGROUP.showBackground</span></span>

<span data-ttu-id="a4909-105">**ShowBackground** 屬性會指定或抓取值，指出 **BUTTONGROUP** 是否只顯示按鈕，或顯示 **影像** 屬性中指定的完整點陣圖。</span><span class="sxs-lookup"><span data-stu-id="a4909-105">The **showBackground** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a><span data-ttu-id="a4909-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="a4909-106">Possible Values</span></span>

<span data-ttu-id="a4909-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="a4909-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a4909-108">值</span><span class="sxs-lookup"><span data-stu-id="a4909-108">Value</span></span> | <span data-ttu-id="a4909-109">描述</span><span class="sxs-lookup"><span data-stu-id="a4909-109">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4909-110">true</span><span class="sxs-lookup"><span data-stu-id="a4909-110">true</span></span>  | <span data-ttu-id="a4909-111">按鈕隨即顯示，而按鈕未佔用的區域則是從影像點陣圖繪製。</span><span class="sxs-lookup"><span data-stu-id="a4909-111">Buttons are displayed and the area not occupied by buttons is drawn from the Image bitmap.</span></span> |
| <span data-ttu-id="a4909-112">false</span><span class="sxs-lookup"><span data-stu-id="a4909-112">false</span></span> | <span data-ttu-id="a4909-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="a4909-113">Default.</span></span> <span data-ttu-id="a4909-114">只會顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="a4909-114">Only the buttons are displayed.</span></span>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="a4909-115">備註</span><span class="sxs-lookup"><span data-stu-id="a4909-115">Remarks</span></span>

<span data-ttu-id="a4909-116">當 **showBackground** 為 true 時，會顯示整個主要 **映射** 。</span><span class="sxs-lookup"><span data-stu-id="a4909-116">When **showBackground** is true, the entire main **image** will be visible.</span></span>

<span data-ttu-id="a4909-117">當 **showBackground** 為 false 時，只會轉譯對應至已指派 **mappingImage** 色彩的區域。</span><span class="sxs-lookup"><span data-stu-id="a4909-117">When **showBackground** is false, only the areas corresponding to assigned **mappingImage** colors will be rendered.</span></span> <span data-ttu-id="a4909-118">換句話說，只會顯示已指派 **mappingColor** 的 **BUTTONELEMENTs** 。</span><span class="sxs-lookup"><span data-stu-id="a4909-118">In other words, only **BUTTONELEMENTs** with their **mappingColor** assigned will be visible.</span></span>

<span data-ttu-id="a4909-119">如果指定了不正確值，則會維護先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4909-119">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4909-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4909-120">Requirements</span></span>



| <span data-ttu-id="a4909-121">需求</span><span class="sxs-lookup"><span data-stu-id="a4909-121">Requirement</span></span> | <span data-ttu-id="a4909-122">值</span><span class="sxs-lookup"><span data-stu-id="a4909-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a4909-123">版本</span><span class="sxs-lookup"><span data-stu-id="a4909-123">Version</span></span><br/> | <span data-ttu-id="a4909-124">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="a4909-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4909-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4909-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4909-126">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="a4909-126">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="a4909-127">**BUTTONELEMENT.mappingColor**</span><span class="sxs-lookup"><span data-stu-id="a4909-127">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="a4909-128">**BUTTONGROUP 影像**</span><span class="sxs-lookup"><span data-stu-id="a4909-128">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="a4909-129">**BUTTONGROUP. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="a4909-129">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





