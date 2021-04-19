---
title: 播放清單。 getNextSelectedItem2
description: GetNextSelectedItem2 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- 播放清單. getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982509"
---
# <a name="playlistgetnextselecteditem2"></a><span data-ttu-id="4ee20-104">播放清單。 getNextSelectedItem2</span><span class="sxs-lookup"><span data-stu-id="4ee20-104">PLAYLIST.getNextSelectedItem2</span></span>

<span data-ttu-id="4ee20-105">**GetNextSelectedItem2** 方法會以指定的索引之後，抓取播放清單中下一個選取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="4ee20-105">The **getNextSelectedItem2** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="4ee20-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ee20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee20-107"><span id="item"></span><span id="ITEM"></span>*專案*</span><span class="sxs-lookup"><span data-stu-id="4ee20-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="4ee20-108">**Number** (**Long**) ，指出要在其後搜尋的專案索引。</span><span class="sxs-lookup"><span data-stu-id="4ee20-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee20-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ee20-109">Return Value</span></span>

<span data-ttu-id="4ee20-110">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="4ee20-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee20-111">備註</span><span class="sxs-lookup"><span data-stu-id="4ee20-111">Remarks</span></span>

<span data-ttu-id="4ee20-112">這個方法可以使用嵌套的播放清單，並取代 **getNextSelectedItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="4ee20-112">This method can work with nested playlists and replaces the **getNextSelectedItem** method, which cannot.</span></span> <span data-ttu-id="4ee20-113">在 *item* 參數中傳遞1以尋找第一個選取的專案。</span><span class="sxs-lookup"><span data-stu-id="4ee20-113">Pass  1 in the *item* parameter to find the first selected item.</span></span> <span data-ttu-id="4ee20-114">如果沒有其他選取的專案，則會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="4ee20-114">When there are no further selected items, -1 is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee20-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ee20-115">Requirements</span></span>



| <span data-ttu-id="4ee20-116">需求</span><span class="sxs-lookup"><span data-stu-id="4ee20-116">Requirement</span></span> | <span data-ttu-id="4ee20-117">值</span><span class="sxs-lookup"><span data-stu-id="4ee20-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4ee20-118">版本</span><span class="sxs-lookup"><span data-stu-id="4ee20-118">Version</span></span><br/> | <span data-ttu-id="4ee20-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4ee20-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ee20-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ee20-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee20-121">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="4ee20-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="4ee20-122">**播放清單。 getNextSelectedItem**</span><span class="sxs-lookup"><span data-stu-id="4ee20-122">**PLAYLIST.getNextSelectedItem**</span></span>](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





