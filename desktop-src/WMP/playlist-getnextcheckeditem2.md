---
title: 播放清單。 getNextCheckedItem2
description: GetNextCheckedItem2 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- 播放清單. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985968"
---
# <a name="playlistgetnextcheckeditem2"></a><span data-ttu-id="5331c-104">播放清單。 getNextCheckedItem2</span><span class="sxs-lookup"><span data-stu-id="5331c-104">PLAYLIST.getNextCheckedItem2</span></span>

<span data-ttu-id="5331c-105">**GetNextCheckedItem2** 方法會以指定的索引之後，抓取播放清單中下一個核取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="5331c-105">The **getNextCheckedItem2** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="5331c-106">參數</span><span class="sxs-lookup"><span data-stu-id="5331c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5331c-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="5331c-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="5331c-108">**Number** (**Long**) ，指出要在其後搜尋的專案索引。</span><span class="sxs-lookup"><span data-stu-id="5331c-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5331c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5331c-109">Return Value</span></span>

<span data-ttu-id="5331c-110">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="5331c-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5331c-111">備註</span><span class="sxs-lookup"><span data-stu-id="5331c-111">Remarks</span></span>

<span data-ttu-id="5331c-112">這個方法可以使用嵌套的播放清單，並取代 **getNextCheckedItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="5331c-112">This method can work with nested playlists and replaces the **getNextCheckedItem** method, which cannot.</span></span> <span data-ttu-id="5331c-113">在 *item* 參數中傳遞1以找出第一個選取的專案。</span><span class="sxs-lookup"><span data-stu-id="5331c-113">Pass  1 in the *item* parameter to find the first checked item.</span></span> <span data-ttu-id="5331c-114">如果沒有進一步的核取專案，這個方法會傳回1。</span><span class="sxs-lookup"><span data-stu-id="5331c-114">When there are no further checked items, this method returns  1.</span></span>

## <a name="requirements"></a><span data-ttu-id="5331c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5331c-115">Requirements</span></span>



| <span data-ttu-id="5331c-116">需求</span><span class="sxs-lookup"><span data-stu-id="5331c-116">Requirement</span></span> | <span data-ttu-id="5331c-117">值</span><span class="sxs-lookup"><span data-stu-id="5331c-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="5331c-118">版本</span><span class="sxs-lookup"><span data-stu-id="5331c-118">Version</span></span><br/> | <span data-ttu-id="5331c-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="5331c-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5331c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5331c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5331c-121">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="5331c-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="5331c-122">**播放清單。 getNextCheckedItem**</span><span class="sxs-lookup"><span data-stu-id="5331c-122">**PLAYLIST.getNextCheckedItem**</span></span>](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





