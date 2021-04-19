---
title: AxWindowsMediaPlayer 物件的 PlaylistChange 事件
description: 當播放清單變更時，就會發生 PlaylistChange 事件。 |AxWindowsMediaPlayer 物件的 PlaylistChange 事件
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990800"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ed9ea-105">AxWindowsMediaPlayer 物件的 PlaylistChange 事件</span><span class="sxs-lookup"><span data-stu-id="ed9ea-105">PlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ed9ea-106">當播放清單變更時，就會發生 PlaylistChange 事件。</span><span class="sxs-lookup"><span data-stu-id="ed9ea-106">The PlaylistChange event occurs when a playlist changes.</span></span>

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="ed9ea-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="ed9ea-107">Event Data</span></span>

<span data-ttu-id="ed9ea-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlaylistChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="ed9ea-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEventHandler**.</span></span> <span data-ttu-id="ed9ea-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlaylistChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ed9ea-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="ed9ea-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ed9ea-110">Property</span></span>     | <span data-ttu-id="ed9ea-111">描述</span><span class="sxs-lookup"><span data-stu-id="ed9ea-111">Description</span></span>                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9ea-112">**播放清單**</span><span class="sxs-lookup"><span data-stu-id="ed9ea-112">**playlist**</span></span> | <span data-ttu-id="ed9ea-113">已變更的 ObjectThe 物件。</span><span class="sxs-lookup"><span data-stu-id="ed9ea-113">System.ObjectThe object which changed.</span></span> <span data-ttu-id="ed9ea-114">您可以將此轉換成 IWMPPlaylist 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="ed9ea-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/>                |
| <span data-ttu-id="ed9ea-115">**change**</span><span class="sxs-lookup"><span data-stu-id="ed9ea-115">**change**</span></span>   | <span data-ttu-id="ed9ea-116">WMPLib. WMPPlaylistChangeEventTypeAn 列舉值，指出播放清單所發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="ed9ea-116">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ed9ea-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed9ea-117">Requirements</span></span>



| <span data-ttu-id="ed9ea-118">需求</span><span class="sxs-lookup"><span data-stu-id="ed9ea-118">Requirement</span></span> | <span data-ttu-id="ed9ea-119">值</span><span class="sxs-lookup"><span data-stu-id="ed9ea-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9ea-120">版本</span><span class="sxs-lookup"><span data-stu-id="ed9ea-120">Version</span></span><br/>   | <span data-ttu-id="ed9ea-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ed9ea-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ed9ea-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="ed9ea-122">Namespace</span></span><br/> | <span data-ttu-id="ed9ea-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ed9ea-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ed9ea-124">組件</span><span class="sxs-lookup"><span data-stu-id="ed9ea-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ed9ea-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ed9ea-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed9ea-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed9ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed9ea-127">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ed9ea-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed9ea-128">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ed9ea-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





