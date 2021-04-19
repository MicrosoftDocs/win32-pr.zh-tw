---
title: 編輯方塊. setSelection
description: SetSelection 方法會從指定的開始索引到指定的結束索引，選取編輯方塊控制項中的文字。
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- 編輯方塊. setSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000710"
---
# <a name="editboxsetselection"></a><span data-ttu-id="a6a9e-104">編輯方塊. setSelection</span><span class="sxs-lookup"><span data-stu-id="a6a9e-104">EDITBOX.setSelection</span></span>

<span data-ttu-id="a6a9e-105">**SetSelection** 方法會從指定的開始索引到指定的結束索引，選取編輯方塊控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="a6a9e-105">The **setSelection** method selects the text in the edit box control from the specified start index to the specified end index.</span></span>

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a><span data-ttu-id="a6a9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="a6a9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a9e-107"><span id="start"></span><span id="START"></span>*開始*</span><span class="sxs-lookup"><span data-stu-id="a6a9e-107"><span id="start"></span><span id="START"></span>*start*</span></span>
</dt> <dd>

<span data-ttu-id="a6a9e-108">**Number** (**Long**) ，其中包含所選取文字之開始位置的字元索引。</span><span class="sxs-lookup"><span data-stu-id="a6a9e-108">**Number** (**long**) containing the character index of the starting position of the selected text.</span></span>

</dd> <dt>

<span data-ttu-id="a6a9e-109"><span id="end"></span><span id="END"></span>*結束*</span><span class="sxs-lookup"><span data-stu-id="a6a9e-109"><span id="end"></span><span id="END"></span>*end*</span></span>
</dt> <dd>

<span data-ttu-id="a6a9e-110">**Number** (**Long**) ，其中包含所選取文字結束位置的字元索引。</span><span class="sxs-lookup"><span data-stu-id="a6a9e-110">**Number** (**long**) containing the character index of the ending position of the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a9e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6a9e-111">Return Value</span></span>

<span data-ttu-id="a6a9e-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a6a9e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a9e-113">備註</span><span class="sxs-lookup"><span data-stu-id="a6a9e-113">Remarks</span></span>

<span data-ttu-id="a6a9e-114">如果 [開始] 為0且結尾是1，則會選取 [編輯方塊] 控制項中的所有文字。</span><span class="sxs-lookup"><span data-stu-id="a6a9e-114">If the start is 0 and the end is  1, all of the text in the edit box control is selected.</span></span> <span data-ttu-id="a6a9e-115">如果啟動是1，則會取消選取任何目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="a6a9e-115">If the start is  1, any current selection is deselected.</span></span>

<span data-ttu-id="a6a9e-116">只有在控制項變成可見之後，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a6a9e-116">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a9e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6a9e-117">Requirements</span></span>



| <span data-ttu-id="a6a9e-118">需求</span><span class="sxs-lookup"><span data-stu-id="a6a9e-118">Requirement</span></span> | <span data-ttu-id="a6a9e-119">值</span><span class="sxs-lookup"><span data-stu-id="a6a9e-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="a6a9e-120">版本</span><span class="sxs-lookup"><span data-stu-id="a6a9e-120">Version</span></span><br/> | <span data-ttu-id="a6a9e-121">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="a6a9e-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6a9e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6a9e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a9e-123">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="a6a9e-123">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="a6a9e-124">**編輯方塊. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="a6a9e-124">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="a6a9e-125">**編輯方塊. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="a6a9e-125">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="a6a9e-126">**編輯方塊. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="a6a9e-126">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> </dl>

 

 





