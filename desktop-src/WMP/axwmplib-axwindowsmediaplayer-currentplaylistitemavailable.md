---
title: AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件
description: 當目前的播放清單變成可用時，就會發生 CurrentPlaylistItemAvailable 事件。 |AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997662"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="5c9aa-105">AxWindowsMediaPlayer 物件的 CurrentPlaylistItemAvailable 事件</span><span class="sxs-lookup"><span data-stu-id="5c9aa-105">CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="5c9aa-106">當目前的播放清單變成可用時，就會發生 CurrentPlaylistItemAvailable 事件。</span><span class="sxs-lookup"><span data-stu-id="5c9aa-106">The CurrentPlaylistItemAvailable event occurs when the current playlist becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="5c9aa-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="5c9aa-107">Event Data</span></span>

<span data-ttu-id="5c9aa-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="5c9aa-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEventHandler**.</span></span> <span data-ttu-id="5c9aa-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5c9aa-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="5c9aa-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5c9aa-110">Property</span></span>         | <span data-ttu-id="5c9aa-111">描述</span><span class="sxs-lookup"><span data-stu-id="5c9aa-111">Description</span></span>                                                    |
|------------------|----------------------------------------------------------------|
| <span data-ttu-id="5c9aa-112">**bstrItemName**</span><span class="sxs-lookup"><span data-stu-id="5c9aa-112">**bstrItemName**</span></span> | <span data-ttu-id="5c9aa-113">目前播放清單專案的 StringThe 名稱。</span><span class="sxs-lookup"><span data-stu-id="5c9aa-113">System.StringThe name of the current playlist item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c9aa-114">備註</span><span class="sxs-lookup"><span data-stu-id="5c9aa-114">Remarks</span></span>

<span data-ttu-id="5c9aa-115">目前播放清單的名稱可以用來從 IWMPPlaylistCollection. getByName 方法所傳回的 IWMPPlaylistArray 介面取出對應的 **IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="5c9aa-115">The name of the current playlist can be used to retrieve the corresponding **IWMPPlaylist** interface from the IWMPPlaylistArray interface that is returned from the IWMPPlaylistCollection.getByName method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9aa-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c9aa-116">Requirements</span></span>



| <span data-ttu-id="5c9aa-117">需求</span><span class="sxs-lookup"><span data-stu-id="5c9aa-117">Requirement</span></span> | <span data-ttu-id="5c9aa-118">值</span><span class="sxs-lookup"><span data-stu-id="5c9aa-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9aa-119">版本</span><span class="sxs-lookup"><span data-stu-id="5c9aa-119">Version</span></span><br/>   | <span data-ttu-id="5c9aa-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="5c9aa-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5c9aa-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="5c9aa-121">Namespace</span></span><br/> | <span data-ttu-id="5c9aa-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="5c9aa-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5c9aa-123">組件</span><span class="sxs-lookup"><span data-stu-id="5c9aa-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5c9aa-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="5c9aa-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9aa-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c9aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9aa-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5c9aa-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c9aa-127">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5c9aa-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c9aa-128">**IWMPPlaylistArray 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5c9aa-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5c9aa-129">**IWMPPlaylistCollection. getByName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5c9aa-129">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





