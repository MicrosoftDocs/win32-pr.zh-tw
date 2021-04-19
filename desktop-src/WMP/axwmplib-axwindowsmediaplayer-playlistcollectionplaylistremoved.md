---
title: AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件
description: 從播放清單集合中移除播放清單時，就會發生 PlaylistCollectionPlaylistRemoved 事件。 |AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993539"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="0c34c-105">AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="0c34c-105">PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="0c34c-106">從播放清單集合中移除播放清單時，就會發生 PlaylistCollectionPlaylistRemoved 事件。</span><span class="sxs-lookup"><span data-stu-id="0c34c-106">The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a><span data-ttu-id="0c34c-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="0c34c-107">Event Data</span></span>

<span data-ttu-id="0c34c-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="0c34c-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEventHandler**.</span></span> <span data-ttu-id="0c34c-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0c34c-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="0c34c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0c34c-110">Property</span></span>             | <span data-ttu-id="0c34c-111">描述</span><span class="sxs-lookup"><span data-stu-id="0c34c-111">Description</span></span>                                                                  |
|----------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0c34c-112">**bstrPlaylistName**</span><span class="sxs-lookup"><span data-stu-id="0c34c-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="0c34c-113">StringSpecifies 已移除的播放清單名稱。</span><span class="sxs-lookup"><span data-stu-id="0c34c-113">System.StringSpecifies the name of the playlist that was removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0c34c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c34c-114">Requirements</span></span>



| <span data-ttu-id="0c34c-115">需求</span><span class="sxs-lookup"><span data-stu-id="0c34c-115">Requirement</span></span> | <span data-ttu-id="0c34c-116">值</span><span class="sxs-lookup"><span data-stu-id="0c34c-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c34c-117">版本</span><span class="sxs-lookup"><span data-stu-id="0c34c-117">Version</span></span><br/>   | <span data-ttu-id="0c34c-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="0c34c-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0c34c-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c34c-119">Namespace</span></span><br/> | <span data-ttu-id="0c34c-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0c34c-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0c34c-121">組件</span><span class="sxs-lookup"><span data-stu-id="0c34c-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0c34c-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="0c34c-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c34c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c34c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c34c-124">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0c34c-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0c34c-125">**IWMPPlaylistCollection. getByName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0c34c-125">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





