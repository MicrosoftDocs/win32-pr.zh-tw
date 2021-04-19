---
title: 播放清單。 setCheckedState
description: SetCheckedState 方法會指定檢查播放清單中的索引項目目。
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- 播放清單. setCheckedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993954"
---
# <a name="playlistsetcheckedstate"></a><span data-ttu-id="1d7c3-104">播放清單。 setCheckedState</span><span class="sxs-lookup"><span data-stu-id="1d7c3-104">PLAYLIST.setCheckedState</span></span>

<span data-ttu-id="1d7c3-105">**SetCheckedState** 方法會指定檢查播放清單中的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="1d7c3-105">The **setCheckedState** method specifies that the indexed item in the playlist is checked.</span></span>

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a><span data-ttu-id="1d7c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d7c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d7c3-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="1d7c3-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="1d7c3-108">**Number** (**long**) 表示要檢查之播放清單專案的索引。</span><span class="sxs-lookup"><span data-stu-id="1d7c3-108">**Number** (**long**) indicating the index of the playlist item to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d7c3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d7c3-109">Return Value</span></span>

<span data-ttu-id="1d7c3-110">這個方法會傳回 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="1d7c3-110">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d7c3-111">備註</span><span class="sxs-lookup"><span data-stu-id="1d7c3-111">Remarks</span></span>

<span data-ttu-id="1d7c3-112">您可以在 *專案* 參數中指定1，將所有專案設定為已核取狀態。</span><span class="sxs-lookup"><span data-stu-id="1d7c3-112">You can set all items to the checked state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="1d7c3-113">這個方法已由 **setCheckedState2** 所取代，支援嵌套播放清單。</span><span class="sxs-lookup"><span data-stu-id="1d7c3-113">This method has been replaced by **setCheckedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d7c3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d7c3-114">Requirements</span></span>



| <span data-ttu-id="1d7c3-115">需求</span><span class="sxs-lookup"><span data-stu-id="1d7c3-115">Requirement</span></span> | <span data-ttu-id="1d7c3-116">值</span><span class="sxs-lookup"><span data-stu-id="1d7c3-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1d7c3-117">版本</span><span class="sxs-lookup"><span data-stu-id="1d7c3-117">Version</span></span><br/> | <span data-ttu-id="1d7c3-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="1d7c3-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d7c3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d7c3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7c3-120">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="1d7c3-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="1d7c3-121">**播放清單。 setCheckedState2**</span><span class="sxs-lookup"><span data-stu-id="1d7c3-121">**PLAYLIST.setCheckedState2**</span></span>](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





