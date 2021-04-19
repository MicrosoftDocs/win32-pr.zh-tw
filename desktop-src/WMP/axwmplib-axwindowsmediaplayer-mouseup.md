---
title: AxWindowsMediaPlayer 物件的 MouseUp 事件
description: 當使用者放開滑鼠按鍵時，就會發生 MouseUp 事件。 |AxWindowsMediaPlayer 物件的 MouseUp 事件
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- AxWindowsMediaPlayer 物件的 MouseUp 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001588"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f2b6a-105">AxWindowsMediaPlayer 物件的 MouseUp 事件</span><span class="sxs-lookup"><span data-stu-id="f2b6a-105">MouseUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f2b6a-106">當使用者放開滑鼠按鍵時，就會發生 MouseUp 事件。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-106">The MouseUp event occurs when the user releases a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a><span data-ttu-id="f2b6a-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="f2b6a-107">Event Data</span></span>

<span data-ttu-id="f2b6a-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MouseUpEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEventHandler**.</span></span> <span data-ttu-id="f2b6a-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MouseUpEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="f2b6a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f2b6a-110">Property</span></span>    | <span data-ttu-id="f2b6a-111">描述</span><span class="sxs-lookup"><span data-stu-id="f2b6a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b6a-112">nButton</span><span class="sxs-lookup"><span data-stu-id="f2b6a-112">nButton</span></span>     | <span data-ttu-id="f2b6a-113">Int16A 位的位，其中位對應至左按鈕 (位 0) ，右鍵 (位 1) ，中間按鈕 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="f2b6a-114">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="f2b6a-115">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="f2b6a-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="f2b6a-116">nShiftState</span></span> | <span data-ttu-id="f2b6a-117">Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="f2b6a-118">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="f2b6a-119">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="f2b6a-120">外匯</span><span class="sxs-lookup"><span data-stu-id="f2b6a-120">fX</span></span>          | <span data-ttu-id="f2b6a-121">滑鼠指標相對於控制項左上角的 Int32The X 軸座標。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="f2b6a-122">財年</span><span class="sxs-lookup"><span data-stu-id="f2b6a-122">fY</span></span>          | <span data-ttu-id="f2b6a-123">滑鼠指標的 Int32The y 座標，相對於控制項的左上角。</span><span class="sxs-lookup"><span data-stu-id="f2b6a-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="f2b6a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2b6a-124">Requirements</span></span>



| <span data-ttu-id="f2b6a-125">需求</span><span class="sxs-lookup"><span data-stu-id="f2b6a-125">Requirement</span></span> | <span data-ttu-id="f2b6a-126">值</span><span class="sxs-lookup"><span data-stu-id="f2b6a-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b6a-127">版本</span><span class="sxs-lookup"><span data-stu-id="f2b6a-127">Version</span></span><br/>   | <span data-ttu-id="f2b6a-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f2b6a-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f2b6a-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="f2b6a-129">Namespace</span></span><br/> | <span data-ttu-id="f2b6a-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f2b6a-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f2b6a-131">組件</span><span class="sxs-lookup"><span data-stu-id="f2b6a-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f2b6a-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="f2b6a-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b6a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2b6a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b6a-134">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f2b6a-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





