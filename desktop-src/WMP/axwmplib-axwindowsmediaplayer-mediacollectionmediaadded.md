---
title: AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件
description: 當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984400"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="da2b8-105">AxWindowsMediaPlayer 物件的 MediaCollectionMediaAdded 事件</span><span class="sxs-lookup"><span data-stu-id="da2b8-105">MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="da2b8-106">當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。</span><span class="sxs-lookup"><span data-stu-id="da2b8-106">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a><span data-ttu-id="da2b8-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="da2b8-107">Event Data</span></span>

<span data-ttu-id="da2b8-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="da2b8-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEventHandler**.</span></span> <span data-ttu-id="da2b8-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionMediaAddedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="da2b8-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="da2b8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="da2b8-110">Property</span></span> | <span data-ttu-id="da2b8-111">描述</span><span class="sxs-lookup"><span data-stu-id="da2b8-111">Description</span></span>                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2b8-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="da2b8-112">pMedia</span></span>   | <span data-ttu-id="da2b8-113">ObjectThe 媒體專案已新增至本機程式庫。</span><span class="sxs-lookup"><span data-stu-id="da2b8-113">System.ObjectThe media item added to the local library.</span></span> <span data-ttu-id="da2b8-114">您可以將此轉換成 IWMPMedia 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="da2b8-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="da2b8-115">備註</span><span class="sxs-lookup"><span data-stu-id="da2b8-115">Remarks</span></span>

<span data-ttu-id="da2b8-116">只有本機程式庫才會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="da2b8-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="da2b8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="da2b8-117">Requirements</span></span>



| <span data-ttu-id="da2b8-118">需求</span><span class="sxs-lookup"><span data-stu-id="da2b8-118">Requirement</span></span> | <span data-ttu-id="da2b8-119">值</span><span class="sxs-lookup"><span data-stu-id="da2b8-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2b8-120">版本</span><span class="sxs-lookup"><span data-stu-id="da2b8-120">Version</span></span><br/>   | <span data-ttu-id="da2b8-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="da2b8-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="da2b8-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="da2b8-122">Namespace</span></span><br/> | <span data-ttu-id="da2b8-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="da2b8-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="da2b8-124">組件</span><span class="sxs-lookup"><span data-stu-id="da2b8-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="da2b8-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="da2b8-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da2b8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da2b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2b8-127">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="da2b8-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da2b8-128">**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="da2b8-128">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da2b8-129">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="da2b8-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da2b8-130">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="da2b8-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





