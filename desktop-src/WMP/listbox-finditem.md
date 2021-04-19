---
title: LISTBOX. findItem
description: FindItem 方法會從指定的專案索引後面的專案開始，搜尋指定的字串。
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX. findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977701"
---
# <a name="listboxfinditem"></a><span data-ttu-id="46d18-104">LISTBOX. findItem</span><span class="sxs-lookup"><span data-stu-id="46d18-104">LISTBOX.findItem</span></span>

<span data-ttu-id="46d18-105">**FindItem** 方法會從指定的專案索引後面的專案開始，搜尋指定的字串。</span><span class="sxs-lookup"><span data-stu-id="46d18-105">The **findItem** method searches for a given string starting with the item following the specified item index.</span></span>

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a><span data-ttu-id="46d18-106">參數</span><span class="sxs-lookup"><span data-stu-id="46d18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d18-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="46d18-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="46d18-108">**Number** (**Long**) ，其中包含要開始搜尋之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="46d18-108">**Number** (**long**) containing the index of the item at which to start the search.</span></span>

</dd> <dt>

<span data-ttu-id="46d18-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span><span class="sxs-lookup"><span data-stu-id="46d18-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span></span>
</dt> <dd>

<span data-ttu-id="46d18-110">包含要搜尋之文字的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="46d18-110">**String** containing the text to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d18-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="46d18-111">Return Value</span></span>

<span data-ttu-id="46d18-112">這個方法會傳回 **數位** (**Long**) ，其中包含包含字串之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="46d18-112">This method returns a **Number** (**long**) containing the index of the item that contains the string.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d18-113">備註</span><span class="sxs-lookup"><span data-stu-id="46d18-113">Remarks</span></span>

<span data-ttu-id="46d18-114">若要在清單方塊控制項的第一行開始搜尋，請使用1做為 *startIndex*。</span><span class="sxs-lookup"><span data-stu-id="46d18-114">To start the search at the first line of the list box control, use  1 as the *startIndex*.</span></span> <span data-ttu-id="46d18-115">若要在找到第一行之後繼續搜尋文字，請使用傳回的行索引作為 *startIndex*，然後搜尋將從下一行開始。</span><span class="sxs-lookup"><span data-stu-id="46d18-115">To continue to search for text after the first line is found, use the returned line index as the *startIndex*, and the search will start at the next line.</span></span> <span data-ttu-id="46d18-116">這個方法會搜尋子字串，且不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="46d18-116">This method will search for substrings and is not case-sensitive.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d18-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d18-117">Requirements</span></span>



| <span data-ttu-id="46d18-118">需求</span><span class="sxs-lookup"><span data-stu-id="46d18-118">Requirement</span></span> | <span data-ttu-id="46d18-119">值</span><span class="sxs-lookup"><span data-stu-id="46d18-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="46d18-120">版本</span><span class="sxs-lookup"><span data-stu-id="46d18-120">Version</span></span><br/> | <span data-ttu-id="46d18-121">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="46d18-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46d18-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46d18-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d18-123">**LISTBOX 元素**</span><span class="sxs-lookup"><span data-stu-id="46d18-123">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





