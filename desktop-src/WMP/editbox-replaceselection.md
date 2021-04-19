---
title: 編輯方塊. replaceSelection
description: ReplaceSelection 方法會以指定的文字取代目前的選取範圍。
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- 編輯方塊. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997676"
---
# <a name="editboxreplaceselection"></a><span data-ttu-id="bb58a-104">編輯方塊. replaceSelection</span><span class="sxs-lookup"><span data-stu-id="bb58a-104">EDITBOX.replaceSelection</span></span>

<span data-ttu-id="bb58a-105">**ReplaceSelection** 方法會以指定的文字取代目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="bb58a-105">The **replaceSelection** method replaces the current selection with the specified text.</span></span>

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a><span data-ttu-id="bb58a-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb58a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb58a-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span><span class="sxs-lookup"><span data-stu-id="bb58a-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span></span>
</dt> <dd>

<span data-ttu-id="bb58a-108">**字串** ，包含要取代所選取文字的文字。</span><span class="sxs-lookup"><span data-stu-id="bb58a-108">**String** containing the text to replace the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb58a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb58a-109">Return Value</span></span>

<span data-ttu-id="bb58a-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bb58a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb58a-111">備註</span><span class="sxs-lookup"><span data-stu-id="bb58a-111">Remarks</span></span>

<span data-ttu-id="bb58a-112">如果未選取任何文字，則會將取代文字插入插入點的目前位置。</span><span class="sxs-lookup"><span data-stu-id="bb58a-112">If there is no text selected, the replacement text is inserted at the current location of the insertion point.</span></span>

<span data-ttu-id="bb58a-113">只有在控制項變成可見之後，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="bb58a-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb58a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb58a-114">Requirements</span></span>



| <span data-ttu-id="bb58a-115">需求</span><span class="sxs-lookup"><span data-stu-id="bb58a-115">Requirement</span></span> | <span data-ttu-id="bb58a-116">值</span><span class="sxs-lookup"><span data-stu-id="bb58a-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="bb58a-117">版本</span><span class="sxs-lookup"><span data-stu-id="bb58a-117">Version</span></span><br/> | <span data-ttu-id="bb58a-118">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bb58a-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb58a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb58a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb58a-120">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="bb58a-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="bb58a-121">**編輯方塊. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="bb58a-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="bb58a-122">**編輯方塊. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="bb58a-122">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="bb58a-123">**編輯方塊. setSelection**</span><span class="sxs-lookup"><span data-stu-id="bb58a-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





