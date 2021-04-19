---
title: AxWindowsMediaPlayer 物件的 KeyUp 事件
description: 當釋放索引鍵時，就會發生 KeyUp 事件。 |AxWindowsMediaPlayer 物件的 KeyUp 事件
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- AxWindowsMediaPlayer 物件的 KeyUp 事件 Windows Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984133"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="71b93-105">AxWindowsMediaPlayer 物件的 KeyUp 事件</span><span class="sxs-lookup"><span data-stu-id="71b93-105">KeyUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="71b93-106">當釋放索引鍵時，就會發生 KeyUp 事件。</span><span class="sxs-lookup"><span data-stu-id="71b93-106">The KeyUp event occurs when a key is released.</span></span>

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a><span data-ttu-id="71b93-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="71b93-107">Event Data</span></span>

<span data-ttu-id="71b93-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ KeyUpEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="71b93-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEventHandler**.</span></span> <span data-ttu-id="71b93-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ KeyUpEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="71b93-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="71b93-110">屬性</span><span class="sxs-lookup"><span data-stu-id="71b93-110">Property</span></span>    | <span data-ttu-id="71b93-111">描述</span><span class="sxs-lookup"><span data-stu-id="71b93-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b93-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="71b93-112">nKeyCode</span></span>    | <span data-ttu-id="71b93-113">Int16Specifies 已按下的實體索引鍵。</span><span class="sxs-lookup"><span data-stu-id="71b93-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="71b93-114">如需可能的值，請參閱 KeyDown 事件的備註一節。</span><span class="sxs-lookup"><span data-stu-id="71b93-114">For possible values, see the Remarks section of the KeyDown event.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="71b93-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="71b93-115">nShiftState</span></span> | <span data-ttu-id="71b93-116">Int16A 位，具有與 SHIFT 鍵對應的最不重要位 (位 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) 。</span><span class="sxs-lookup"><span data-stu-id="71b93-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="71b93-117">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="71b93-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="71b93-118">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="71b93-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="71b93-119">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="71b93-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71b93-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="71b93-120">Requirements</span></span>



| <span data-ttu-id="71b93-121">需求</span><span class="sxs-lookup"><span data-stu-id="71b93-121">Requirement</span></span> | <span data-ttu-id="71b93-122">值</span><span class="sxs-lookup"><span data-stu-id="71b93-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b93-123">版本</span><span class="sxs-lookup"><span data-stu-id="71b93-123">Version</span></span><br/>   | <span data-ttu-id="71b93-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="71b93-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="71b93-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="71b93-125">Namespace</span></span><br/> | <span data-ttu-id="71b93-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="71b93-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="71b93-127">組件</span><span class="sxs-lookup"><span data-stu-id="71b93-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="71b93-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="71b93-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b93-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71b93-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b93-130">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="71b93-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





