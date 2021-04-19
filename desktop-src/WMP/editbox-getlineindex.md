---
title: 編輯方塊. getLineIndex
description: GetLineIndex 方法會使用指定的行索引，來抓取行第一個字元的字元索引。
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- 編輯方塊. getLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996111"
---
# <a name="editboxgetlineindex"></a><span data-ttu-id="21a05-104">編輯方塊. getLineIndex</span><span class="sxs-lookup"><span data-stu-id="21a05-104">EDITBOX.getLineIndex</span></span>

<span data-ttu-id="21a05-105">**GetLineIndex** 方法會使用指定的行索引，來抓取行第一個字元的字元索引。</span><span class="sxs-lookup"><span data-stu-id="21a05-105">The **getLineIndex** method retrieves the character index of the first character on the line with the specified line index.</span></span>

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a><span data-ttu-id="21a05-106">參數</span><span class="sxs-lookup"><span data-stu-id="21a05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21a05-107"><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="21a05-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="21a05-108">**Number** (**Long**) ，其中包含要抓取其字元索引的行索引。</span><span class="sxs-lookup"><span data-stu-id="21a05-108">**Number** (**long**) containing the index of the line whose character index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21a05-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="21a05-109">Return Value</span></span>

<span data-ttu-id="21a05-110">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="21a05-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="21a05-111">備註</span><span class="sxs-lookup"><span data-stu-id="21a05-111">Remarks</span></span>

<span data-ttu-id="21a05-112">如果指定的行索引是1，則會使用包含插入點的行。</span><span class="sxs-lookup"><span data-stu-id="21a05-112">If the specified line index is  1, the line containing the insertion point is used.</span></span>

<span data-ttu-id="21a05-113">只有在控制項變成可見之後，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="21a05-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a05-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="21a05-114">Requirements</span></span>



| <span data-ttu-id="21a05-115">需求</span><span class="sxs-lookup"><span data-stu-id="21a05-115">Requirement</span></span> | <span data-ttu-id="21a05-116">值</span><span class="sxs-lookup"><span data-stu-id="21a05-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="21a05-117">版本</span><span class="sxs-lookup"><span data-stu-id="21a05-117">Version</span></span><br/> | <span data-ttu-id="21a05-118">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="21a05-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21a05-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21a05-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a05-120">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="21a05-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="21a05-121">**編輯方塊. getLine**</span><span class="sxs-lookup"><span data-stu-id="21a05-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="21a05-122">**編輯方塊. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="21a05-122">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> </dl>

 

 





