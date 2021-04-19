---
title: 播放清單。 sortColumn
description: SortColumn 方法會排序指定之資料行中的資料。
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- 播放清單. sortColumn Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979620"
---
# <a name="playlistsortcolumn"></a><span data-ttu-id="95ed1-104">播放清單。 sortColumn</span><span class="sxs-lookup"><span data-stu-id="95ed1-104">PLAYLIST.sortColumn</span></span>

<span data-ttu-id="95ed1-105">**SortColumn** 方法會排序指定之資料行中的資料。</span><span class="sxs-lookup"><span data-stu-id="95ed1-105">The **sortColumn** method sorts the data in the specified column.</span></span>

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a><span data-ttu-id="95ed1-106">參數</span><span class="sxs-lookup"><span data-stu-id="95ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ed1-107"><span id="column"></span><span id="COLUMN"></span>*列*</span><span class="sxs-lookup"><span data-stu-id="95ed1-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="95ed1-108">**Number** (**Long**) ，表示要排序的資料行索引。</span><span class="sxs-lookup"><span data-stu-id="95ed1-108">**Number** (**long**) indicating the index of the column to sort.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ed1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="95ed1-109">Return Value</span></span>

<span data-ttu-id="95ed1-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="95ed1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ed1-111">備註</span><span class="sxs-lookup"><span data-stu-id="95ed1-111">Remarks</span></span>

<span data-ttu-id="95ed1-112">這個方法會將指定的資料行排序，其方式與 **播放清單** 元素中的資料行標頭按鈕相同。</span><span class="sxs-lookup"><span data-stu-id="95ed1-112">This method sorts the specified column in the same way as the column header buttons in the **PLAYLIST** element.</span></span> <span data-ttu-id="95ed1-113">如果資料行尚未排序，則會依英數位元順序排序。</span><span class="sxs-lookup"><span data-stu-id="95ed1-113">If the column has not yet been sorted, it is sorted in alphanumeric order.</span></span> <span data-ttu-id="95ed1-114">如果已排序，則會反轉其順序。</span><span class="sxs-lookup"><span data-stu-id="95ed1-114">If it has been sorted, its order is reversed.</span></span>

<span data-ttu-id="95ed1-115">若要讓此方法運作， **allowColumnSorting** 屬性必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="95ed1-115">For this method to work, the **allowColumnSorting** attribute must be set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="95ed1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="95ed1-116">Requirements</span></span>



| <span data-ttu-id="95ed1-117">需求</span><span class="sxs-lookup"><span data-stu-id="95ed1-117">Requirement</span></span> | <span data-ttu-id="95ed1-118">值</span><span class="sxs-lookup"><span data-stu-id="95ed1-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="95ed1-119">版本</span><span class="sxs-lookup"><span data-stu-id="95ed1-119">Version</span></span><br/> | <span data-ttu-id="95ed1-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="95ed1-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95ed1-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95ed1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ed1-122">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="95ed1-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="95ed1-123">**播放清單。 allowColumnSorting**</span><span class="sxs-lookup"><span data-stu-id="95ed1-123">**PLAYLIST.allowColumnSorting**</span></span>](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





