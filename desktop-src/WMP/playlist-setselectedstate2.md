---
title: 播放清單。 setSelectedState2
description: SetSelectedState2 方法會使用播放清單元素中的指定索引來設定專案的選取狀態。
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- 播放清單. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991049"
---
# <a name="playlistsetselectedstate2"></a><span data-ttu-id="e53b1-104">播放清單。 setSelectedState2</span><span class="sxs-lookup"><span data-stu-id="e53b1-104">PLAYLIST.setSelectedState2</span></span>

<span data-ttu-id="e53b1-105">**SetSelectedState2** 方法會使用 **播放清單** 元素中的指定索引來設定專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="e53b1-105">The **setSelectedState2** method sets the selected state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a><span data-ttu-id="e53b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="e53b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e53b1-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="e53b1-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="e53b1-108">**數位** (**long**) 指出播放清單中專案的索引。</span><span class="sxs-lookup"><span data-stu-id="e53b1-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="e53b1-109"><span id="selected"></span><span id="SELECTED"></span>*選擇*</span><span class="sxs-lookup"><span data-stu-id="e53b1-109"><span id="selected"></span><span id="SELECTED"></span>*selected*</span></span>
</dt> <dd>

<span data-ttu-id="e53b1-110">**布林值** ，指出是否要選取指定的專案 (true) 或未選取 (false) 。</span><span class="sxs-lookup"><span data-stu-id="e53b1-110">**Boolean** indicating whether the specified item is to be selected (true) or unselected (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e53b1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e53b1-111">Return Value</span></span>

<span data-ttu-id="e53b1-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e53b1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e53b1-113">備註</span><span class="sxs-lookup"><span data-stu-id="e53b1-113">Remarks</span></span>

<span data-ttu-id="e53b1-114">這個方法可以使用嵌套的播放清單，並取代無法使用的 **setSelectedState** 方法。</span><span class="sxs-lookup"><span data-stu-id="e53b1-114">This method can work with nested playlists and replaces the **setSelectedState** method which cannot.</span></span> <span data-ttu-id="e53b1-115">您可以在 *專案* 參數中指定1，將所有專案設定為要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="e53b1-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53b1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e53b1-116">Requirements</span></span>



| <span data-ttu-id="e53b1-117">需求</span><span class="sxs-lookup"><span data-stu-id="e53b1-117">Requirement</span></span> | <span data-ttu-id="e53b1-118">值</span><span class="sxs-lookup"><span data-stu-id="e53b1-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e53b1-119">版本</span><span class="sxs-lookup"><span data-stu-id="e53b1-119">Version</span></span><br/> | <span data-ttu-id="e53b1-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e53b1-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e53b1-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e53b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53b1-122">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="e53b1-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="e53b1-123">**播放清單。 setSelectedState**</span><span class="sxs-lookup"><span data-stu-id="e53b1-123">**PLAYLIST.setSelectedState**</span></span>](playlist-setselectedstate.md)
</dt> </dl>

 

 





