---
title: '[] 方法'
description: '[] 方法會建立新的播放清單物件。'
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，Player 類別'
- Player 類別 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992796"
---
# <a name="playernewplaylist-method"></a><span data-ttu-id="d500a-106">[] 方法</span><span class="sxs-lookup"><span data-stu-id="d500a-106">Player.newPlaylist method</span></span>

<span data-ttu-id="d500a-107">**[]** 方法會建立新的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="d500a-107">The **newPlaylist** method creates a new **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d500a-108">語法</span><span class="sxs-lookup"><span data-stu-id="d500a-108">Syntax</span></span>


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="d500a-109">參數</span><span class="sxs-lookup"><span data-stu-id="d500a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d500a-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d500a-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d500a-111">包含新播放清單名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="d500a-111">**String** containing the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="d500a-112">*URL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d500a-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d500a-113">**字串** ，包含要用來建立 **播放清單** 物件之 Windows Media 中繼檔播放清單的 URL。</span><span class="sxs-lookup"><span data-stu-id="d500a-113">**String** containing the URL of the Windows Media metafile playlist to create the **Playlist** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d500a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d500a-114">Return value</span></span>

<span data-ttu-id="d500a-115">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="d500a-115">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d500a-116">備註</span><span class="sxs-lookup"><span data-stu-id="d500a-116">Remarks</span></span>

<span data-ttu-id="d500a-117">如果 *URL* 參數設定為 null 或 "" (空白字串) ，則會建立空白的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="d500a-117">If the *URL* parameter is set to null or "" (empty string), an empty **Playlist** object will be created.</span></span> <span data-ttu-id="d500a-118">如果 *name* 參數設定為 ""，則會使用中繼檔中的名稱。</span><span class="sxs-lookup"><span data-stu-id="d500a-118">If the *name* parameter is set to "", the name in the metafile is used.</span></span>

<span data-ttu-id="d500a-119">使用這個方法建立的新播放清單，不會新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="d500a-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="d500a-120">若要將新的播放清單新增至程式庫，請使用 *PlaylistCollection*。**importPlaylist** 或 *PlaylistCollection*。**[]**。</span><span class="sxs-lookup"><span data-stu-id="d500a-120">To add a new playlist to the library, use *PlaylistCollection*.**importPlaylist** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="d500a-121">新增至程式庫時，會自動移除播放清單名稱中的任何前置或尾端空格。</span><span class="sxs-lookup"><span data-stu-id="d500a-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="d500a-122">由於程式庫允許多個具有相同名稱的播放清單，因此您可能會想要先檢查具有指定名稱的播放清單是否存在，然後再新增一個。</span><span class="sxs-lookup"><span data-stu-id="d500a-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="d500a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d500a-123">Requirements</span></span>



| <span data-ttu-id="d500a-124">需求</span><span class="sxs-lookup"><span data-stu-id="d500a-124">Requirement</span></span> | <span data-ttu-id="d500a-125">值</span><span class="sxs-lookup"><span data-stu-id="d500a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d500a-126">版本</span><span class="sxs-lookup"><span data-stu-id="d500a-126">Version</span></span><br/> | <span data-ttu-id="d500a-127">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="d500a-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d500a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d500a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d500a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d500a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d500a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d500a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d500a-131">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="d500a-131">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="d500a-132">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="d500a-132">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

<span data-ttu-id="d500a-133">[**PlaylistCollection. []**](playlistcollection-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="d500a-133">[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)</span></span>
</dt> <dt>

[<span data-ttu-id="d500a-134">**Windows Media 中繼檔**</span><span class="sxs-lookup"><span data-stu-id="d500a-134">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





