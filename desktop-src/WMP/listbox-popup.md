---
title: LISTBOX. popUp
description: PopUp 屬性指定一個值，指出專案是否代表 popUp 或清單方塊控制項。
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976060"
---
# <a name="listboxpopup"></a><span data-ttu-id="60862-104">LISTBOX. popUp</span><span class="sxs-lookup"><span data-stu-id="60862-104">LISTBOX.popUp</span></span>

<span data-ttu-id="60862-105">**PopUp** 屬性指定一個值，指出專案是否代表 popUp 或清單方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="60862-105">The **popUp** attribute specifies a value indicating whether the element represents a popup or list box control.</span></span>

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a><span data-ttu-id="60862-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="60862-106">Possible Values</span></span>

<span data-ttu-id="60862-107">這個屬性是在設計階段指定的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="60862-107">This attribute is a **Boolean** specified at design time only.</span></span>



| <span data-ttu-id="60862-108">值</span><span class="sxs-lookup"><span data-stu-id="60862-108">Value</span></span> | <span data-ttu-id="60862-109">描述</span><span class="sxs-lookup"><span data-stu-id="60862-109">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="60862-110">true</span><span class="sxs-lookup"><span data-stu-id="60862-110">true</span></span>  | <span data-ttu-id="60862-111">元素代表 popup 控制項。</span><span class="sxs-lookup"><span data-stu-id="60862-111">The element represents a popup control.</span></span>    |
| <span data-ttu-id="60862-112">false</span><span class="sxs-lookup"><span data-stu-id="60862-112">false</span></span> | <span data-ttu-id="60862-113">元素代表清單方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="60862-113">The element represents a list box control.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="60862-114">備註</span><span class="sxs-lookup"><span data-stu-id="60862-114">Remarks</span></span>

<span data-ttu-id="60862-115">**POPUP** 元素表示只有在需要時才會顯示的清單方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="60862-115">The **POPUP** element represents a list box control that is displayed only when needed.</span></span> <span data-ttu-id="60862-116">它與 **LISTBOX** 元素相同，但這個屬性的預設值除外，後者會變更顯示行為。</span><span class="sxs-lookup"><span data-stu-id="60862-116">It is identical to the **LISTBOX** element except for the default value of this attribute, which changes the display behavior.</span></span> <span data-ttu-id="60862-117">若為 **LISTBOX** 元素，預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="60862-117">For **LISTBOX** elements, the default value is false.</span></span> <span data-ttu-id="60862-118">針對 **POPUP** 元素，預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="60862-118">For **POPUP** elements, the default value is true.</span></span> <span data-ttu-id="60862-119">**LISTBOX** 或 **POPUP** 元素應該根據所需的行為來使用，而不是指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="60862-119">Instead of specifying this attribute, the **LISTBOX** or **POPUP** element should be used to according to the desired behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="60862-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="60862-120">Requirements</span></span>



| <span data-ttu-id="60862-121">需求</span><span class="sxs-lookup"><span data-stu-id="60862-121">Requirement</span></span> | <span data-ttu-id="60862-122">值</span><span class="sxs-lookup"><span data-stu-id="60862-122">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="60862-123">版本</span><span class="sxs-lookup"><span data-stu-id="60862-123">Version</span></span><br/> | <span data-ttu-id="60862-124">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="60862-124">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60862-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60862-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60862-126">**LISTBOX 元素**</span><span class="sxs-lookup"><span data-stu-id="60862-126">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="60862-127">**POPUP 元素**</span><span class="sxs-lookup"><span data-stu-id="60862-127">**POPUP Element**</span></span>](popup-element.md)
</dt> </dl>

 

 





