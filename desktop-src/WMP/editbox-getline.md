---
title: 編輯方塊. getLine
description: GetLine 方法會使用指定的索引來抓取行的文字。
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- 編輯方塊. getLine Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995199"
---
# <a name="editboxgetline"></a><span data-ttu-id="8559a-104">編輯方塊. getLine</span><span class="sxs-lookup"><span data-stu-id="8559a-104">EDITBOX.getLine</span></span>

<span data-ttu-id="8559a-105">**GetLine** 方法會使用指定的索引來抓取行的文字。</span><span class="sxs-lookup"><span data-stu-id="8559a-105">The **getLine** method retrieves the text for the line with the specified index.</span></span>

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a><span data-ttu-id="8559a-106">參數</span><span class="sxs-lookup"><span data-stu-id="8559a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8559a-107"><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="8559a-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="8559a-108">包含要取出的行之索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="8559a-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8559a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8559a-109">Return Value</span></span>

<span data-ttu-id="8559a-110">這個方法會傳回 **字串**。</span><span class="sxs-lookup"><span data-stu-id="8559a-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8559a-111">備註</span><span class="sxs-lookup"><span data-stu-id="8559a-111">Remarks</span></span>

<span data-ttu-id="8559a-112">如果索引無效，則會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="8559a-112">If the index is not valid, an empty string is returned.</span></span> <span data-ttu-id="8559a-113">只有在控制項變成可見之後，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8559a-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="8559a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8559a-114">Requirements</span></span>



| <span data-ttu-id="8559a-115">需求</span><span class="sxs-lookup"><span data-stu-id="8559a-115">Requirement</span></span> | <span data-ttu-id="8559a-116">值</span><span class="sxs-lookup"><span data-stu-id="8559a-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="8559a-117">版本</span><span class="sxs-lookup"><span data-stu-id="8559a-117">Version</span></span><br/> | <span data-ttu-id="8559a-118">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="8559a-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8559a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8559a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8559a-120">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="8559a-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="8559a-121">**編輯方塊. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="8559a-121">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="8559a-122">**編輯方塊. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="8559a-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





