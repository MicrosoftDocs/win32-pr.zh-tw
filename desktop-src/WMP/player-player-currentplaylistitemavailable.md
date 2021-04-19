---
title: CurrentPlaylistItemAvailable 事件
description: 當目前的播放清單變成可用時，就會發生 CurrentPlaylistItemAvailable 事件。 |CurrentPlaylistItemAvailable 事件
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- CurrentPlaylistItemAvailable 事件 Windows Media Player
- CurrentPlaylistItemAvailable 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentPlaylistItemAvailable 事件
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997705"
---
# <a name="playercurrentplaylistitemavailable-event"></a><span data-ttu-id="4277e-107">CurrentPlaylistItemAvailable 事件</span><span class="sxs-lookup"><span data-stu-id="4277e-107">Player.CurrentPlaylistItemAvailable event</span></span>

<span data-ttu-id="4277e-108">當目前的播放清單變成可用時，就會發生 **CurrentPlaylistItemAvailable** 事件。</span><span class="sxs-lookup"><span data-stu-id="4277e-108">The **CurrentPlaylistItemAvailable** event occurs when the current playlist becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="4277e-109">語法</span><span class="sxs-lookup"><span data-stu-id="4277e-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="4277e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4277e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4277e-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="4277e-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="4277e-112">包含目前播放清單專案名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="4277e-112">**String** containing the name of the current playlist item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4277e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4277e-113">Return value</span></span>

<span data-ttu-id="4277e-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4277e-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4277e-115">備註</span><span class="sxs-lookup"><span data-stu-id="4277e-115">Remarks</span></span>

<span data-ttu-id="4277e-116">目前播放清單的名稱可以用來使用 *PlaylistCollection* 來取出對應的 **播放清單** 物件。**getByName** 方法。</span><span class="sxs-lookup"><span data-stu-id="4277e-116">The name of the current playlist can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="4277e-117">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="4277e-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="4277e-118">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="4277e-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="4277e-119">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4277e-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4277e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4277e-120">Requirements</span></span>



| <span data-ttu-id="4277e-121">需求</span><span class="sxs-lookup"><span data-stu-id="4277e-121">Requirement</span></span> | <span data-ttu-id="4277e-122">值</span><span class="sxs-lookup"><span data-stu-id="4277e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4277e-123">版本</span><span class="sxs-lookup"><span data-stu-id="4277e-123">Version</span></span><br/> | <span data-ttu-id="4277e-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4277e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4277e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4277e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4277e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4277e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4277e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4277e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4277e-128">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="4277e-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="4277e-129">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="4277e-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="4277e-130">**PlaylistCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="4277e-130">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





