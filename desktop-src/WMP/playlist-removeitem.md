---
title: RemoveItem 方法
description: RemoveItem 方法會從播放清單中移除指定的專案。
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- removeItem 方法 Windows Media Player
- removeItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，removeItem 方法
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998797"
---
# <a name="playlistremoveitem-method"></a><span data-ttu-id="fdf1c-106">RemoveItem 方法</span><span class="sxs-lookup"><span data-stu-id="fdf1c-106">Playlist.removeItem method</span></span>

<span data-ttu-id="fdf1c-107">**RemoveItem** 方法會從播放清單中移除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-107">The **removeItem** method removes the specified item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf1c-108">語法</span><span class="sxs-lookup"><span data-stu-id="fdf1c-108">Syntax</span></span>


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="fdf1c-109">參數</span><span class="sxs-lookup"><span data-stu-id="fdf1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf1c-110">*專案* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdf1c-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf1c-111">要移除的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-111">**Media** object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf1c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdf1c-112">Return value</span></span>

<span data-ttu-id="fdf1c-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdf1c-114">備註</span><span class="sxs-lookup"><span data-stu-id="fdf1c-114">Remarks</span></span>

<span data-ttu-id="fdf1c-115">如果移除的專案是目前播放的曲目 (*播放機*。**currentMedia**) ，播放會停止，且播放清單中的下一個專案會變成目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-115">If the item removed is the currently playing track (*Player*.**currentMedia**), playback stops and the next item in the playlist becomes the current one.</span></span> <span data-ttu-id="fdf1c-116">如果沒有下一個專案，則會使用前一個專案，如果沒有其他專案，則會使用 [ *播放* 程式]。**currentMedia** 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-116">If there is no next item, the previous item is used, or if there are no other items, then *Player*.**currentMedia** is set to **NULL**.</span></span>

<span data-ttu-id="fdf1c-117">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-117">To use this method, full access to the library is required.</span></span> <span data-ttu-id="fdf1c-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf1c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdf1c-119">Requirements</span></span>



| <span data-ttu-id="fdf1c-120">需求</span><span class="sxs-lookup"><span data-stu-id="fdf1c-120">Requirement</span></span> | <span data-ttu-id="fdf1c-121">值</span><span class="sxs-lookup"><span data-stu-id="fdf1c-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf1c-122">版本</span><span class="sxs-lookup"><span data-stu-id="fdf1c-122">Version</span></span><br/> | <span data-ttu-id="fdf1c-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fdf1c-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fdf1c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fdf1c-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="fdf1c-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdf1c-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdf1c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdf1c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf1c-127">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="fdf1c-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="fdf1c-128">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="fdf1c-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="fdf1c-129">**播放清單。 insertItem**</span><span class="sxs-lookup"><span data-stu-id="fdf1c-129">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="fdf1c-130">**播放清單。專案**</span><span class="sxs-lookup"><span data-stu-id="fdf1c-130">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="fdf1c-131">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fdf1c-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fdf1c-132">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fdf1c-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





