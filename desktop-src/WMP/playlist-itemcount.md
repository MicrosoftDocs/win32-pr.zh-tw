---
title: 播放清單。 itemCount
description: ItemCount 屬性會抓取播放清單元素目前所顯示的專案數。
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- 播放清單. itemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999503"
---
# <a name="playlistitemcount"></a><span data-ttu-id="7679a-104">播放清單。 itemCount</span><span class="sxs-lookup"><span data-stu-id="7679a-104">PLAYLIST.itemCount</span></span>

<span data-ttu-id="7679a-105">**ItemCount** 屬性會抓取 **播放清單** 元素目前所顯示的專案數。</span><span class="sxs-lookup"><span data-stu-id="7679a-105">The **itemCount** attribute retrieves the number of items currently displayed in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a><span data-ttu-id="7679a-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="7679a-106">Possible Values</span></span>

<span data-ttu-id="7679a-107">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="7679a-107">This attribute is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7679a-108">備註</span><span class="sxs-lookup"><span data-stu-id="7679a-108">Remarks</span></span>

<span data-ttu-id="7679a-109">**ItemCount** 屬性將會計算展開專案的總數。</span><span class="sxs-lookup"><span data-stu-id="7679a-109">The **itemCount** property will count the total number of expanded items.</span></span> <span data-ttu-id="7679a-110">例如，如果有兩個包含三個媒體專案的播放清單，則如果沒有展開播放清單，則 **itemCount** 會傳回2。</span><span class="sxs-lookup"><span data-stu-id="7679a-110">For example, if there are two playlists that contain three media items each, **itemCount** will return 2 if the playlists are not expanded.</span></span> <span data-ttu-id="7679a-111">如果只展開第一個播放清單，則 **itemCount** 會傳回4。</span><span class="sxs-lookup"><span data-stu-id="7679a-111">If only the first playlist is expanded, **itemCount** will return 4.</span></span> <span data-ttu-id="7679a-112">如果這兩個播放清單都已展開， **itemCount** 會傳回6。</span><span class="sxs-lookup"><span data-stu-id="7679a-112">If both playlists are expanded, **itemCount** will return 6.</span></span>

## <a name="requirements"></a><span data-ttu-id="7679a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7679a-113">Requirements</span></span>



| <span data-ttu-id="7679a-114">需求</span><span class="sxs-lookup"><span data-stu-id="7679a-114">Requirement</span></span> | <span data-ttu-id="7679a-115">值</span><span class="sxs-lookup"><span data-stu-id="7679a-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7679a-116">版本</span><span class="sxs-lookup"><span data-stu-id="7679a-116">Version</span></span><br/> | <span data-ttu-id="7679a-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="7679a-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7679a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7679a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7679a-119">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="7679a-119">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





