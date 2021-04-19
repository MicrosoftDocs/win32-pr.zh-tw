---
title: 文字。工具提示
description: ToolTip 屬性會指定或抓取文字控制項的工具提示文字。
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- 文字。工具提示 Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990200"
---
# <a name="texttooltip"></a><span data-ttu-id="7b9b9-104">文字。工具提示</span><span class="sxs-lookup"><span data-stu-id="7b9b9-104">TEXT.toolTip</span></span>

<span data-ttu-id="7b9b9-105">**Tooltip** 屬性會指定或抓取文字控制項的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="7b9b9-105">The **toolTip** attribute specifies or retrieves the ToolTip text for the text control.</span></span>

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a><span data-ttu-id="7b9b9-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="7b9b9-106">Possible Values</span></span>

<span data-ttu-id="7b9b9-107">此屬性是讀取/寫入 **字串** ，最大長度為1024個字元。</span><span class="sxs-lookup"><span data-stu-id="7b9b9-107">This attribute is a read/write **String** with a maximum length of 1024 characters.</span></span> <span data-ttu-id="7b9b9-108">它沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="7b9b9-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b9b9-109">備註</span><span class="sxs-lookup"><span data-stu-id="7b9b9-109">Remarks</span></span>

<span data-ttu-id="7b9b9-110">如果未指定這個屬性，而且 **值** 屬性中的文字在文字控制項中被截斷，或 **wordWrap** 設定為 True，則工具提示會顯示 **值** 屬性的全文檢索。</span><span class="sxs-lookup"><span data-stu-id="7b9b9-110">If this attribute is not specified, and the text in the **value** attribute is truncated in the Text control, or **wordWrap** is set to true, the ToolTip will display the full text of the **value** attribute.</span></span>

<span data-ttu-id="7b9b9-111">當這個屬性設定為 "" (空白字串) 時，不會顯示任何工具提示。</span><span class="sxs-lookup"><span data-stu-id="7b9b9-111">When this attribute is set to "" (empty string), no ToolTip is displayed.</span></span>

<span data-ttu-id="7b9b9-112">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="7b9b9-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9b9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b9b9-113">Requirements</span></span>



| <span data-ttu-id="7b9b9-114">需求</span><span class="sxs-lookup"><span data-stu-id="7b9b9-114">Requirement</span></span> | <span data-ttu-id="7b9b9-115">值</span><span class="sxs-lookup"><span data-stu-id="7b9b9-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7b9b9-116">版本</span><span class="sxs-lookup"><span data-stu-id="7b9b9-116">Version</span></span><br/> | <span data-ttu-id="7b9b9-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="7b9b9-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b9b9-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b9b9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9b9-119">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="7b9b9-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="7b9b9-120">**TEXT。值**</span><span class="sxs-lookup"><span data-stu-id="7b9b9-120">**TEXT.value**</span></span>](text-value.md)
</dt> <dt>

[<span data-ttu-id="7b9b9-121">**WordWrap**</span><span class="sxs-lookup"><span data-stu-id="7b9b9-121">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





