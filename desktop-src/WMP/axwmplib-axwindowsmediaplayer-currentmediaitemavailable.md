---
title: AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件
description: 當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 CurrentMediaItemAvailable 事件。 |AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995044"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ec78f-105">AxWindowsMediaPlayer 物件的 CurrentMediaItemAvailable 事件</span><span class="sxs-lookup"><span data-stu-id="ec78f-105">CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ec78f-106">當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 CurrentMediaItemAvailable 事件。</span><span class="sxs-lookup"><span data-stu-id="ec78f-106">The CurrentMediaItemAvailable event occurs when a graphic metadata item in the current media item becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="ec78f-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="ec78f-107">Event Data</span></span>

<span data-ttu-id="ec78f-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="ec78f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEventHandler**.</span></span> <span data-ttu-id="ec78f-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CurrentMediaItemAvailableEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ec78f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="ec78f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ec78f-110">Property</span></span>     | <span data-ttu-id="ec78f-111">描述</span><span class="sxs-lookup"><span data-stu-id="ec78f-111">Description</span></span>                                                 |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="ec78f-112">bstrItemName</span><span class="sxs-lookup"><span data-stu-id="ec78f-112">bstrItemName</span></span> | <span data-ttu-id="ec78f-113">目前媒體專案的 StringThe 名稱。</span><span class="sxs-lookup"><span data-stu-id="ec78f-113">System.StringThe name of the current media item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec78f-114">備註</span><span class="sxs-lookup"><span data-stu-id="ec78f-114">Remarks</span></span>

<span data-ttu-id="ec78f-115">因為播放可以在媒體專案完全下載之前開始播放，所以媒體專案中包含的任何元資料圖形 (例如專輯封面) 在開始播放時可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="ec78f-115">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="ec78f-116">此事件會在元資料圖形專案完成下載時發出警示。</span><span class="sxs-lookup"><span data-stu-id="ec78f-116">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="ec78f-117">然後，您可以藉由將 **bstrItemName** 的值傳遞給 *IWMPMediaCollection*，來取得 **IWMPMedia** 介面。**getByName** 方法，之後您就可以使用 *IWMPMedia3* 來存取元資料圖形專案。**getItemInfoByType** 並為屬性名稱指定 **WM/圖片**。</span><span class="sxs-lookup"><span data-stu-id="ec78f-117">You can then retrieve the **IWMPMedia** interface by passing the value of **bstrItemName** to the *IWMPMediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *IWMPMedia3*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec78f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec78f-118">Requirements</span></span>



| <span data-ttu-id="ec78f-119">需求</span><span class="sxs-lookup"><span data-stu-id="ec78f-119">Requirement</span></span> | <span data-ttu-id="ec78f-120">值</span><span class="sxs-lookup"><span data-stu-id="ec78f-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec78f-121">版本</span><span class="sxs-lookup"><span data-stu-id="ec78f-121">Version</span></span><br/>   | <span data-ttu-id="ec78f-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ec78f-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ec78f-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec78f-123">Namespace</span></span><br/> | <span data-ttu-id="ec78f-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ec78f-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ec78f-125">組件</span><span class="sxs-lookup"><span data-stu-id="ec78f-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ec78f-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ec78f-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec78f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec78f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec78f-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ec78f-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ec78f-129">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ec78f-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ec78f-130">**IWMPMedia3. getItemInfoByType (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ec78f-130">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ec78f-131">**IWMPMediaCollection. getByName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ec78f-131">**IWMPMediaCollection.getByName (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





