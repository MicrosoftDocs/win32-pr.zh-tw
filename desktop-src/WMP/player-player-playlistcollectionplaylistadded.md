---
title: PlaylistCollectionPlaylistAdded 事件
description: 當播放清單新增至播放清單集合時，就會發生 PlaylistCollectionPlaylistAdded 事件。 |PlaylistCollectionPlaylistAdded 事件
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- PlaylistCollectionPlaylistAdded 事件 Windows Media Player
- PlaylistCollectionPlaylistAdded 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PlaylistCollectionPlaylistAdded 事件
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995774"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a><span data-ttu-id="206e5-107">PlaylistCollectionPlaylistAdded 事件</span><span class="sxs-lookup"><span data-stu-id="206e5-107">Player.PlaylistCollectionPlaylistAdded event</span></span>

<span data-ttu-id="206e5-108">當播放清單新增至播放清單集合時，就會發生 **PlaylistCollectionPlaylistAdded** 事件。</span><span class="sxs-lookup"><span data-stu-id="206e5-108">The **PlaylistCollectionPlaylistAdded** event occurs when a playlist is added to the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="206e5-109">語法</span><span class="sxs-lookup"><span data-stu-id="206e5-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="206e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="206e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="206e5-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="206e5-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="206e5-112">**字串** ，指定已新增之播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="206e5-112">**String** specifying the name of the playlist that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="206e5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="206e5-113">Return value</span></span>

<span data-ttu-id="206e5-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="206e5-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="206e5-115">備註</span><span class="sxs-lookup"><span data-stu-id="206e5-115">Remarks</span></span>

<span data-ttu-id="206e5-116">已新增的播放清單名稱可以用來使用 *PlaylistCollection* 來取出對應的 **播放清單** 物件。**getByName** 方法。</span><span class="sxs-lookup"><span data-stu-id="206e5-116">The name of the playlist that was added can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="206e5-117">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="206e5-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="206e5-118">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="206e5-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="206e5-119">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="206e5-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="206e5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="206e5-120">Requirements</span></span>



| <span data-ttu-id="206e5-121">需求</span><span class="sxs-lookup"><span data-stu-id="206e5-121">Requirement</span></span> | <span data-ttu-id="206e5-122">值</span><span class="sxs-lookup"><span data-stu-id="206e5-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="206e5-123">版本</span><span class="sxs-lookup"><span data-stu-id="206e5-123">Version</span></span><br/> | <span data-ttu-id="206e5-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="206e5-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="206e5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="206e5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="206e5-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="206e5-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206e5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="206e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206e5-128">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="206e5-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="206e5-129">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="206e5-129">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





