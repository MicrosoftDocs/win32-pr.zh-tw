---
title: 編輯方塊. getLineFromChar
description: GetLineFromChar 方法會抓取指定字元索引的行索引。
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- 編輯方塊. getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000488"
---
# <a name="editboxgetlinefromchar"></a><span data-ttu-id="3d749-104">編輯方塊. getLineFromChar</span><span class="sxs-lookup"><span data-stu-id="3d749-104">EDITBOX.getLineFromChar</span></span>

<span data-ttu-id="3d749-105">**GetLineFromChar** 方法會抓取指定字元索引的行索引。</span><span class="sxs-lookup"><span data-stu-id="3d749-105">The **getLineFromChar** method retrieves the line index for the specified character index.</span></span>

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a><span data-ttu-id="3d749-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d749-107"><span id="index"></span><span id="INDEX"></span>*指數*</span><span class="sxs-lookup"><span data-stu-id="3d749-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="3d749-108">**Number** (**Long**) ，其中包含要抓取其行索引的字元索引。</span><span class="sxs-lookup"><span data-stu-id="3d749-108">**Number** (**long**) containing the index of the character whose line index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d749-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d749-109">Return Value</span></span>

<span data-ttu-id="3d749-110">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="3d749-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d749-111">備註</span><span class="sxs-lookup"><span data-stu-id="3d749-111">Remarks</span></span>

<span data-ttu-id="3d749-112">如果指定的字元位置是1，這個方法會抓取目前行的行索引。</span><span class="sxs-lookup"><span data-stu-id="3d749-112">If the specified character position is  1, this method retrieves the line index of the current line.</span></span>

<span data-ttu-id="3d749-113">只有在控制項變成可見之後，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3d749-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d749-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d749-114">Requirements</span></span>



| <span data-ttu-id="3d749-115">需求</span><span class="sxs-lookup"><span data-stu-id="3d749-115">Requirement</span></span> | <span data-ttu-id="3d749-116">值</span><span class="sxs-lookup"><span data-stu-id="3d749-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="3d749-117">版本</span><span class="sxs-lookup"><span data-stu-id="3d749-117">Version</span></span><br/> | <span data-ttu-id="3d749-118">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="3d749-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d749-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d749-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d749-120">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="3d749-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="3d749-121">**編輯方塊. getLine**</span><span class="sxs-lookup"><span data-stu-id="3d749-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="3d749-122">**編輯方塊. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="3d749-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





