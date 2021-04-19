---
title: 播放清單。 getNextCheckedItem
description: GetNextCheckedItem 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- 播放清單. getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983961"
---
# <a name="playlistgetnextcheckeditem"></a><span data-ttu-id="12132-104">播放清單。 getNextCheckedItem</span><span class="sxs-lookup"><span data-stu-id="12132-104">PLAYLIST.getNextCheckedItem</span></span>

<span data-ttu-id="12132-105">**GetNextCheckedItem** 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="12132-105">The **getNextCheckedItem** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="12132-106">參數</span><span class="sxs-lookup"><span data-stu-id="12132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12132-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="12132-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="12132-108">**Number** (**Long**) ，指出要在其後搜尋的專案索引。</span><span class="sxs-lookup"><span data-stu-id="12132-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12132-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="12132-109">Return Value</span></span>

<span data-ttu-id="12132-110">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="12132-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="12132-111">備註</span><span class="sxs-lookup"><span data-stu-id="12132-111">Remarks</span></span>

<span data-ttu-id="12132-112">如果沒有進一步的核取專案，這個方法會傳回1。</span><span class="sxs-lookup"><span data-stu-id="12132-112">When there are no further checked items, this method returns  1.</span></span>

<span data-ttu-id="12132-113">這個方法已由 **getNextCheckedItem2** 所取代，支援嵌套播放清單。</span><span class="sxs-lookup"><span data-stu-id="12132-113">This method has been replaced by **getNextCheckedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="12132-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="12132-114">Requirements</span></span>



| <span data-ttu-id="12132-115">需求</span><span class="sxs-lookup"><span data-stu-id="12132-115">Requirement</span></span> | <span data-ttu-id="12132-116">值</span><span class="sxs-lookup"><span data-stu-id="12132-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="12132-117">版本</span><span class="sxs-lookup"><span data-stu-id="12132-117">Version</span></span><br/> | <span data-ttu-id="12132-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="12132-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12132-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12132-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12132-120">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="12132-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="12132-121">**播放清單。 getNextCheckedItem2**</span><span class="sxs-lookup"><span data-stu-id="12132-121">**PLAYLIST.getNextCheckedItem2**</span></span>](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





