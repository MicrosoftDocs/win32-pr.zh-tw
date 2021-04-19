---
title: LISTBOX. getNextSelectedItem
description: GetNextSelectedItem 方法會從具有指定索引之專案之後的專案開始，從清單方塊控制項中取出下一個選取的專案。
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982598"
---
# <a name="listboxgetnextselecteditem"></a><span data-ttu-id="ab6fd-104">LISTBOX. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="ab6fd-104">LISTBOX.getNextSelectedItem</span></span>

<span data-ttu-id="ab6fd-105">**GetNextSelectedItem** 方法會從具有指定索引之專案之後的專案開始，從清單方塊控制項中取出下一個選取的專案。</span><span class="sxs-lookup"><span data-stu-id="ab6fd-105">The **getNextSelectedItem** method retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a><span data-ttu-id="ab6fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab6fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6fd-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="ab6fd-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="ab6fd-108">**Number** (**Long**) ，其中包含要抓取之專案之前的專案索引。</span><span class="sxs-lookup"><span data-stu-id="ab6fd-108">**Number** (**long**) containing the index of the item that precedes the item being retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6fd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab6fd-109">Return Value</span></span>

<span data-ttu-id="ab6fd-110">這個方法會傳回 **數位** (**Long**) ，其中包含下一個選取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="ab6fd-110">This method returns a **Number** (**long**) containing the index of the next selected item.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab6fd-111">備註</span><span class="sxs-lookup"><span data-stu-id="ab6fd-111">Remarks</span></span>

<span data-ttu-id="ab6fd-112">若要從頭開始搜尋，請使用1作為開始索引。</span><span class="sxs-lookup"><span data-stu-id="ab6fd-112">To start search from the beginning, use  1 for the start index.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6fd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab6fd-113">Requirements</span></span>



| <span data-ttu-id="ab6fd-114">需求</span><span class="sxs-lookup"><span data-stu-id="ab6fd-114">Requirement</span></span> | <span data-ttu-id="ab6fd-115">值</span><span class="sxs-lookup"><span data-stu-id="ab6fd-115">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="ab6fd-116">版本</span><span class="sxs-lookup"><span data-stu-id="ab6fd-116">Version</span></span><br/> | <span data-ttu-id="ab6fd-117">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="ab6fd-117">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab6fd-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab6fd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6fd-119">**LISTBOX 元素**</span><span class="sxs-lookup"><span data-stu-id="ab6fd-119">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





