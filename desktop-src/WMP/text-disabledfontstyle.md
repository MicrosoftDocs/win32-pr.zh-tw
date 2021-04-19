---
title: DisabledFontStyle
description: DisabledFontStyle 屬性會指定或抓取文字控制項停用時所用的字型樣式。
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- DisabledFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998880"
---
# <a name="textdisabledfontstyle"></a><span data-ttu-id="ac2a1-104">DisabledFontStyle</span><span class="sxs-lookup"><span data-stu-id="ac2a1-104">TEXT.disabledFontStyle</span></span>

<span data-ttu-id="ac2a1-105">**DisabledFontStyle** 屬性會指定或抓取文字控制項停用時所用的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-105">The **disabledFontStyle** attribute specifies or retrieves the font style used for the Text control when it is disabled.</span></span>

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="ac2a1-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="ac2a1-106">Possible Values</span></span>

<span data-ttu-id="ac2a1-107">這個屬性是包含下列一或多個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="ac2a1-108">值</span><span class="sxs-lookup"><span data-stu-id="ac2a1-108">Value</span></span>     | <span data-ttu-id="ac2a1-109">描述</span><span class="sxs-lookup"><span data-stu-id="ac2a1-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="ac2a1-110">粗體</span><span class="sxs-lookup"><span data-stu-id="ac2a1-110">Bold</span></span>      | <span data-ttu-id="ac2a1-111">粗體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-111">Bold font style.</span></span>      |
| <span data-ttu-id="ac2a1-112">斜體</span><span class="sxs-lookup"><span data-stu-id="ac2a1-112">Italic</span></span>    | <span data-ttu-id="ac2a1-113">斜體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-113">Italic font style.</span></span>    |
| <span data-ttu-id="ac2a1-114">Underline</span><span class="sxs-lookup"><span data-stu-id="ac2a1-114">Underline</span></span> | <span data-ttu-id="ac2a1-115">底線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-115">Underline font style.</span></span> |
| <span data-ttu-id="ac2a1-116">帶</span><span class="sxs-lookup"><span data-stu-id="ac2a1-116">Strikeout</span></span> | <span data-ttu-id="ac2a1-117">刪除線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-117">Strikeout font style.</span></span> |
| <span data-ttu-id="ac2a1-118">正常</span><span class="sxs-lookup"><span data-stu-id="ac2a1-118">Normal</span></span>    | <span data-ttu-id="ac2a1-119">一般字型樣式。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="ac2a1-120">備註</span><span class="sxs-lookup"><span data-stu-id="ac2a1-120">Remarks</span></span>

<span data-ttu-id="ac2a1-121">您可以使用值的任何組合，並以空格分隔。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="ac2a1-122">標準樣式的優先順序會高於所有其他值，而且會忽略任何其他指定的標準。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="ac2a1-123">如果未指定 **disabledFontStyle** ，則會使用 **fontStyle** 。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-123">If **disabledFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="ac2a1-124">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="ac2a1-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2a1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac2a1-125">Requirements</span></span>



| <span data-ttu-id="ac2a1-126">需求</span><span class="sxs-lookup"><span data-stu-id="ac2a1-126">Requirement</span></span> | <span data-ttu-id="ac2a1-127">值</span><span class="sxs-lookup"><span data-stu-id="ac2a1-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ac2a1-128">版本</span><span class="sxs-lookup"><span data-stu-id="ac2a1-128">Version</span></span><br/> | <span data-ttu-id="ac2a1-129">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="ac2a1-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac2a1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac2a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2a1-131">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="ac2a1-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="ac2a1-132">**FontStyle**</span><span class="sxs-lookup"><span data-stu-id="ac2a1-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





