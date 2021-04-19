---
title: AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件
description: 當播放清單新增至播放清單集合時，就會發生 PlaylistCollectionPlaylistAdded 事件。 |AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001176"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="59821-105">AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistAdded 事件</span><span class="sxs-lookup"><span data-stu-id="59821-105">PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="59821-106">當播放清單新增至播放清單集合時，就會發生 PlaylistCollectionPlaylistAdded 事件。</span><span class="sxs-lookup"><span data-stu-id="59821-106">The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a><span data-ttu-id="59821-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="59821-107">Event Data</span></span>

<span data-ttu-id="59821-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="59821-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEventHandler**.</span></span> <span data-ttu-id="59821-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="59821-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="59821-110">屬性</span><span class="sxs-lookup"><span data-stu-id="59821-110">Property</span></span>             | <span data-ttu-id="59821-111">描述</span><span class="sxs-lookup"><span data-stu-id="59821-111">Description</span></span>                                                                |
|----------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="59821-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="59821-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="59821-113">StringSpecifies 已新增的播放清單名稱。</span><span class="sxs-lookup"><span data-stu-id="59821-113">System.StringSpecifies the name of the playlist that was added.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59821-114">備註</span><span class="sxs-lookup"><span data-stu-id="59821-114">Remarks</span></span>

<span data-ttu-id="59821-115">已新增的播放清單名稱可用來使用 IWMPPlaylistCollection 來取出對應的播放清單。**getByName** 方法。</span><span class="sxs-lookup"><span data-stu-id="59821-115">The name of the playlist that was added can be used to retrieve the corresponding playlist by using the IWMPPlaylistCollection.**getByName** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="59821-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="59821-116">Requirements</span></span>



| <span data-ttu-id="59821-117">需求</span><span class="sxs-lookup"><span data-stu-id="59821-117">Requirement</span></span> | <span data-ttu-id="59821-118">值</span><span class="sxs-lookup"><span data-stu-id="59821-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59821-119">版本</span><span class="sxs-lookup"><span data-stu-id="59821-119">Version</span></span><br/>   | <span data-ttu-id="59821-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="59821-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="59821-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="59821-121">Namespace</span></span><br/> | <span data-ttu-id="59821-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="59821-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="59821-123">組件</span><span class="sxs-lookup"><span data-stu-id="59821-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="59821-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="59821-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59821-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59821-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59821-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59821-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59821-127">**IWMPPlaylistCollection. getByName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59821-127">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





