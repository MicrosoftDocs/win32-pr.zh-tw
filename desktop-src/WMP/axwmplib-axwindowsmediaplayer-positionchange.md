---
title: AxWindowsMediaPlayer 物件的 PositionChange 事件
description: 當媒體專案中目前的播放位置變更時，就會發生 PositionChange 事件。
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- AxWindowsMediaPlayer 物件的 PositionChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999159"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="08297-104">AxWindowsMediaPlayer 物件的 PositionChange 事件</span><span class="sxs-lookup"><span data-stu-id="08297-104">PositionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="08297-105">當媒體專案中目前的播放位置變更時，就會發生 PositionChange 事件。</span><span class="sxs-lookup"><span data-stu-id="08297-105">The PositionChange event occurs when the current playback position within the media item has been changed.</span></span>

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a><span data-ttu-id="08297-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="08297-106">Event Data</span></span>

<span data-ttu-id="08297-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PositionChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="08297-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEventHandler**.</span></span> <span data-ttu-id="08297-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PositionChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="08297-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="08297-109">屬性</span><span class="sxs-lookup"><span data-stu-id="08297-109">Property</span></span>    | <span data-ttu-id="08297-110">描述</span><span class="sxs-lookup"><span data-stu-id="08297-110">Description</span></span>                                         |
|-------------|-----------------------------------------------------|
| <span data-ttu-id="08297-111">oldPosition</span><span class="sxs-lookup"><span data-stu-id="08297-111">oldPosition</span></span> | <span data-ttu-id="08297-112">DoubleSpecifies 舊的位置。</span><span class="sxs-lookup"><span data-stu-id="08297-112">System.DoubleSpecifies the old position.</span></span><br/> |
| <span data-ttu-id="08297-113">newPosition</span><span class="sxs-lookup"><span data-stu-id="08297-113">newPosition</span></span> | <span data-ttu-id="08297-114">DoubleSpecifies 新的位置。</span><span class="sxs-lookup"><span data-stu-id="08297-114">System.DoubleSpecifies the new position.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08297-115">備註</span><span class="sxs-lookup"><span data-stu-id="08297-115">Remarks</span></span>

<span data-ttu-id="08297-116">此事件不會在播放期間定期引發。</span><span class="sxs-lookup"><span data-stu-id="08297-116">This event is not raised routinely during playback.</span></span> <span data-ttu-id="08297-117">只有在主動變更播放媒體專案的目前位置時（例如當使用者移動搜尋控制碼，或執行程式碼以指定 IWMPControls 的值）時，才會發生此問題。**currentPosition**。</span><span class="sxs-lookup"><span data-stu-id="08297-117">It only occurs when something actively changes the current position of the playing media item, such as when the user moves the seek handle or when code is executed that specifies a value for IWMPControls.**currentPosition**.</span></span>

## <a name="requirements"></a><span data-ttu-id="08297-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="08297-118">Requirements</span></span>



| <span data-ttu-id="08297-119">需求</span><span class="sxs-lookup"><span data-stu-id="08297-119">Requirement</span></span> | <span data-ttu-id="08297-120">值</span><span class="sxs-lookup"><span data-stu-id="08297-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08297-121">版本</span><span class="sxs-lookup"><span data-stu-id="08297-121">Version</span></span><br/>   | <span data-ttu-id="08297-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="08297-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="08297-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="08297-123">Namespace</span></span><br/> | <span data-ttu-id="08297-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="08297-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="08297-125">組件</span><span class="sxs-lookup"><span data-stu-id="08297-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="08297-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="08297-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08297-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08297-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08297-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="08297-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="08297-129">**IWMPControls. currentPosition (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="08297-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





