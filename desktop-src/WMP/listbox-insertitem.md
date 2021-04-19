---
title: LISTBOX. insertItem
description: InsertItem 方法會將指定的文字插入清單方塊控制項中的指定索引處。
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- LISTBOX. insertItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3600b40ca164c71bd62c0a9a368516d6ad0e1edd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981626"
---
# <a name="listboxinsertitem"></a><span data-ttu-id="e62a8-104">LISTBOX. insertItem</span><span class="sxs-lookup"><span data-stu-id="e62a8-104">LISTBOX.insertItem</span></span>

<span data-ttu-id="e62a8-105">**InsertItem** 方法會將指定的文字插入清單方塊控制項中的指定索引處。</span><span class="sxs-lookup"><span data-stu-id="e62a8-105">The **insertItem** method inserts the specified text at the specified index in the list box control.</span></span>

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a><span data-ttu-id="e62a8-106">參數</span><span class="sxs-lookup"><span data-stu-id="e62a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e62a8-107"><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="e62a8-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="e62a8-108">包含要取出的行之索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="e62a8-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e62a8-109"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="e62a8-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="e62a8-110">包含要插入之文字的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="e62a8-110">**String** containing the text to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e62a8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e62a8-111">Return Value</span></span>

<span data-ttu-id="e62a8-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e62a8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e62a8-113">備註</span><span class="sxs-lookup"><span data-stu-id="e62a8-113">Remarks</span></span>

<span data-ttu-id="e62a8-114">插入線條時，插入行下方行的行索引會增加1。</span><span class="sxs-lookup"><span data-stu-id="e62a8-114">When a line is inserted, the line indexes for the lines below the inserted line increase by one.</span></span>

## <a name="requirements"></a><span data-ttu-id="e62a8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e62a8-115">Requirements</span></span>



| <span data-ttu-id="e62a8-116">需求</span><span class="sxs-lookup"><span data-stu-id="e62a8-116">Requirement</span></span> | <span data-ttu-id="e62a8-117">值</span><span class="sxs-lookup"><span data-stu-id="e62a8-117">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="e62a8-118">版本</span><span class="sxs-lookup"><span data-stu-id="e62a8-118">Version</span></span><br/> | <span data-ttu-id="e62a8-119">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e62a8-119">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e62a8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e62a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e62a8-121">**LISTBOX 元素**</span><span class="sxs-lookup"><span data-stu-id="e62a8-121">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





