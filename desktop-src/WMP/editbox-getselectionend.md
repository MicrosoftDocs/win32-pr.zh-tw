---
title: 編輯方塊. getSelectionEnd
description: GetSelectionEnd 方法會抓取編輯方塊控制項中所選取文字的結束位置。
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- 編輯方塊. getSelectionEnd Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001230"
---
# <a name="editboxgetselectionend"></a><span data-ttu-id="de56d-104">編輯方塊. getSelectionEnd</span><span class="sxs-lookup"><span data-stu-id="de56d-104">EDITBOX.getSelectionEnd</span></span>

<span data-ttu-id="de56d-105">**GetSelectionEnd** 方法會抓取編輯方塊控制項中所選取文字的結束位置。</span><span class="sxs-lookup"><span data-stu-id="de56d-105">The **getSelectionEnd** method retrieves the ending position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a><span data-ttu-id="de56d-106">參數</span><span class="sxs-lookup"><span data-stu-id="de56d-106">Parameters</span></span>

<span data-ttu-id="de56d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="de56d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de56d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="de56d-108">Return Value</span></span>

<span data-ttu-id="de56d-109">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="de56d-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="de56d-110">備註</span><span class="sxs-lookup"><span data-stu-id="de56d-110">Remarks</span></span>

<span data-ttu-id="de56d-111">如果未選取任何文字，這個方法會傳回插入點的位置。</span><span class="sxs-lookup"><span data-stu-id="de56d-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="de56d-112">如果控制項是多行，此方法會傳回控制項中的字元索引，而不是行索引。</span><span class="sxs-lookup"><span data-stu-id="de56d-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="de56d-113">只有在控制項變成可見之後，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="de56d-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="de56d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="de56d-114">Requirements</span></span>



| <span data-ttu-id="de56d-115">需求</span><span class="sxs-lookup"><span data-stu-id="de56d-115">Requirement</span></span> | <span data-ttu-id="de56d-116">值</span><span class="sxs-lookup"><span data-stu-id="de56d-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="de56d-117">版本</span><span class="sxs-lookup"><span data-stu-id="de56d-117">Version</span></span><br/> | <span data-ttu-id="de56d-118">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="de56d-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de56d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de56d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de56d-120">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="de56d-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="de56d-121">**編輯方塊. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="de56d-121">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="de56d-122">**編輯方塊. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="de56d-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="de56d-123">**編輯方塊. setSelection**</span><span class="sxs-lookup"><span data-stu-id="de56d-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





