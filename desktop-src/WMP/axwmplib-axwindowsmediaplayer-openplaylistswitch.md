---
title: AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件
description: 當 DVD 上的標題開始播放時，就會發生 OpenPlaylistSwitch 事件。 |AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件 Windows Media Player
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993265"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d6307-105">AxWindowsMediaPlayer 物件的 OpenPlaylistSwitch 事件</span><span class="sxs-lookup"><span data-stu-id="d6307-105">OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d6307-106">當 DVD 上的標題開始播放時，就會發生 OpenPlaylistSwitch 事件。</span><span class="sxs-lookup"><span data-stu-id="d6307-106">The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.</span></span>

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a><span data-ttu-id="d6307-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="d6307-107">Event Data</span></span>

<span data-ttu-id="d6307-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="d6307-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEventHandler**.</span></span> <span data-ttu-id="d6307-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ OpenPlaylistSwitchEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="d6307-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d6307-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d6307-110">Property</span></span>  | <span data-ttu-id="d6307-111">描述</span><span class="sxs-lookup"><span data-stu-id="d6307-111">Description</span></span>                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6307-112">**pItem**</span><span class="sxs-lookup"><span data-stu-id="d6307-112">**pItem**</span></span> | <span data-ttu-id="d6307-113">代表標題的 ObjectObject。</span><span class="sxs-lookup"><span data-stu-id="d6307-113">System.ObjectObject representing the title.</span></span> <span data-ttu-id="d6307-114">您可以將此轉換成 IWMPPlaylist 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="d6307-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d6307-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6307-115">Requirements</span></span>



| <span data-ttu-id="d6307-116">需求</span><span class="sxs-lookup"><span data-stu-id="d6307-116">Requirement</span></span> | <span data-ttu-id="d6307-117">值</span><span class="sxs-lookup"><span data-stu-id="d6307-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6307-118">版本</span><span class="sxs-lookup"><span data-stu-id="d6307-118">Version</span></span><br/>   | <span data-ttu-id="d6307-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d6307-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d6307-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="d6307-120">Namespace</span></span><br/> | <span data-ttu-id="d6307-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d6307-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d6307-122">組件</span><span class="sxs-lookup"><span data-stu-id="d6307-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d6307-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d6307-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6307-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6307-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6307-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d6307-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d6307-126">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d6307-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





