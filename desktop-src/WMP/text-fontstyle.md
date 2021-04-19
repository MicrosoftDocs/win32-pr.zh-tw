---
title: FontStyle
description: FontStyle 屬性會指定或抓取文字控制項的字型樣式。
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- FontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982929"
---
# <a name="textfontstyle"></a><span data-ttu-id="c1d2c-104">FontStyle</span><span class="sxs-lookup"><span data-stu-id="c1d2c-104">TEXT.fontStyle</span></span>

<span data-ttu-id="c1d2c-105">**FontStyle** 屬性會指定或抓取文字控制項的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-105">The **fontStyle** attribute specifies or retrieves the font style for the Text control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="c1d2c-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="c1d2c-106">Possible Values</span></span>

<span data-ttu-id="c1d2c-107">這個屬性是包含下列一或多個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="c1d2c-108">值</span><span class="sxs-lookup"><span data-stu-id="c1d2c-108">Value</span></span>     | <span data-ttu-id="c1d2c-109">描述</span><span class="sxs-lookup"><span data-stu-id="c1d2c-109">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="c1d2c-110">粗體</span><span class="sxs-lookup"><span data-stu-id="c1d2c-110">Bold</span></span>      | <span data-ttu-id="c1d2c-111">粗體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-111">Bold font style.</span></span>            |
| <span data-ttu-id="c1d2c-112">斜體</span><span class="sxs-lookup"><span data-stu-id="c1d2c-112">Italic</span></span>    | <span data-ttu-id="c1d2c-113">斜體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-113">Italic font style.</span></span>          |
| <span data-ttu-id="c1d2c-114">Underline</span><span class="sxs-lookup"><span data-stu-id="c1d2c-114">Underline</span></span> | <span data-ttu-id="c1d2c-115">底線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-115">Underline font style.</span></span>       |
| <span data-ttu-id="c1d2c-116">帶</span><span class="sxs-lookup"><span data-stu-id="c1d2c-116">Strikeout</span></span> | <span data-ttu-id="c1d2c-117">刪除線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-117">Strikeout font style.</span></span>       |
| <span data-ttu-id="c1d2c-118">正常</span><span class="sxs-lookup"><span data-stu-id="c1d2c-118">Normal</span></span>    | <span data-ttu-id="c1d2c-119">預設值。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-119">Default.</span></span> <span data-ttu-id="c1d2c-120">一般字型樣式。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-120">Normal font style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c1d2c-121">備註</span><span class="sxs-lookup"><span data-stu-id="c1d2c-121">Remarks</span></span>

<span data-ttu-id="c1d2c-122">您可以使用值的任何組合，並以空格分隔。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-122">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="c1d2c-123">標準樣式的優先順序會高於所有其他值，而且會忽略任何其他指定的標準。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-123">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="c1d2c-124">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="c1d2c-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d2c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1d2c-125">Requirements</span></span>



| <span data-ttu-id="c1d2c-126">需求</span><span class="sxs-lookup"><span data-stu-id="c1d2c-126">Requirement</span></span> | <span data-ttu-id="c1d2c-127">值</span><span class="sxs-lookup"><span data-stu-id="c1d2c-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c1d2c-128">版本</span><span class="sxs-lookup"><span data-stu-id="c1d2c-128">Version</span></span><br/> | <span data-ttu-id="c1d2c-129">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1d2c-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1d2c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1d2c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d2c-131">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="c1d2c-131">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





