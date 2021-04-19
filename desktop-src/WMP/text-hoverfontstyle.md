---
title: HoverFontStyle
description: 當滑鼠游標停留在文字控制項上方時，hoverFontStyle 屬性會指定或抓取文字控制項所使用的字型樣式。
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- HoverFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000721"
---
# <a name="texthoverfontstyle"></a><span data-ttu-id="3ea27-104">HoverFontStyle</span><span class="sxs-lookup"><span data-stu-id="3ea27-104">TEXT.hoverFontStyle</span></span>

<span data-ttu-id="3ea27-105">當滑鼠游標停留在文字控制項上方時， **hoverFontStyle** 屬性會指定或抓取文字控制項所使用的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="3ea27-105">The **hoverFontStyle** attribute specifies or retrieves the font style used for the Text control when the mouse cursor hovers over it.</span></span>

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="3ea27-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="3ea27-106">Possible Values</span></span>

<span data-ttu-id="3ea27-107">這個屬性是包含下列一或多個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="3ea27-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="3ea27-108">值</span><span class="sxs-lookup"><span data-stu-id="3ea27-108">Value</span></span>     | <span data-ttu-id="3ea27-109">描述</span><span class="sxs-lookup"><span data-stu-id="3ea27-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="3ea27-110">粗體</span><span class="sxs-lookup"><span data-stu-id="3ea27-110">Bold</span></span>      | <span data-ttu-id="3ea27-111">粗體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="3ea27-111">Bold font style.</span></span>      |
| <span data-ttu-id="3ea27-112">斜體</span><span class="sxs-lookup"><span data-stu-id="3ea27-112">Italic</span></span>    | <span data-ttu-id="3ea27-113">斜體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="3ea27-113">Italic font style.</span></span>    |
| <span data-ttu-id="3ea27-114">Underline</span><span class="sxs-lookup"><span data-stu-id="3ea27-114">Underline</span></span> | <span data-ttu-id="3ea27-115">底線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="3ea27-115">Underline font style.</span></span> |
| <span data-ttu-id="3ea27-116">帶</span><span class="sxs-lookup"><span data-stu-id="3ea27-116">Strikeout</span></span> | <span data-ttu-id="3ea27-117">刪除線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="3ea27-117">Strikeout font style.</span></span> |
| <span data-ttu-id="3ea27-118">正常</span><span class="sxs-lookup"><span data-stu-id="3ea27-118">Normal</span></span>    | <span data-ttu-id="3ea27-119">一般字型樣式。</span><span class="sxs-lookup"><span data-stu-id="3ea27-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="3ea27-120">備註</span><span class="sxs-lookup"><span data-stu-id="3ea27-120">Remarks</span></span>

<span data-ttu-id="3ea27-121">您可以使用值的任何組合，並以空格分隔。</span><span class="sxs-lookup"><span data-stu-id="3ea27-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="3ea27-122">標準樣式的優先順序會高於所有其他值，而且會忽略任何其他指定的標準。</span><span class="sxs-lookup"><span data-stu-id="3ea27-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="3ea27-123">如果未指定 **hoverFontStyle** ，則會使用 **fontStyle** 。</span><span class="sxs-lookup"><span data-stu-id="3ea27-123">If **hoverFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="3ea27-124">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="3ea27-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ea27-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ea27-125">Requirements</span></span>



| <span data-ttu-id="3ea27-126">需求</span><span class="sxs-lookup"><span data-stu-id="3ea27-126">Requirement</span></span> | <span data-ttu-id="3ea27-127">值</span><span class="sxs-lookup"><span data-stu-id="3ea27-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3ea27-128">版本</span><span class="sxs-lookup"><span data-stu-id="3ea27-128">Version</span></span><br/> | <span data-ttu-id="3ea27-129">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="3ea27-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ea27-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ea27-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea27-131">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="3ea27-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="3ea27-132">**FontStyle**</span><span class="sxs-lookup"><span data-stu-id="3ea27-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





