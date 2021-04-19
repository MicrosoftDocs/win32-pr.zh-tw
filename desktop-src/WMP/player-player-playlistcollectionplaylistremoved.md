---
title: PlaylistCollectionPlaylistRemoved 事件
description: 從播放清單集合中移除播放清單時，就會發生 PlaylistCollectionPlaylistRemoved 事件。 |PlaylistCollectionPlaylistRemoved 事件
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- PlaylistCollectionPlaylistRemoved 事件 Windows Media Player
- PlaylistCollectionPlaylistRemoved 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PlaylistCollectionPlaylistRemoved 事件
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987952"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a><span data-ttu-id="ea9c1-107">PlaylistCollectionPlaylistRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="ea9c1-107">Player.PlaylistCollectionPlaylistRemoved event</span></span>

<span data-ttu-id="ea9c1-108">從播放清單集合中移除播放清單時，就會發生 **PlaylistCollectionPlaylistRemoved** 事件。</span><span class="sxs-lookup"><span data-stu-id="ea9c1-108">The **PlaylistCollectionPlaylistRemoved** event occurs when a playlist is removed from the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea9c1-109">語法</span><span class="sxs-lookup"><span data-stu-id="ea9c1-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="ea9c1-110">參數</span><span class="sxs-lookup"><span data-stu-id="ea9c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9c1-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="ea9c1-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9c1-112">**字串** ，指定已移除之播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea9c1-112">**String** specifying the name of the playlist that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9c1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea9c1-113">Return value</span></span>

<span data-ttu-id="ea9c1-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ea9c1-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9c1-115">備註</span><span class="sxs-lookup"><span data-stu-id="ea9c1-115">Remarks</span></span>

<span data-ttu-id="ea9c1-116">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="ea9c1-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="ea9c1-117">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="ea9c1-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="ea9c1-118">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="ea9c1-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9c1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea9c1-119">Requirements</span></span>



| <span data-ttu-id="ea9c1-120">需求</span><span class="sxs-lookup"><span data-stu-id="ea9c1-120">Requirement</span></span> | <span data-ttu-id="ea9c1-121">值</span><span class="sxs-lookup"><span data-stu-id="ea9c1-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9c1-122">版本</span><span class="sxs-lookup"><span data-stu-id="ea9c1-122">Version</span></span><br/> | <span data-ttu-id="ea9c1-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ea9c1-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ea9c1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ea9c1-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea9c1-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea9c1-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9c1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea9c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9c1-127">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="ea9c1-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="ea9c1-128">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="ea9c1-128">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





