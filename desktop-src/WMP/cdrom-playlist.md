---
title: Cdrom 播放清單
description: 播放清單物件會抓取播放清單物件，此物件代表 cd 光碟機中目前的曲目，或 DVD 的根層級標題專案。
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom Windows Media Player 的播放清單
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983312"
---
# <a name="cdromplaylist"></a><span data-ttu-id="dc029-104">Cdrom 播放清單</span><span class="sxs-lookup"><span data-stu-id="dc029-104">Cdrom.playlist</span></span>

<span data-ttu-id="dc029-105">**播放** 清單物件會抓取 **播放清單** 物件，此物件代表 cd 光碟機中目前的曲目，或 DVD 的根層級標題專案。</span><span class="sxs-lookup"><span data-stu-id="dc029-105">The **playlist** property retrieves a **Playlist** object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a><span data-ttu-id="dc029-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="dc029-106">Possible Values</span></span>

<span data-ttu-id="dc029-107">這個屬性是唯讀的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="dc029-107">This property is a read-only **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc029-108">備註</span><span class="sxs-lookup"><span data-stu-id="dc029-108">Remarks</span></span>

<span data-ttu-id="dc029-109">一般而言，Dvd 會組織成標題。</span><span class="sxs-lookup"><span data-stu-id="dc029-109">Typically, DVDs are organized into titles.</span></span> <span data-ttu-id="dc029-110">每個標題都包含一或多個章節。</span><span class="sxs-lookup"><span data-stu-id="dc029-110">Each title contains one or more chapters.</span></span> <span data-ttu-id="dc029-111">每個 DVD 的撰寫方式都不同，因此使用標題和章節的方式是由內容作者決定。</span><span class="sxs-lookup"><span data-stu-id="dc029-111">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="dc029-112">若是 DVD，這個方法會抓取播放清單，其中包含代表 DVD 媒體之 **媒體** 物件的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="dc029-112">For DVD, this method retrieves a playlist that contains as the first item a **Media** object that represents the DVD media.</span></span> <span data-ttu-id="dc029-113">如果播放專案是在插入新 DVD 之後第一次播放，播放該專案會導致 DVD 播放，或在 DVD 與最後一張 DVD 相同時繼續播放。</span><span class="sxs-lookup"><span data-stu-id="dc029-113">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="dc029-114">在播放期間將這個專案設定為目前的專案，會從一開始就播放 DVD。</span><span class="sxs-lookup"><span data-stu-id="dc029-114">Setting this item as the current one during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="dc029-115">播放清單中)  (**媒體** 物件的其他專案，則是以嵌套播放清單表示的 DVD 標題。</span><span class="sxs-lookup"><span data-stu-id="dc029-115">Additional items (**Media** objects) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="dc029-116">當您指定 *控制項* 時。**currentItem** 為等於其中一個嵌套播放清單專案，Windows Media Player 會自動將嵌套播放清單設定為 *播放* 程式。開始進行章節的 **currentPlaylist** 之後。</span><span class="sxs-lookup"><span data-stu-id="dc029-116">When you specify *Controls*.**currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as *Player*.**currentPlaylist** after chapter playback begins.</span></span> <span data-ttu-id="dc029-117">然後，您可以使用 **currentPlaylist** 物件屬性、方法和事件來處理 DVD 章節，也就是播放清單專案。</span><span class="sxs-lookup"><span data-stu-id="dc029-117">You can then use the **currentPlaylist** object properties, methods, and events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="dc029-118">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="dc029-118">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="dc029-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="dc029-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="dc029-120">**Windows Media Player 10** 行動裝置版：不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="dc029-120">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="dc029-121">範例</span><span class="sxs-lookup"><span data-stu-id="dc029-121">Examples</span></span>

<span data-ttu-id="dc029-122">下列範例會使用 *光碟*。用來填滿 HTML 文字元素的 **播放清單** ，名稱為 myText，而音訊 CD 的標題則是目前位於第一個 CD 光碟機的標題。</span><span class="sxs-lookup"><span data-stu-id="dc029-122">The following example uses *Cdrom*.**playlist** to fill an HTML text element, named myText, with the titles of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="dc029-123">使用 *CdromCollection*。用來判斷可用 CD 磁片磁碟機數目的 **計數** 。</span><span class="sxs-lookup"><span data-stu-id="dc029-123">Use *CdromCollection*.**count** to determine the number of available CD drives.</span></span> <span data-ttu-id="dc029-124">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="dc029-124">The **Player** object was created with ID = "Player".</span></span>


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a><span data-ttu-id="dc029-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc029-125">Requirements</span></span>



| <span data-ttu-id="dc029-126">需求</span><span class="sxs-lookup"><span data-stu-id="dc029-126">Requirement</span></span> | <span data-ttu-id="dc029-127">值</span><span class="sxs-lookup"><span data-stu-id="dc029-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc029-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc029-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dc029-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc029-129">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc029-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc029-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dc029-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc029-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dc029-132">版本</span><span class="sxs-lookup"><span data-stu-id="dc029-132">Version</span></span><br/>                  | <span data-ttu-id="dc029-133">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="dc029-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dc029-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dc029-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc029-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc029-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc029-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc029-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc029-137">**Cdrom 物件**</span><span class="sxs-lookup"><span data-stu-id="dc029-137">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="dc029-138">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="dc029-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="dc029-139">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="dc029-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





