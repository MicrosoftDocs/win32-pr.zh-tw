---
title: 播放清單。 getNextSelectedItem
description: GetNextSelectedItem 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- 播放清單. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985743"
---
# <a name="playlistgetnextselecteditem"></a><span data-ttu-id="e8628-104">播放清單。 getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="e8628-104">PLAYLIST.getNextSelectedItem</span></span>

<span data-ttu-id="e8628-105">**GetNextSelectedItem** 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="e8628-105">The **getNextSelectedItem** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="e8628-106">參數</span><span class="sxs-lookup"><span data-stu-id="e8628-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8628-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="e8628-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="e8628-108">**Number** (**Long**) ，指出要在其後搜尋的專案索引。</span><span class="sxs-lookup"><span data-stu-id="e8628-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8628-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8628-109">Return Value</span></span>

<span data-ttu-id="e8628-110">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="e8628-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8628-111">備註</span><span class="sxs-lookup"><span data-stu-id="e8628-111">Remarks</span></span>

<span data-ttu-id="e8628-112">如果沒有其他選取的專案，這個方法會傳回1。</span><span class="sxs-lookup"><span data-stu-id="e8628-112">When there are no further selected items, this method returns  1.</span></span>

<span data-ttu-id="e8628-113">這個方法已由 **getNextSelectedItem2** 所取代，支援嵌套播放清單。</span><span class="sxs-lookup"><span data-stu-id="e8628-113">This method has been replaced by **getNextSelectedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8628-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8628-114">Requirements</span></span>



| <span data-ttu-id="e8628-115">需求</span><span class="sxs-lookup"><span data-stu-id="e8628-115">Requirement</span></span> | <span data-ttu-id="e8628-116">值</span><span class="sxs-lookup"><span data-stu-id="e8628-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e8628-117">版本</span><span class="sxs-lookup"><span data-stu-id="e8628-117">Version</span></span><br/> | <span data-ttu-id="e8628-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="e8628-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8628-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8628-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8628-120">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="e8628-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="e8628-121">**播放清單。 getNextSelectedItem2**</span><span class="sxs-lookup"><span data-stu-id="e8628-121">**PLAYLIST.getNextSelectedItem2**</span></span>](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





