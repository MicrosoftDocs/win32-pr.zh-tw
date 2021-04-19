---
title: PlaylistCollection. [] 方法
description: '[] 方法會在文件庫中建立新的播放清單。'
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，PlaylistCollection 類別'
- PlaylistCollection 類別 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991156"
---
# <a name="playlistcollectionnewplaylist-method"></a><span data-ttu-id="0148e-106">PlaylistCollection. [] 方法</span><span class="sxs-lookup"><span data-stu-id="0148e-106">PlaylistCollection.newPlaylist method</span></span>

<span data-ttu-id="0148e-107">**[]** 方法會在文件庫中建立新的播放清單。</span><span class="sxs-lookup"><span data-stu-id="0148e-107">The **newPlaylist** method creates a new playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="0148e-108">語法</span><span class="sxs-lookup"><span data-stu-id="0148e-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="0148e-109">參數</span><span class="sxs-lookup"><span data-stu-id="0148e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0148e-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0148e-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0148e-111">包含要建立之播放清單名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0148e-111">**String** containing the name of the playlist to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0148e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0148e-112">Return value</span></span>

<span data-ttu-id="0148e-113">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="0148e-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0148e-114">備註</span><span class="sxs-lookup"><span data-stu-id="0148e-114">Remarks</span></span>

<span data-ttu-id="0148e-115">這個方法會在文件庫中建立空的播放清單。</span><span class="sxs-lookup"><span data-stu-id="0148e-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="0148e-116">若要以媒體專案填滿播放清單，請使用 *播放清單*。**appendItem** 或 *播放清單*。**insertItem**。</span><span class="sxs-lookup"><span data-stu-id="0148e-116">To fill the playlist with media items, use *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="0148e-117">程式庫中允許有多個具有相同名稱的播放清單。</span><span class="sxs-lookup"><span data-stu-id="0148e-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="0148e-118">若要避免使用這個方法建立重複的播放清單名稱，請使用 **getByName** 和 *PlaylistArray*。**計數** ，以判斷具有特定名稱的播放清單是否已存在。</span><span class="sxs-lookup"><span data-stu-id="0148e-118">To avoid creating a duplicate playlist name with this method, use **getByName** and *PlaylistArray*.**count** to determine whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="0148e-119">播放清單名稱中不允許前置和尾端空格，並且會自動從指定給 *name* 參數的值中移除。</span><span class="sxs-lookup"><span data-stu-id="0148e-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *name* parameter.</span></span>

<span data-ttu-id="0148e-120">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="0148e-120">To use this method, full access to the library is required.</span></span> <span data-ttu-id="0148e-121">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="0148e-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0148e-122">範例</span><span class="sxs-lookup"><span data-stu-id="0148e-122">Examples</span></span>

<span data-ttu-id="0148e-123">下列 JScript 範例會建立名為 "ThreeList" 的新空白播放清單。</span><span class="sxs-lookup"><span data-stu-id="0148e-123">The following JScript example creates a new empty playlist called "ThreeList".</span></span> <span data-ttu-id="0148e-124">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="0148e-124">The **Player** object was created with ID="Player".</span></span>


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a><span data-ttu-id="0148e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0148e-125">Requirements</span></span>



| <span data-ttu-id="0148e-126">需求</span><span class="sxs-lookup"><span data-stu-id="0148e-126">Requirement</span></span> | <span data-ttu-id="0148e-127">值</span><span class="sxs-lookup"><span data-stu-id="0148e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0148e-128">版本</span><span class="sxs-lookup"><span data-stu-id="0148e-128">Version</span></span><br/> | <span data-ttu-id="0148e-129">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0148e-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0148e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0148e-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0148e-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0148e-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0148e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0148e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0148e-133">**MediaCollection 新增**</span><span class="sxs-lookup"><span data-stu-id="0148e-133">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="0148e-134">**播放清單。 appendItem**</span><span class="sxs-lookup"><span data-stu-id="0148e-134">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="0148e-135">**播放清單。 insertItem**</span><span class="sxs-lookup"><span data-stu-id="0148e-135">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="0148e-136">**PlaylistArray 計數**</span><span class="sxs-lookup"><span data-stu-id="0148e-136">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="0148e-137">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="0148e-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="0148e-138">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="0148e-138">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="0148e-139">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0148e-139">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="0148e-140">**PlaylistCollection。移除**</span><span class="sxs-lookup"><span data-stu-id="0148e-140">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="0148e-141">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0148e-141">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0148e-142">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0148e-142">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





