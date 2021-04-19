---
title: AxWindowsMediaPlayer 物件的 OpenStateChange 事件
description: 當 openState 屬性變更值時，就會發生 OpenStateChange 事件。 |AxWindowsMediaPlayer 物件的 OpenStateChange 事件
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- AxWindowsMediaPlayer 物件的 OpenStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991529"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9c04d-105">AxWindowsMediaPlayer 物件的 OpenStateChange 事件</span><span class="sxs-lookup"><span data-stu-id="9c04d-105">OpenStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9c04d-106">當 **openState** 屬性變更值時，就會發生 OpenStateChange 事件。</span><span class="sxs-lookup"><span data-stu-id="9c04d-106">The OpenStateChange event occurs when the **openState** property changes value.</span></span>

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a><span data-ttu-id="9c04d-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="9c04d-107">Event Data</span></span>

<span data-ttu-id="9c04d-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ OpenStateChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="9c04d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEventHandler**.</span></span> <span data-ttu-id="9c04d-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ OpenStateChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="9c04d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="9c04d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9c04d-110">Property</span></span> | <span data-ttu-id="9c04d-111">描述</span><span class="sxs-lookup"><span data-stu-id="9c04d-111">Description</span></span>                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c04d-112">NewState</span><span class="sxs-lookup"><span data-stu-id="9c04d-112">NewState</span></span> | <span data-ttu-id="9c04d-113">Int32Specifies 新的開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="9c04d-113">System.Int32Specifies the new open state.</span></span> <span data-ttu-id="9c04d-114">如需值的表格，請參閱 [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)。</span><span class="sxs-lookup"><span data-stu-id="9c04d-114">For a table of values, see [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c04d-115">備註</span><span class="sxs-lookup"><span data-stu-id="9c04d-115">Remarks</span></span>

<span data-ttu-id="9c04d-116">Windows Media Player 可以在嘗試開啟網路檔案（例如找出伺服器、連線到伺服器，最後開啟檔案）時，經歷數個開啟的狀態。</span><span class="sxs-lookup"><span data-stu-id="9c04d-116">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="9c04d-117">每次開啟狀態變更時，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="9c04d-117">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="9c04d-118">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="9c04d-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="9c04d-119">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="9c04d-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="9c04d-120">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="9c04d-120">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c04d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c04d-121">Requirements</span></span>



| <span data-ttu-id="9c04d-122">需求</span><span class="sxs-lookup"><span data-stu-id="9c04d-122">Requirement</span></span> | <span data-ttu-id="9c04d-123">值</span><span class="sxs-lookup"><span data-stu-id="9c04d-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c04d-124">版本</span><span class="sxs-lookup"><span data-stu-id="9c04d-124">Version</span></span><br/>   | <span data-ttu-id="9c04d-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="9c04d-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9c04d-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="9c04d-126">Namespace</span></span><br/> | <span data-ttu-id="9c04d-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9c04d-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9c04d-128">組件</span><span class="sxs-lookup"><span data-stu-id="9c04d-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9c04d-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="9c04d-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c04d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c04d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c04d-131">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="9c04d-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9c04d-132">**AxWindowsMediaPlayer. openState (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="9c04d-132">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





