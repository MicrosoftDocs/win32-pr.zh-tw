---
title: PlaylistCollection 物件
description: PlaylistCollection 物件提供一種方式來組織播放清單。
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- PlaylistCollection 物件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965615"
---
# <a name="playlistcollection-object"></a><span data-ttu-id="d7687-104">PlaylistCollection 物件</span><span class="sxs-lookup"><span data-stu-id="d7687-104">PlaylistCollection Object</span></span>

<span data-ttu-id="d7687-105">**PlaylistCollection** 物件提供一種方式來組織播放清單。</span><span class="sxs-lookup"><span data-stu-id="d7687-105">The **PlaylistCollection** object provides a way to organize your playlists.</span></span>

<span data-ttu-id="d7687-106">**PlaylistCollection** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="d7687-106">The **PlaylistCollection** object supports the following methods.</span></span>



| <span data-ttu-id="d7687-107">方法</span><span class="sxs-lookup"><span data-stu-id="d7687-107">Method</span></span>                                                  | <span data-ttu-id="d7687-108">描述</span><span class="sxs-lookup"><span data-stu-id="d7687-108">Description</span></span>                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7687-109">getAll</span><span class="sxs-lookup"><span data-stu-id="d7687-109">getAll</span></span>](playlistcollection-getall.md)                 | <span data-ttu-id="d7687-110">抓取 [PlaylistArray](playlistarray-object.md) 物件，其中包含文件庫中的所有播放清單。</span><span class="sxs-lookup"><span data-stu-id="d7687-110">Retrieves a [PlaylistArray](playlistarray-object.md) object containing all the playlists in the library.</span></span>                |
| [<span data-ttu-id="d7687-111">getByName</span><span class="sxs-lookup"><span data-stu-id="d7687-111">getByName</span></span>](playlistcollection-getbyname.md)           | <span data-ttu-id="d7687-112">抓取 [PlaylistArray](playlistarray-object.md) 物件，其中包含具有指定名稱的播放清單（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d7687-112">Retrieves a [PlaylistArray](playlistarray-object.md) object containing playlists with the specified name, if any exist.</span></span> |
| [<span data-ttu-id="d7687-113">importPlaylist</span><span class="sxs-lookup"><span data-stu-id="d7687-113">importPlaylist</span></span>](playlistcollection-importplaylist.md) | <span data-ttu-id="d7687-114">將靜態播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="d7687-114">Adds a static playlist to the library.</span></span>                                                                                   |
| [<span data-ttu-id="d7687-115">isDeleted</span><span class="sxs-lookup"><span data-stu-id="d7687-115">isDeleted</span></span>](playlistcollection-isdeleted.md)           | <span data-ttu-id="d7687-116">抓取值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="d7687-116">Retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>                              |
| <span data-ttu-id="d7687-117">[[]](playlistcollection-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="d7687-117">[newPlaylist](playlistcollection-newplaylist.md)</span></span>       | <span data-ttu-id="d7687-118">在文件庫中建立新的播放清單。</span><span class="sxs-lookup"><span data-stu-id="d7687-118">Creates a new playlist in the library.</span></span>                                                                                   |
| [<span data-ttu-id="d7687-119">remove</span><span class="sxs-lookup"><span data-stu-id="d7687-119">remove</span></span>](playlistcollection-remove.md)                 | <span data-ttu-id="d7687-120">從媒體櫃移除播放清單。</span><span class="sxs-lookup"><span data-stu-id="d7687-120">Removes a playlist from the library.</span></span>                                                                                     |
| [<span data-ttu-id="d7687-121">setDeleted</span><span class="sxs-lookup"><span data-stu-id="d7687-121">setDeleted</span></span>](playlistcollection-setdeleted.md)         | <span data-ttu-id="d7687-122">移動播放清單至 [刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="d7687-122">Moves a playlist to the deleted items folder.</span></span>                                                                            |



 

<span data-ttu-id="d7687-123">**PlaylistCollection** 物件是透過下列屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="d7687-123">The **PlaylistCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="d7687-124">Object</span><span class="sxs-lookup"><span data-stu-id="d7687-124">Object</span></span>                      | <span data-ttu-id="d7687-125">屬性</span><span class="sxs-lookup"><span data-stu-id="d7687-125">Property</span></span>                                            |
|-----------------------------|-----------------------------------------------------|
| [<span data-ttu-id="d7687-126">球員</span><span class="sxs-lookup"><span data-stu-id="d7687-126">Player</span></span>](player-object.md) | [<span data-ttu-id="d7687-127">playlistCollection</span><span class="sxs-lookup"><span data-stu-id="d7687-127">playlistCollection</span></span>](player-playlistcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="d7687-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7687-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7687-129">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="d7687-129">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




