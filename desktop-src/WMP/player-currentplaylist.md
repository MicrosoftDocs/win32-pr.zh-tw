---
title: CurrentPlaylist
description: CurrentPlaylist 屬性會指定或抓取目前的播放清單物件。
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- CurrentPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980154"
---
# <a name="playercurrentplaylist"></a><span data-ttu-id="a3855-104">CurrentPlaylist</span><span class="sxs-lookup"><span data-stu-id="a3855-104">Player.currentPlaylist</span></span>

<span data-ttu-id="a3855-105">CurrentPlaylist 屬性會指定或抓取目前的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="a3855-105">The currentPlaylist property specifies or retrieves the current **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3855-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3855-106">Syntax</span></span>

<span data-ttu-id="a3855-107">*玩家* 。**currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="a3855-107">*player* .**currentPlaylist**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a3855-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="a3855-108">Possible Values</span></span>

<span data-ttu-id="a3855-109">此屬性是讀取/寫入 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="a3855-109">This property is a read/write **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3855-110">備註</span><span class="sxs-lookup"><span data-stu-id="a3855-110">Remarks</span></span>

<span data-ttu-id="a3855-111">如果 *設定*，則為。**autoStart** 屬性為 true，每當您設定 **currentPlaylist** 時，就會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="a3855-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="a3855-112">這個屬性會採用播放清單物件，可以透過數種方式取得，例如藉由呼叫 *PlaylistArray*。**專案** 或 *PlaylistCollection*。**[]**。</span><span class="sxs-lookup"><span data-stu-id="a3855-112">This property takes a Playlist object, which can be acquired in several ways, such as by calling *PlaylistArray*.**item** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="a3855-113">若要使用檔案名載入 **播放清單** 專案，請設定 URL 屬性或使用 *播放* 清單。**[]**。</span><span class="sxs-lookup"><span data-stu-id="a3855-113">To load a **Playlist** item using a file name, set the URL property or use *Player*.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="a3855-114">範例</span><span class="sxs-lookup"><span data-stu-id="a3855-114">Examples</span></span>

<span data-ttu-id="a3855-115">下列 JScript 範例會抓取媒體櫃中的第一個播放清單。</span><span class="sxs-lookup"><span data-stu-id="a3855-115">The following JScript example retrieves the first playlist in the library.</span></span> <span data-ttu-id="a3855-116">然後，它會使用 **currentPlaylist** 讓抓取的播放清單成為目前的播放清單，然後顯示目前播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3855-116">It then uses **currentPlaylist** to make the retrieved playlist the current playlist, and then to display the name of the current playlist.</span></span> <span data-ttu-id="a3855-117">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="a3855-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a><span data-ttu-id="a3855-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3855-118">Requirements</span></span>



| <span data-ttu-id="a3855-119">需求</span><span class="sxs-lookup"><span data-stu-id="a3855-119">Requirement</span></span> | <span data-ttu-id="a3855-120">值</span><span class="sxs-lookup"><span data-stu-id="a3855-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3855-121">版本</span><span class="sxs-lookup"><span data-stu-id="a3855-121">Version</span></span><br/> | <span data-ttu-id="a3855-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a3855-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a3855-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a3855-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3855-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3855-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3855-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3855-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3855-126">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="a3855-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

<span data-ttu-id="a3855-127">[**[]**](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="a3855-127">[**Player.newPlaylist**](player-newplaylist.md)</span></span>
</dt> <dt>

[<span data-ttu-id="a3855-128">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="a3855-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="a3855-129">**PlaylistArray 專案**</span><span class="sxs-lookup"><span data-stu-id="a3855-129">**PlaylistArray.item**</span></span>](playlistarray-item.md)
</dt> <dt>

<span data-ttu-id="a3855-130">[**PlaylistCollection. []**](playlistcollection-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="a3855-130">[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)</span></span>
</dt> <dt>

[<span data-ttu-id="a3855-131">**設定。 autoStart**</span><span class="sxs-lookup"><span data-stu-id="a3855-131">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





