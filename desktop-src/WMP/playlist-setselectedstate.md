---
title: 播放清單。 setSelectedState
description: SetSelectedState 方法會指定選取播放清單中的索引項目目。
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- 播放清單. setSelectedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982702"
---
# <a name="playlistsetselectedstate"></a><span data-ttu-id="b8b2a-104">播放清單。 setSelectedState</span><span class="sxs-lookup"><span data-stu-id="b8b2a-104">PLAYLIST.setSelectedState</span></span>

<span data-ttu-id="b8b2a-105">**SetSelectedState** 方法會指定選取播放清單中的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="b8b2a-105">The **setSelectedState** method specifies that the indexed item in the playlist is selected.</span></span>

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a><span data-ttu-id="b8b2a-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8b2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b2a-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="b8b2a-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="b8b2a-108">**數位** (**long**) 指出播放清單中專案的索引。</span><span class="sxs-lookup"><span data-stu-id="b8b2a-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b2a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8b2a-109">Return Value</span></span>

<span data-ttu-id="b8b2a-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b8b2a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b2a-111">備註</span><span class="sxs-lookup"><span data-stu-id="b8b2a-111">Remarks</span></span>

<span data-ttu-id="b8b2a-112">您可以在 *專案* 參數中指定1，將所有專案設定為選取的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8b2a-112">You can set all items to the selected state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="b8b2a-113">這個方法已由 **setSelectedState2** 所取代，支援嵌套播放清單。</span><span class="sxs-lookup"><span data-stu-id="b8b2a-113">This method has been replaced by **setSelectedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b2a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8b2a-114">Requirements</span></span>



| <span data-ttu-id="b8b2a-115">需求</span><span class="sxs-lookup"><span data-stu-id="b8b2a-115">Requirement</span></span> | <span data-ttu-id="b8b2a-116">值</span><span class="sxs-lookup"><span data-stu-id="b8b2a-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b8b2a-117">版本</span><span class="sxs-lookup"><span data-stu-id="b8b2a-117">Version</span></span><br/> | <span data-ttu-id="b8b2a-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b8b2a-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8b2a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8b2a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b2a-120">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="b8b2a-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="b8b2a-121">**播放清單。 setSelectedState2**</span><span class="sxs-lookup"><span data-stu-id="b8b2a-121">**PLAYLIST.setSelectedState2**</span></span>](playlist-setselectedstate2.md)
</dt> </dl>

 

 





