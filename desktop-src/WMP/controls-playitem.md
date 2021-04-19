---
title: PlayItem 方法
description: PlayItem 方法會播放指定的媒體專案。 |PlayItem 方法
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- playItem 方法 Windows Media Player
- playItem 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，playItem 方法
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000943"
---
# <a name="controlsplayitem-method"></a><span data-ttu-id="931a2-107">PlayItem 方法</span><span class="sxs-lookup"><span data-stu-id="931a2-107">Controls.playItem method</span></span>

<span data-ttu-id="931a2-108">**PlayItem** 方法會播放指定的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="931a2-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="931a2-109">語法</span><span class="sxs-lookup"><span data-stu-id="931a2-109">Syntax</span></span>


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a><span data-ttu-id="931a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="931a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="931a2-111">*theMediaItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="931a2-111">*theMediaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="931a2-112">要播放的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="931a2-112">**Media** object to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="931a2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="931a2-113">Return value</span></span>

<span data-ttu-id="931a2-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="931a2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="931a2-115">備註</span><span class="sxs-lookup"><span data-stu-id="931a2-115">Remarks</span></span>

<span data-ttu-id="931a2-116">無論 *設定* 的值為何，都會自動載入並播放媒體專案。**autoStart** 屬性。</span><span class="sxs-lookup"><span data-stu-id="931a2-116">The media item will be loaded and played automatically, regardless of the value of the *Settings*.**autoStart** property.</span></span> <span data-ttu-id="931a2-117">若要載入專案而不自動播放，請 *設定 [設定]*。**自動啟動** 至 false，並將值指派給 *Player*。**URL**，之後可以呼叫 **播放** 來開始播放專案。</span><span class="sxs-lookup"><span data-stu-id="931a2-117">To load an item without playing it automatically, set *Settings*.**autoStart** to false and assign a value to *Player*.**URL**, after which **play** can be called to start playing the item.</span></span>

<span data-ttu-id="931a2-118">注意</span><span class="sxs-lookup"><span data-stu-id="931a2-118">Note</span></span>

<span data-ttu-id="931a2-119">**playItem** 僅適用于 *currentPlaylist* 中的專案。</span><span class="sxs-lookup"><span data-stu-id="931a2-119">**playItem** works only with items in *currentPlaylist*.</span></span> <span data-ttu-id="931a2-120">不支援使用已儲存媒體專案的參考來呼叫 **playItem** 。</span><span class="sxs-lookup"><span data-stu-id="931a2-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="931a2-121">範例</span><span class="sxs-lookup"><span data-stu-id="931a2-121">Examples</span></span>

<span data-ttu-id="931a2-122">下列 JScript 範例會使用 **playItem** 來播放目前播放清單中的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="931a2-122">The following JScript example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="931a2-123">您可以根據播放清單中的位置，選擇要播放的專案。</span><span class="sxs-lookup"><span data-stu-id="931a2-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="931a2-124">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="931a2-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a><span data-ttu-id="931a2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="931a2-125">Requirements</span></span>



| <span data-ttu-id="931a2-126">需求</span><span class="sxs-lookup"><span data-stu-id="931a2-126">Requirement</span></span> | <span data-ttu-id="931a2-127">值</span><span class="sxs-lookup"><span data-stu-id="931a2-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="931a2-128">版本</span><span class="sxs-lookup"><span data-stu-id="931a2-128">Version</span></span><br/> | <span data-ttu-id="931a2-129">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="931a2-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="931a2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="931a2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="931a2-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="931a2-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="931a2-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="931a2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="931a2-133">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="931a2-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="931a2-134">**播放清單。專案**</span><span class="sxs-lookup"><span data-stu-id="931a2-134">**Playlist.item**</span></span>](playlist-item.md)
</dt> </dl>

 

 





