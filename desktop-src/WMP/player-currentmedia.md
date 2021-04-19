---
title: CurrentMedia
description: CurrentMedia 屬性會指定或抓取目前的媒體物件。
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- CurrentMedia Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990219"
---
# <a name="playercurrentmedia"></a><span data-ttu-id="65816-104">CurrentMedia</span><span class="sxs-lookup"><span data-stu-id="65816-104">Player.currentMedia</span></span>

<span data-ttu-id="65816-105">**CurrentMedia** 屬性會指定或抓取目前的媒體物件。</span><span class="sxs-lookup"><span data-stu-id="65816-105">The **currentMedia** property specifies or retrieves the current Media object.</span></span>

## <a name="syntax"></a><span data-ttu-id="65816-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="65816-106">Syntax</span></span>

<span data-ttu-id="65816-107">*玩家* 。**currentMedia**</span><span class="sxs-lookup"><span data-stu-id="65816-107">*player* .**currentMedia**</span></span>

## <a name="possible-values"></a><span data-ttu-id="65816-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="65816-108">Possible Values</span></span>

<span data-ttu-id="65816-109">此屬性是讀取/寫入媒體物件。</span><span class="sxs-lookup"><span data-stu-id="65816-109">This property is a read/write Media object.</span></span>

## <a name="remarks"></a><span data-ttu-id="65816-110">備註</span><span class="sxs-lookup"><span data-stu-id="65816-110">Remarks</span></span>

<span data-ttu-id="65816-111">如果 *設定*，則為。**autoStart** 屬性為 true，每當您設定 **currentMedia** 時，就會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="65816-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="65816-112">這個屬性會採用媒體物件，您可以使用 *播放清單* 來取得該物件。**專案**。</span><span class="sxs-lookup"><span data-stu-id="65816-112">This property takes a Media object, which can be acquired by using *Playlist*.**item**.</span></span> <span data-ttu-id="65816-113">若要使用檔案名載入 **媒體** 專案，請設定 URL 屬性，或使用 **newMedia**。</span><span class="sxs-lookup"><span data-stu-id="65816-113">To load a **Media** item using a file name, set the URL property or use **newMedia**.</span></span>

## <a name="examples"></a><span data-ttu-id="65816-114">範例</span><span class="sxs-lookup"><span data-stu-id="65816-114">Examples</span></span>

<span data-ttu-id="65816-115">下列 JScript 範例會抓取媒體櫃中的第一個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="65816-115">The following JScript example retrieves the first media item in the library.</span></span> <span data-ttu-id="65816-116">然後，它會使用 **currentMedia** 使取出的媒體專案成為目前的媒體專案，然後顯示目前媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="65816-116">It then uses **currentMedia** to make the retrieved media item the current media item, and then to display the name of the current media item.</span></span> <span data-ttu-id="65816-117">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="65816-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a><span data-ttu-id="65816-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="65816-118">Requirements</span></span>



| <span data-ttu-id="65816-119">需求</span><span class="sxs-lookup"><span data-stu-id="65816-119">Requirement</span></span> | <span data-ttu-id="65816-120">值</span><span class="sxs-lookup"><span data-stu-id="65816-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65816-121">版本</span><span class="sxs-lookup"><span data-stu-id="65816-121">Version</span></span><br/> | <span data-ttu-id="65816-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="65816-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="65816-123">DLL</span><span class="sxs-lookup"><span data-stu-id="65816-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="65816-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65816-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65816-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65816-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65816-126">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="65816-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="65816-127">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="65816-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="65816-128">**NewMedia**</span><span class="sxs-lookup"><span data-stu-id="65816-128">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="65816-129">**播放清單。專案**</span><span class="sxs-lookup"><span data-stu-id="65816-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="65816-130">**設定。 autoStart**</span><span class="sxs-lookup"><span data-stu-id="65816-130">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





