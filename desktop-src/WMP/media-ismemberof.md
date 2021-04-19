---
title: IsMemberOf 方法
description: IsMemberOf 方法會傳回值，指出媒體專案是否為指定播放清單的成員。
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- isMemberOf 方法 Windows Media Player
- isMemberOf 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，isMemberOf 方法
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990037"
---
# <a name="mediaismemberof-method"></a><span data-ttu-id="eb947-106">IsMemberOf 方法</span><span class="sxs-lookup"><span data-stu-id="eb947-106">Media.isMemberOf method</span></span>

<span data-ttu-id="eb947-107">**IsMemberOf** 方法會傳回值，指出媒體專案是否為指定播放清單的成員。</span><span class="sxs-lookup"><span data-stu-id="eb947-107">The **isMemberOf** method returns a value indicating whether the media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb947-108">語法</span><span class="sxs-lookup"><span data-stu-id="eb947-108">Syntax</span></span>


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="eb947-109">參數</span><span class="sxs-lookup"><span data-stu-id="eb947-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb947-110">*播放清單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb947-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb947-111">可能包含媒體專案的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="eb947-111">**Playlist** object that might contain the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb947-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb947-112">Return value</span></span>

<span data-ttu-id="eb947-113">這個方法會傳回 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="eb947-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb947-114">備註</span><span class="sxs-lookup"><span data-stu-id="eb947-114">Remarks</span></span>

<span data-ttu-id="eb947-115">這個方法無法檢查透過 **MediaCollection** 物件取出的播放清單。</span><span class="sxs-lookup"><span data-stu-id="eb947-115">This method is cannot check playlists retrieved through the **MediaCollection** object.</span></span> <span data-ttu-id="eb947-116">若要測試媒體專案是否為特定命名播放清單的成員，請使用 *播放* 程式取出播放清單。*playlistCollection*。**getByName** (*名稱*) 。**專案** (0) 。</span><span class="sxs-lookup"><span data-stu-id="eb947-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist with *player*.*playlistCollection*.**getByName**(*name*).**item**(0).</span></span> <span data-ttu-id="eb947-117">此方法也可以搭配 CD 播放清單和中繼檔播放清單使用。</span><span class="sxs-lookup"><span data-stu-id="eb947-117">This method can also be used with CD playlists and metafile playlists.</span></span>

<span data-ttu-id="eb947-118">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="eb947-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="eb947-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="eb947-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eb947-120">範例</span><span class="sxs-lookup"><span data-stu-id="eb947-120">Examples</span></span>

<span data-ttu-id="eb947-121">下列 JScript 範例會使用 *媒體*。**isMemberOf** ，測試目前的媒體專案是否為名為範例播放清單的播放清單成員。</span><span class="sxs-lookup"><span data-stu-id="eb947-121">The following JScript example uses *Media*.**isMemberOf** to test whether the current media item is a member of the playlist named Sample Playlist.</span></span> <span data-ttu-id="eb947-122">如果不是，則會將目前的媒體專案附加至範例播放清單。</span><span class="sxs-lookup"><span data-stu-id="eb947-122">If it is not, the current media item is appended to the sample playlist.</span></span> <span data-ttu-id="eb947-123">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="eb947-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a><span data-ttu-id="eb947-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb947-124">Requirements</span></span>



| <span data-ttu-id="eb947-125">需求</span><span class="sxs-lookup"><span data-stu-id="eb947-125">Requirement</span></span> | <span data-ttu-id="eb947-126">值</span><span class="sxs-lookup"><span data-stu-id="eb947-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb947-127">版本</span><span class="sxs-lookup"><span data-stu-id="eb947-127">Version</span></span><br/> | <span data-ttu-id="eb947-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="eb947-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="eb947-129">DLL</span><span class="sxs-lookup"><span data-stu-id="eb947-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="eb947-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb947-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb947-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb947-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb947-132">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="eb947-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="eb947-133">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="eb947-133">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="eb947-134">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="eb947-134">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="eb947-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="eb947-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="eb947-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="eb947-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





