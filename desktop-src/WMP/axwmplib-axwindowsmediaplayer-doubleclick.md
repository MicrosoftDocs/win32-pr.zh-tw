---
title: AxWindowsMediaPlayer 物件的 DoubleClick 事件
description: 當使用者按兩下 Windows Media Player 控制項上的滑鼠按鍵時，就會發生 DoubleClick 事件。
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- AxWindowsMediaPlayer 物件的 DoubleClick 事件 Windows Media Player
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995720"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2ca3f-104">AxWindowsMediaPlayer 物件的 DoubleClick 事件</span><span class="sxs-lookup"><span data-stu-id="2ca3f-104">DoubleClick Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2ca3f-105">當使用者按兩下 Windows Media Player 控制項上的滑鼠按鍵時，就會發生 DoubleClick 事件。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-105">The DoubleClick event occurs when the user double-clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a><span data-ttu-id="2ca3f-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="2ca3f-106">Event Data</span></span>

<span data-ttu-id="2ca3f-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ DoubleClickEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEventHandler**.</span></span> <span data-ttu-id="2ca3f-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ DoubleClickEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="2ca3f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2ca3f-109">Property</span></span>    | <span data-ttu-id="2ca3f-110">描述</span><span class="sxs-lookup"><span data-stu-id="2ca3f-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca3f-111">nButton</span><span class="sxs-lookup"><span data-stu-id="2ca3f-111">nButton</span></span>     | <span data-ttu-id="2ca3f-112">Int16A 位的位，其中位對應至左按鈕 (位 0) ，右鍵 (位 1) ，中間按鈕 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="2ca3f-113">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2ca3f-114">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="2ca3f-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="2ca3f-115">nShiftState</span></span> | <span data-ttu-id="2ca3f-116">Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="2ca3f-117">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2ca3f-118">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="2ca3f-119">外匯</span><span class="sxs-lookup"><span data-stu-id="2ca3f-119">fX</span></span>          | <span data-ttu-id="2ca3f-120">滑鼠指標相對於控制項左上角的 Int32The X 軸座標。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="2ca3f-121">財年</span><span class="sxs-lookup"><span data-stu-id="2ca3f-121">fY</span></span>          | <span data-ttu-id="2ca3f-122">滑鼠指標的 Int32The y 座標，相對於控制項的左上角。</span><span class="sxs-lookup"><span data-stu-id="2ca3f-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="2ca3f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ca3f-123">Requirements</span></span>



| <span data-ttu-id="2ca3f-124">需求</span><span class="sxs-lookup"><span data-stu-id="2ca3f-124">Requirement</span></span> | <span data-ttu-id="2ca3f-125">值</span><span class="sxs-lookup"><span data-stu-id="2ca3f-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca3f-126">版本</span><span class="sxs-lookup"><span data-stu-id="2ca3f-126">Version</span></span><br/>   | <span data-ttu-id="2ca3f-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2ca3f-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2ca3f-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="2ca3f-128">Namespace</span></span><br/> | <span data-ttu-id="2ca3f-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2ca3f-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2ca3f-130">組件</span><span class="sxs-lookup"><span data-stu-id="2ca3f-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2ca3f-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2ca3f-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca3f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ca3f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca3f-133">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2ca3f-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





