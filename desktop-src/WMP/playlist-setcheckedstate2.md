---
title: 播放清單。 setCheckedState2
description: SetCheckedState2 方法會使用播放清單元素中的指定索引來設定專案的已核取狀態。
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- 播放清單. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995593"
---
# <a name="playlistsetcheckedstate2"></a><span data-ttu-id="06d1b-104">播放清單。 setCheckedState2</span><span class="sxs-lookup"><span data-stu-id="06d1b-104">PLAYLIST.setCheckedState2</span></span>

<span data-ttu-id="06d1b-105">**SetCheckedState2** 方法會使用 **播放清單** 元素中的指定索引來設定專案的已核取狀態。</span><span class="sxs-lookup"><span data-stu-id="06d1b-105">The **setCheckedState2** method sets the checked state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a><span data-ttu-id="06d1b-106">參數</span><span class="sxs-lookup"><span data-stu-id="06d1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06d1b-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="06d1b-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="06d1b-108">**Number** (**long**) 指出要檢查或取消選取之播放清單專案的索引。</span><span class="sxs-lookup"><span data-stu-id="06d1b-108">**Number** (**long**) indicating the index of the playlist item to be checked or unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="06d1b-109"><span id="checked"></span><span id="CHECKED"></span>*檢查*</span><span class="sxs-lookup"><span data-stu-id="06d1b-109"><span id="checked"></span><span id="CHECKED"></span>*checked*</span></span>
</dt> <dd>

<span data-ttu-id="06d1b-110">**布林值** ，指出是否要檢查指定的專案 (true) 或未核取 (false) 。</span><span class="sxs-lookup"><span data-stu-id="06d1b-110">**Boolean** indicating whether the specified item is to be checked (true) or unchecked (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06d1b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="06d1b-111">Return Value</span></span>

<span data-ttu-id="06d1b-112">這個方法會傳回 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="06d1b-112">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="06d1b-113">備註</span><span class="sxs-lookup"><span data-stu-id="06d1b-113">Remarks</span></span>

<span data-ttu-id="06d1b-114">這個方法可以使用嵌套的播放清單，並取代 **setCheckedState** 方法。</span><span class="sxs-lookup"><span data-stu-id="06d1b-114">This method can work with nested playlists and replaces the **setCheckedState** method, which cannot.</span></span> <span data-ttu-id="06d1b-115">您可以在 *專案* 參數中指定1，將所有專案設定為要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="06d1b-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="06d1b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="06d1b-116">Requirements</span></span>



| <span data-ttu-id="06d1b-117">需求</span><span class="sxs-lookup"><span data-stu-id="06d1b-117">Requirement</span></span> | <span data-ttu-id="06d1b-118">值</span><span class="sxs-lookup"><span data-stu-id="06d1b-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="06d1b-119">版本</span><span class="sxs-lookup"><span data-stu-id="06d1b-119">Version</span></span><br/> | <span data-ttu-id="06d1b-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="06d1b-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06d1b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06d1b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d1b-122">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="06d1b-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="06d1b-123">**播放清單。 setCheckedState**</span><span class="sxs-lookup"><span data-stu-id="06d1b-123">**PLAYLIST.setCheckedState**</span></span>](playlist-setcheckedstate.md)
</dt> </dl>

 

 





