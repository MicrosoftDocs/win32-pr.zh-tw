---
title: AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件
description: 從程式庫移除屬性值時，就會發生 MediaCollectionAttributeStringRemoved 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975954"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4da7e-105">AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="4da7e-105">MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4da7e-106">從程式庫移除屬性值時，就會發生 MediaCollectionAttributeStringRemoved 事件。</span><span class="sxs-lookup"><span data-stu-id="4da7e-106">The MediaCollectionAttributeStringRemoved event occurs when an attribute value is removed from the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a><span data-ttu-id="4da7e-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="4da7e-107">Event Data</span></span>

<span data-ttu-id="4da7e-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="4da7e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEventHandler**.</span></span> <span data-ttu-id="4da7e-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="4da7e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4da7e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4da7e-110">Property</span></span>           | <span data-ttu-id="4da7e-111">描述</span><span class="sxs-lookup"><span data-stu-id="4da7e-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da7e-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="4da7e-112">**bstrAttribName**</span></span> | <span data-ttu-id="4da7e-113">StringSpecifies 屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="4da7e-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="4da7e-114">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="4da7e-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="4da7e-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="4da7e-115">bstrAttribVal</span></span>      | <span data-ttu-id="4da7e-116">StringSpecifies 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="4da7e-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="4da7e-117">備註</span><span class="sxs-lookup"><span data-stu-id="4da7e-117">Remarks</span></span>

<span data-ttu-id="4da7e-118">從程式庫中移除媒體專案時，會從 **MediaCollection** 中移除其中繼資料，並針對移除的每個屬性引發此事件。</span><span class="sxs-lookup"><span data-stu-id="4da7e-118">When a media item is removed from the library, its metadata is removed from the **MediaCollection** and this event is fired for each attribute removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da7e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4da7e-119">Requirements</span></span>



| <span data-ttu-id="4da7e-120">需求</span><span class="sxs-lookup"><span data-stu-id="4da7e-120">Requirement</span></span> | <span data-ttu-id="4da7e-121">值</span><span class="sxs-lookup"><span data-stu-id="4da7e-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da7e-122">版本</span><span class="sxs-lookup"><span data-stu-id="4da7e-122">Version</span></span><br/>   | <span data-ttu-id="4da7e-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4da7e-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4da7e-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="4da7e-124">Namespace</span></span><br/> | <span data-ttu-id="4da7e-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4da7e-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4da7e-126">組件</span><span class="sxs-lookup"><span data-stu-id="4da7e-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4da7e-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4da7e-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da7e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4da7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da7e-129">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4da7e-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4da7e-130">**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4da7e-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4da7e-131">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4da7e-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





