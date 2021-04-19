---
title: AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件
description: 當程式庫中的屬性值變更時，就會發生 MediaCollectionAttributeStringChanged 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996449"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4347c-105">AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringChanged 事件</span><span class="sxs-lookup"><span data-stu-id="4347c-105">MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4347c-106">當程式庫中的屬性值變更時，就會發生 MediaCollectionAttributeStringChanged 事件。</span><span class="sxs-lookup"><span data-stu-id="4347c-106">The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a><span data-ttu-id="4347c-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="4347c-107">Event Data</span></span>

<span data-ttu-id="4347c-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="4347c-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEventHandler**.</span></span> <span data-ttu-id="4347c-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="4347c-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4347c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4347c-110">Property</span></span>         | <span data-ttu-id="4347c-111">描述</span><span class="sxs-lookup"><span data-stu-id="4347c-111">Description</span></span>                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4347c-112">bstrAttribName</span><span class="sxs-lookup"><span data-stu-id="4347c-112">bstrAttribName</span></span>   | <span data-ttu-id="4347c-113">StringSpecifies 屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="4347c-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="4347c-114">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="4347c-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="4347c-115">bstrOldAttribVal</span><span class="sxs-lookup"><span data-stu-id="4347c-115">bstrOldAttribVal</span></span> | <span data-ttu-id="4347c-116">StringSpecifies 屬性的舊值。</span><span class="sxs-lookup"><span data-stu-id="4347c-116">System.StringSpecifies the old value of the attribute.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="4347c-117">bstrNewAttribVal</span><span class="sxs-lookup"><span data-stu-id="4347c-117">bstrNewAttribVal</span></span> | <span data-ttu-id="4347c-118">StringSpecifies 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="4347c-118">System.StringSpecifies the new value of the attribute.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="4347c-119">備註</span><span class="sxs-lookup"><span data-stu-id="4347c-119">Remarks</span></span>

<span data-ttu-id="4347c-120">當使用者修改程式庫中繼資料時，會更新媒體集合，並針對每個屬性變更引發此事件。</span><span class="sxs-lookup"><span data-stu-id="4347c-120">When a user modifies library metadata, the media collection is updated and this event fires for each attribute changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4347c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4347c-121">Requirements</span></span>



| <span data-ttu-id="4347c-122">需求</span><span class="sxs-lookup"><span data-stu-id="4347c-122">Requirement</span></span> | <span data-ttu-id="4347c-123">值</span><span class="sxs-lookup"><span data-stu-id="4347c-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4347c-124">版本</span><span class="sxs-lookup"><span data-stu-id="4347c-124">Version</span></span><br/>   | <span data-ttu-id="4347c-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4347c-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4347c-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="4347c-126">Namespace</span></span><br/> | <span data-ttu-id="4347c-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4347c-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4347c-128">組件</span><span class="sxs-lookup"><span data-stu-id="4347c-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4347c-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4347c-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4347c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4347c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4347c-131">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4347c-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4347c-132">**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4347c-132">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4347c-133">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4347c-133">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





