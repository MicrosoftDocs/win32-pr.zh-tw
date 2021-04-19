---
title: AxWindowsMediaPlayer 物件的 ModeChange 事件
description: 當 Windows Media Player 的模式變更時，就會發生 ModeChange 事件。 |AxWindowsMediaPlayer 物件的 ModeChange 事件
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- AxWindowsMediaPlayer 物件的 ModeChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983105"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="aa9a3-105">AxWindowsMediaPlayer 物件的 ModeChange 事件</span><span class="sxs-lookup"><span data-stu-id="aa9a3-105">ModeChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="aa9a3-106">當 Windows Media Player 的模式變更時，就會發生 ModeChange 事件。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-106">The ModeChange event occurs when a mode of Windows Media Player is changed.</span></span>

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a><span data-ttu-id="aa9a3-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="aa9a3-107">Event Data</span></span>

<span data-ttu-id="aa9a3-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ ModeChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEventHandler**.</span></span> <span data-ttu-id="aa9a3-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ ModeChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="aa9a3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="aa9a3-110">Property</span></span> | <span data-ttu-id="aa9a3-111">描述</span><span class="sxs-lookup"><span data-stu-id="aa9a3-111">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9a3-112">modeName</span><span class="sxs-lookup"><span data-stu-id="aa9a3-112">modeName</span></span> | <span data-ttu-id="aa9a3-113">StringIndicates 已變更的模式。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-113">System.StringIndicates the mode that was changed.</span></span> <span data-ttu-id="aa9a3-114">如需可能的值，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-114">For possible values, see Remarks.</span></span><br/> |
| <span data-ttu-id="aa9a3-115">newValue</span><span class="sxs-lookup"><span data-stu-id="aa9a3-115">newValue</span></span> | <span data-ttu-id="aa9a3-116">BooleanIndicates 指定模式的新狀態。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-116">System.BooleanIndicates the new state of the specified mode.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="aa9a3-117">備註</span><span class="sxs-lookup"><span data-stu-id="aa9a3-117">Remarks</span></span>

<span data-ttu-id="aa9a3-118">下表顯示 modeName 屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-118">The following table shows the possible values for the modeName property.</span></span>



| <span data-ttu-id="aa9a3-119">String</span><span class="sxs-lookup"><span data-stu-id="aa9a3-119">String</span></span>  | <span data-ttu-id="aa9a3-120">Description</span><span class="sxs-lookup"><span data-stu-id="aa9a3-120">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="aa9a3-121">隨機播放</span><span class="sxs-lookup"><span data-stu-id="aa9a3-121">shuffle</span></span> | <span data-ttu-id="aa9a3-122">曲目會以隨機順序播放。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-122">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="aa9a3-123">loop</span><span class="sxs-lookup"><span data-stu-id="aa9a3-123">loop</span></span>    | <span data-ttu-id="aa9a3-124">整個播放曲目順序都會重複播放。</span><span class="sxs-lookup"><span data-stu-id="aa9a3-124">The entire sequence of tracks is played repeatedly.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="aa9a3-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa9a3-125">Requirements</span></span>



| <span data-ttu-id="aa9a3-126">需求</span><span class="sxs-lookup"><span data-stu-id="aa9a3-126">Requirement</span></span> | <span data-ttu-id="aa9a3-127">值</span><span class="sxs-lookup"><span data-stu-id="aa9a3-127">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9a3-128">版本</span><span class="sxs-lookup"><span data-stu-id="aa9a3-128">Version</span></span><br/>   | <span data-ttu-id="aa9a3-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="aa9a3-129">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="aa9a3-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="aa9a3-130">Namespace</span></span><br/> | <span data-ttu-id="aa9a3-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="aa9a3-131">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="aa9a3-132">組件</span><span class="sxs-lookup"><span data-stu-id="aa9a3-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="aa9a3-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="aa9a3-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9a3-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa9a3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9a3-135">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="aa9a3-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aa9a3-136">**IWMPSettings. getMode (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="aa9a3-136">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aa9a3-137">**IWMPSettings. setMode (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="aa9a3-137">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





