---
title: AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件
description: 將屬性值新增至程式庫時，就會發生 MediaCollectionAttributeStringAdded 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999111"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="fdba7-105">AxWindowsMediaPlayer 物件的 MediaCollectionAttributeStringAdded 事件</span><span class="sxs-lookup"><span data-stu-id="fdba7-105">MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="fdba7-106">將屬性值新增至程式庫時，就會發生 MediaCollectionAttributeStringAdded 事件。</span><span class="sxs-lookup"><span data-stu-id="fdba7-106">The MediaCollectionAttributeStringAdded event occurs when an attribute value is added to the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a><span data-ttu-id="fdba7-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="fdba7-107">Event Data</span></span>

<span data-ttu-id="fdba7-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaCollectionAttributeStringAddedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="fdba7-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEventHandler**.</span></span> <span data-ttu-id="fdba7-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="fdba7-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="fdba7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fdba7-110">Property</span></span>           | <span data-ttu-id="fdba7-111">描述</span><span class="sxs-lookup"><span data-stu-id="fdba7-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdba7-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="fdba7-112">**bstrAttribName**</span></span> | <span data-ttu-id="fdba7-113">StringSpecifies 屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdba7-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="fdba7-114">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="fdba7-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="fdba7-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="fdba7-115">bstrAttribVal</span></span>      | <span data-ttu-id="fdba7-116">StringSpecifies 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fdba7-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="fdba7-117">備註</span><span class="sxs-lookup"><span data-stu-id="fdba7-117">Remarks</span></span>

<span data-ttu-id="fdba7-118">當媒體專案加入至程式庫時，會將其中繼資料新增至媒體集合，並為每個新增的屬性引發此事件。</span><span class="sxs-lookup"><span data-stu-id="fdba7-118">When a media item is added to the library, its metadata is added to the media collection and this event is fired for each attribute added.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdba7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdba7-119">Requirements</span></span>



| <span data-ttu-id="fdba7-120">需求</span><span class="sxs-lookup"><span data-stu-id="fdba7-120">Requirement</span></span> | <span data-ttu-id="fdba7-121">值</span><span class="sxs-lookup"><span data-stu-id="fdba7-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdba7-122">版本</span><span class="sxs-lookup"><span data-stu-id="fdba7-122">Version</span></span><br/>   | <span data-ttu-id="fdba7-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="fdba7-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="fdba7-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="fdba7-124">Namespace</span></span><br/> | <span data-ttu-id="fdba7-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="fdba7-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="fdba7-126">組件</span><span class="sxs-lookup"><span data-stu-id="fdba7-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fdba7-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdba7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdba7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdba7-129">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fdba7-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fdba7-130">**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fdba7-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fdba7-131">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fdba7-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





