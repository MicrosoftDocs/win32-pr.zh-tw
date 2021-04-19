---
title: LISTBOX. fontStyle
description: FontStyle 屬性會指定或抓取清單方塊控制項的字型樣式。
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984055"
---
# <a name="listboxfontstyle"></a><span data-ttu-id="170e6-104">LISTBOX. fontStyle</span><span class="sxs-lookup"><span data-stu-id="170e6-104">LISTBOX.fontStyle</span></span>

<span data-ttu-id="170e6-105">**FontStyle** 屬性會指定或抓取清單方塊控制項的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="170e6-105">The **fontStyle** attribute specifies or retrieves the font style for the list box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="170e6-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="170e6-106">Possible Values</span></span>

<span data-ttu-id="170e6-107">這個屬性是包含下列一或多個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="170e6-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="170e6-108">值</span><span class="sxs-lookup"><span data-stu-id="170e6-108">Value</span></span>     | <span data-ttu-id="170e6-109">描述</span><span class="sxs-lookup"><span data-stu-id="170e6-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="170e6-110">粗體</span><span class="sxs-lookup"><span data-stu-id="170e6-110">Bold</span></span>      | <span data-ttu-id="170e6-111">粗體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="170e6-111">Bold font style.</span></span>      |
| <span data-ttu-id="170e6-112">斜體</span><span class="sxs-lookup"><span data-stu-id="170e6-112">Italic</span></span>    | <span data-ttu-id="170e6-113">斜體字型樣式。</span><span class="sxs-lookup"><span data-stu-id="170e6-113">Italic font style.</span></span>    |
| <span data-ttu-id="170e6-114">Underline</span><span class="sxs-lookup"><span data-stu-id="170e6-114">Underline</span></span> | <span data-ttu-id="170e6-115">底線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="170e6-115">Underline font style.</span></span> |
| <span data-ttu-id="170e6-116">帶</span><span class="sxs-lookup"><span data-stu-id="170e6-116">Strikeout</span></span> | <span data-ttu-id="170e6-117">刪除線字型樣式。</span><span class="sxs-lookup"><span data-stu-id="170e6-117">Strikeout font style.</span></span> |
| <span data-ttu-id="170e6-118">正常</span><span class="sxs-lookup"><span data-stu-id="170e6-118">Normal</span></span>    | <span data-ttu-id="170e6-119">一般字型樣式。</span><span class="sxs-lookup"><span data-stu-id="170e6-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="170e6-120">備註</span><span class="sxs-lookup"><span data-stu-id="170e6-120">Remarks</span></span>

<span data-ttu-id="170e6-121">您可以使用值的任何組合，並以空格分隔。</span><span class="sxs-lookup"><span data-stu-id="170e6-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="170e6-122">標準樣式的優先順序會高於所有其他值，而且會忽略任何其他指定的標準。</span><span class="sxs-lookup"><span data-stu-id="170e6-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="170e6-123">基於轉譯目的，Normal 是預設字型樣式。</span><span class="sxs-lookup"><span data-stu-id="170e6-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="170e6-124">從此屬性抓取的預設值為 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="170e6-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="170e6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="170e6-125">Requirements</span></span>



| <span data-ttu-id="170e6-126">需求</span><span class="sxs-lookup"><span data-stu-id="170e6-126">Requirement</span></span> | <span data-ttu-id="170e6-127">值</span><span class="sxs-lookup"><span data-stu-id="170e6-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="170e6-128">版本</span><span class="sxs-lookup"><span data-stu-id="170e6-128">Version</span></span><br/> | <span data-ttu-id="170e6-129">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="170e6-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="170e6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="170e6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="170e6-131">**LISTBOX 元素**</span><span class="sxs-lookup"><span data-stu-id="170e6-131">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="170e6-132">**LISTBOX. fontSize**</span><span class="sxs-lookup"><span data-stu-id="170e6-132">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> </dl>

 

 





