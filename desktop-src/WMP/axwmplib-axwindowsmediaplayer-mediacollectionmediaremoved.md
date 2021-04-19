---
title: AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件
description: 從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987911"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="1c5e2-105">AxWindowsMediaPlayer 物件的 MediaCollectionMediaRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="1c5e2-105">MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="1c5e2-106">從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。</span><span class="sxs-lookup"><span data-stu-id="1c5e2-106">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a><span data-ttu-id="1c5e2-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="1c5e2-107">Event Data</span></span>

<span data-ttu-id="1c5e2-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="1c5e2-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEventHandler**.</span></span> <span data-ttu-id="1c5e2-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="1c5e2-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="1c5e2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1c5e2-110">Property</span></span> | <span data-ttu-id="1c5e2-111">描述</span><span class="sxs-lookup"><span data-stu-id="1c5e2-111">Description</span></span>                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5e2-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="1c5e2-112">pMedia</span></span>   | <span data-ttu-id="1c5e2-113">從本機程式庫移除的 ObjectThe 媒體專案。</span><span class="sxs-lookup"><span data-stu-id="1c5e2-113">System.ObjectThe media item removed from the local library.</span></span> <span data-ttu-id="1c5e2-114">您可以將此轉換成 IWMPMedia 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="1c5e2-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c5e2-115">備註</span><span class="sxs-lookup"><span data-stu-id="1c5e2-115">Remarks</span></span>

<span data-ttu-id="1c5e2-116">只有本機程式庫才會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="1c5e2-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5e2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c5e2-117">Requirements</span></span>



| <span data-ttu-id="1c5e2-118">需求</span><span class="sxs-lookup"><span data-stu-id="1c5e2-118">Requirement</span></span> | <span data-ttu-id="1c5e2-119">值</span><span class="sxs-lookup"><span data-stu-id="1c5e2-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5e2-120">版本</span><span class="sxs-lookup"><span data-stu-id="1c5e2-120">Version</span></span><br/>   | <span data-ttu-id="1c5e2-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="1c5e2-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="1c5e2-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="1c5e2-122">Namespace</span></span><br/> | <span data-ttu-id="1c5e2-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1c5e2-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1c5e2-124">組件</span><span class="sxs-lookup"><span data-stu-id="1c5e2-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1c5e2-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="1c5e2-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c5e2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c5e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5e2-127">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1c5e2-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1c5e2-128">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1c5e2-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





