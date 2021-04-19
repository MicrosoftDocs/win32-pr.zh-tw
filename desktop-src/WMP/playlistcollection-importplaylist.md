---
title: PlaylistCollection. importPlaylist 方法
description: ImportPlaylist 方法會將靜態播放清單新增至程式庫。 |PlaylistCollection. importPlaylist 方法
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- importPlaylist 方法 Windows Media Player
- importPlaylist 方法 Windows Media Player，PlaylistCollection 類別
- PlaylistCollection 類別 Windows Media Player，importPlaylist 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984112"
---
# <a name="playlistcollectionimportplaylist-method"></a><span data-ttu-id="32ebb-107">PlaylistCollection. importPlaylist 方法</span><span class="sxs-lookup"><span data-stu-id="32ebb-107">PlaylistCollection.importPlaylist method</span></span>

<span data-ttu-id="32ebb-108">**ImportPlaylist** 方法會將靜態播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="32ebb-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ebb-109">語法</span><span class="sxs-lookup"><span data-stu-id="32ebb-109">Syntax</span></span>


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="32ebb-110">參數</span><span class="sxs-lookup"><span data-stu-id="32ebb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ebb-111">*播放清單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32ebb-111">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ebb-112">要加入的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="32ebb-112">**Playlist** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ebb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="32ebb-113">Return value</span></span>

<span data-ttu-id="32ebb-114">這個方法會傳回已加入的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="32ebb-114">This method returns the **Playlist** object that was added.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ebb-115">備註</span><span class="sxs-lookup"><span data-stu-id="32ebb-115">Remarks</span></span>

<span data-ttu-id="32ebb-116">未包含任何媒體專案的播放清單，無法使用此方法新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="32ebb-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="32ebb-117">若要在程式庫中建立空的播放清單，請使用 **[]** 方法。</span><span class="sxs-lookup"><span data-stu-id="32ebb-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="32ebb-118">然後，您可以使用 *播放清單* 來填滿媒體專案所產生的播放清單。**appendItem** 或 *播放清單*。**insertItem**。</span><span class="sxs-lookup"><span data-stu-id="32ebb-118">You can then fill the resulting playlist with media items by using *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="32ebb-119">如果您將此方法傳遞給自動播放清單，則查詢會執行一次，並將結果以靜態播放清單的形式新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="32ebb-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="32ebb-120">若要將自動播放清單新增至程式庫並保留其自動行為，請使用 *MediaCollection*。**加入**。</span><span class="sxs-lookup"><span data-stu-id="32ebb-120">To add an auto playlist to the library and preserve its automatic behavior, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="32ebb-121">如需詳細資訊，請參閱 [靜態和自動播放清單](static-and-auto-playlists.md)。</span><span class="sxs-lookup"><span data-stu-id="32ebb-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="32ebb-122">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="32ebb-122">To use this method, full access to the library is required.</span></span> <span data-ttu-id="32ebb-123">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="32ebb-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32ebb-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="32ebb-124">Requirements</span></span>



| <span data-ttu-id="32ebb-125">需求</span><span class="sxs-lookup"><span data-stu-id="32ebb-125">Requirement</span></span> | <span data-ttu-id="32ebb-126">值</span><span class="sxs-lookup"><span data-stu-id="32ebb-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32ebb-127">版本</span><span class="sxs-lookup"><span data-stu-id="32ebb-127">Version</span></span><br/> | <span data-ttu-id="32ebb-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="32ebb-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="32ebb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="32ebb-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="32ebb-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32ebb-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ebb-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32ebb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ebb-132">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="32ebb-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="32ebb-133">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="32ebb-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="32ebb-134">**MediaCollection 新增**</span><span class="sxs-lookup"><span data-stu-id="32ebb-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="32ebb-135">**播放清單。 appendItem**</span><span class="sxs-lookup"><span data-stu-id="32ebb-135">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="32ebb-136">**播放清單。 insertItem**</span><span class="sxs-lookup"><span data-stu-id="32ebb-136">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="32ebb-137">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="32ebb-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

<span data-ttu-id="32ebb-138">[**PlaylistCollection. []**](playlistcollection-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="32ebb-138">[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)</span></span>
</dt> <dt>

[<span data-ttu-id="32ebb-139">**PlaylistCollection。移除**</span><span class="sxs-lookup"><span data-stu-id="32ebb-139">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="32ebb-140">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="32ebb-140">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="32ebb-141">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="32ebb-141">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





