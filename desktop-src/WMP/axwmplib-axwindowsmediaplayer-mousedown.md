---
title: AxWindowsMediaPlayer 物件的 MouseDown 事件
description: 當使用者按下滑鼠按鍵時，就會發生 MouseDown 事件。 |AxWindowsMediaPlayer 物件的 MouseDown 事件
ms.assetid: 3dfbd034-67d4-4b7e-88d8-a77d301c5df7
keywords:
- AxWindowsMediaPlayer 物件的 MouseDown 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MouseDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0779df27f406691903a0362c9eb3a1df993f595f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000433"
---
# <a name="mousedown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a7a66-105">AxWindowsMediaPlayer 物件的 MouseDown 事件</span><span class="sxs-lookup"><span data-stu-id="a7a66-105">MouseDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a7a66-106">當使用者按下滑鼠按鍵時，就會發生 MouseDown 事件。</span><span class="sxs-lookup"><span data-stu-id="a7a66-106">The MouseDown event occurs when the user presses a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseDownEvent(
  object sender,
  _WMPOCXEvents_MouseDownEvent e
)

[Visual Basic]
Private Sub player_MouseDownEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseDownEvent
) Handles player.MouseDownEvent
```

## <a name="event-data"></a><span data-ttu-id="a7a66-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="a7a66-107">Event Data</span></span>

<span data-ttu-id="a7a66-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MouseDownEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="a7a66-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEventHandler**.</span></span> <span data-ttu-id="a7a66-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MouseDownEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a7a66-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="a7a66-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a7a66-110">Property</span></span>    | <span data-ttu-id="a7a66-111">描述</span><span class="sxs-lookup"><span data-stu-id="a7a66-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a66-112">nButton</span><span class="sxs-lookup"><span data-stu-id="a7a66-112">nButton</span></span>     | <span data-ttu-id="a7a66-113">Int16A 位的位，其中位對應至左按鈕 (位 0) ，右鍵 (位 1) ，中間按鈕 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="a7a66-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="a7a66-114">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="a7a66-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="a7a66-115">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="a7a66-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="a7a66-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="a7a66-116">nShiftState</span></span> | <span data-ttu-id="a7a66-117">Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="a7a66-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="a7a66-118">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="a7a66-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="a7a66-119">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="a7a66-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="a7a66-120">外匯</span><span class="sxs-lookup"><span data-stu-id="a7a66-120">fX</span></span>          | <span data-ttu-id="a7a66-121">滑鼠指標相對於控制項左上角的 Int32The X 軸座標。</span><span class="sxs-lookup"><span data-stu-id="a7a66-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="a7a66-122">財年</span><span class="sxs-lookup"><span data-stu-id="a7a66-122">fY</span></span>          | <span data-ttu-id="a7a66-123">滑鼠指標的 Int32The y 座標，相對於控制項的左上角。</span><span class="sxs-lookup"><span data-stu-id="a7a66-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="a7a66-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7a66-124">Requirements</span></span>



| <span data-ttu-id="a7a66-125">需求</span><span class="sxs-lookup"><span data-stu-id="a7a66-125">Requirement</span></span> | <span data-ttu-id="a7a66-126">值</span><span class="sxs-lookup"><span data-stu-id="a7a66-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a66-127">版本</span><span class="sxs-lookup"><span data-stu-id="a7a66-127">Version</span></span><br/>   | <span data-ttu-id="a7a66-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a7a66-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a7a66-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="a7a66-129">Namespace</span></span><br/> | <span data-ttu-id="a7a66-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a7a66-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a7a66-131">組件</span><span class="sxs-lookup"><span data-stu-id="a7a66-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a7a66-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a7a66-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7a66-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7a66-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a66-134">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a7a66-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





