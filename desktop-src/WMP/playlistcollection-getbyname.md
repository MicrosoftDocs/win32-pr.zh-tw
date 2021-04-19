---
title: PlaylistCollection. getByName 方法
description: GetByName 方法會抓取 PlaylistArray 物件，其中包含具有指定名稱的播放清單（如果有的話）。
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- getByName 方法 Windows Media Player
- getByName 方法 Windows Media Player，PlaylistCollection 類別
- PlaylistCollection 類別 Windows Media Player，getByName 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999374"
---
# <a name="playlistcollectiongetbyname-method"></a><span data-ttu-id="0c024-106">PlaylistCollection. getByName 方法</span><span class="sxs-lookup"><span data-stu-id="0c024-106">PlaylistCollection.getByName method</span></span>

<span data-ttu-id="0c024-107">**GetByName** 方法會抓取 **PlaylistArray** 物件，其中包含具有指定名稱的播放清單（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0c024-107">The **getByName** method retrieves a **PlaylistArray** object containing playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c024-108">語法</span><span class="sxs-lookup"><span data-stu-id="0c024-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="0c024-109">參數</span><span class="sxs-lookup"><span data-stu-id="0c024-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c024-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c024-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c024-111">包含要抓取之播放清單名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="0c024-111">**String** containing the name of the playlists to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c024-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c024-112">Return value</span></span>

<span data-ttu-id="0c024-113">這個方法會傳回 **PlaylistArray** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c024-113">This method returns a **PlaylistArray** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c024-114">備註</span><span class="sxs-lookup"><span data-stu-id="0c024-114">Remarks</span></span>

<span data-ttu-id="0c024-115">使用 *PlaylistArray*。判斷播放清單是否存在的 **計數** 。</span><span class="sxs-lookup"><span data-stu-id="0c024-115">Use *PlaylistArray*.**count** to determine whether a playlist exists.</span></span> <span data-ttu-id="0c024-116">如果 **count** 為零，則不存在播放清單。</span><span class="sxs-lookup"><span data-stu-id="0c024-116">If **count** is zero, a playlist does not exist.</span></span>

<span data-ttu-id="0c024-117">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="0c024-117">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0c024-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="0c024-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0c024-119">範例</span><span class="sxs-lookup"><span data-stu-id="0c024-119">Examples</span></span>

<span data-ttu-id="0c024-120">下列 JScript 範例會使用 *playlistCollection*。**getByName** ，檢查名為 "ThreeList" 的播放清單的 **playlistCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c024-120">The following JScript example uses *playlistCollection*.**getByName** to check the **playlistCollection** object for a playlist named "ThreeList".</span></span> <span data-ttu-id="0c024-121">如果 "Threelist" 播放清單存在， **getByName** 會將 "Threelist" 設定為目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="0c024-121">If the "Threelist" playlist exists, **getByName** sets "ThreeList" as the current playlist.</span></span> <span data-ttu-id="0c024-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c024-122">The **Player** object was created with the ID = "Player".</span></span>


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a><span data-ttu-id="0c024-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c024-123">Requirements</span></span>



| <span data-ttu-id="0c024-124">需求</span><span class="sxs-lookup"><span data-stu-id="0c024-124">Requirement</span></span> | <span data-ttu-id="0c024-125">值</span><span class="sxs-lookup"><span data-stu-id="0c024-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c024-126">版本</span><span class="sxs-lookup"><span data-stu-id="0c024-126">Version</span></span><br/> | <span data-ttu-id="0c024-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0c024-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0c024-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0c024-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c024-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c024-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c024-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c024-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c024-131">**PlaylistArray 物件**</span><span class="sxs-lookup"><span data-stu-id="0c024-131">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="0c024-132">**PlaylistArray 計數**</span><span class="sxs-lookup"><span data-stu-id="0c024-132">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="0c024-133">**PlaylistCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="0c024-133">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="0c024-134">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0c024-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0c024-135">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0c024-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





