---
title: AxWindowsMediaPlayer 物件的 DurationUnitChange 事件
description: DurationUnitChange 事件已保留供日後使用。
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- AxWindowsMediaPlayer 物件的 DurationUnitChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982072"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="02b84-104">AxWindowsMediaPlayer 物件的 DurationUnitChange 事件</span><span class="sxs-lookup"><span data-stu-id="02b84-104">DurationUnitChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="02b84-105">DurationUnitChange 事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="02b84-105">The DurationUnitChange event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a><span data-ttu-id="02b84-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="02b84-106">Event Data</span></span>

<span data-ttu-id="02b84-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ DurationUnitChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="02b84-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEventHandler**.</span></span> <span data-ttu-id="02b84-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ DurationUnitChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="02b84-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="02b84-109">屬性</span><span class="sxs-lookup"><span data-stu-id="02b84-109">Property</span></span>        | <span data-ttu-id="02b84-110">描述</span><span class="sxs-lookup"><span data-stu-id="02b84-110">Description</span></span>                               |
|-----------------|-------------------------------------------|
| <span data-ttu-id="02b84-111">newDurationUnit</span><span class="sxs-lookup"><span data-stu-id="02b84-111">newDurationUnit</span></span> | <span data-ttu-id="02b84-112">**System.object** 不支援。</span><span class="sxs-lookup"><span data-stu-id="02b84-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02b84-113">備註</span><span class="sxs-lookup"><span data-stu-id="02b84-113">Remarks</span></span>

<span data-ttu-id="02b84-114">此事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="02b84-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b84-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="02b84-115">Requirements</span></span>



| <span data-ttu-id="02b84-116">需求</span><span class="sxs-lookup"><span data-stu-id="02b84-116">Requirement</span></span> | <span data-ttu-id="02b84-117">值</span><span class="sxs-lookup"><span data-stu-id="02b84-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b84-118">版本</span><span class="sxs-lookup"><span data-stu-id="02b84-118">Version</span></span><br/>   | <span data-ttu-id="02b84-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="02b84-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="02b84-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="02b84-120">Namespace</span></span><br/> | <span data-ttu-id="02b84-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="02b84-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="02b84-122">組件</span><span class="sxs-lookup"><span data-stu-id="02b84-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="02b84-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="02b84-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b84-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02b84-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b84-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="02b84-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





