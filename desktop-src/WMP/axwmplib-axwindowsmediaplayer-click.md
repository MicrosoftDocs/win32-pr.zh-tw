---
title: 按一下 AxWindowsMediaPlayer 物件的事件
description: 當使用者按一下 Windows Media Player 控制項上的滑鼠按鍵時，就會發生 Click 事件。
ms.assetid: 41a719a2-103a-46b5-806d-5c21c4a09e00
keywords:
- 按一下 [AxWindowsMediaPlayer] 物件的 [事件] Windows Media Player
topic_type:
- apiref
api_name:
- Click Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d316e5dc4c12e75d75dd0b292c1df6db974bc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986559"
---
# <a name="click-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="5139b-104">按一下 AxWindowsMediaPlayer 物件的事件</span><span class="sxs-lookup"><span data-stu-id="5139b-104">Click Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="5139b-105">當使用者按一下 Windows Media Player 控制項上的滑鼠按鍵時，就會發生 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="5139b-105">The Click event occurs when the user clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_OnClick(
  object  sender,
  _WMPOCXEvents_ClickEvent e
);

[Visual Basic]
Private Sub player_OnClick(  
  sender As Object,
  e As WMPOCXEvents_ClickEvent
) Handles player.ClickEvent
```

## <a name="event-data"></a><span data-ttu-id="5139b-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="5139b-106">Event Data</span></span>

<span data-ttu-id="5139b-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ ClickEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="5139b-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ClickEventHandler**.</span></span> <span data-ttu-id="5139b-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ ClickEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5139b-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="5139b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5139b-109">Property</span></span>    | <span data-ttu-id="5139b-110">描述</span><span class="sxs-lookup"><span data-stu-id="5139b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5139b-111">nButton</span><span class="sxs-lookup"><span data-stu-id="5139b-111">nButton</span></span>     | <span data-ttu-id="5139b-112">Int16A 位的位，其中位對應至左按鈕 (位 0) ，右鍵 (位 1) ，中間按鈕 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="5139b-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="5139b-113">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="5139b-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="5139b-114">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="5139b-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="5139b-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="5139b-115">nShiftState</span></span> | <span data-ttu-id="5139b-116">Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="5139b-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="5139b-117">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="5139b-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="5139b-118">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="5139b-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="5139b-119">外匯</span><span class="sxs-lookup"><span data-stu-id="5139b-119">fX</span></span>          | <span data-ttu-id="5139b-120">滑鼠指標相對於控制項左上角的 Int32The X 軸座標。</span><span class="sxs-lookup"><span data-stu-id="5139b-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="5139b-121">財年</span><span class="sxs-lookup"><span data-stu-id="5139b-121">fY</span></span>          | <span data-ttu-id="5139b-122">滑鼠指標的 Int32The y 座標，相對於控制項的左上角。</span><span class="sxs-lookup"><span data-stu-id="5139b-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="5139b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5139b-123">Requirements</span></span>



| <span data-ttu-id="5139b-124">需求</span><span class="sxs-lookup"><span data-stu-id="5139b-124">Requirement</span></span> | <span data-ttu-id="5139b-125">值</span><span class="sxs-lookup"><span data-stu-id="5139b-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5139b-126">版本</span><span class="sxs-lookup"><span data-stu-id="5139b-126">Version</span></span><br/>   | <span data-ttu-id="5139b-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="5139b-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5139b-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="5139b-128">Namespace</span></span><br/> | <span data-ttu-id="5139b-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="5139b-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5139b-130">組件</span><span class="sxs-lookup"><span data-stu-id="5139b-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5139b-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="5139b-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5139b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5139b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5139b-133">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5139b-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





