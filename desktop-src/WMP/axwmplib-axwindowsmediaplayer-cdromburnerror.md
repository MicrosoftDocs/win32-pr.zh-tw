---
title: AxWindowsMediaPlayer 物件的 CdromBurnError 事件
description: 在 CD 燒錄操作期間發生一般錯誤時，就會發生 CdromBurnError 事件。
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- AxWindowsMediaPlayer 物件的 CdromBurnError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986560"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="69ee1-104">AxWindowsMediaPlayer 物件的 CdromBurnError 事件</span><span class="sxs-lookup"><span data-stu-id="69ee1-104">CdromBurnError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="69ee1-105">在 CD 燒錄操作期間發生一般錯誤時，就會發生 CdromBurnError 事件。</span><span class="sxs-lookup"><span data-stu-id="69ee1-105">The CdromBurnError event occurs when a generic error happens during a CD burning operation.</span></span>

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a><span data-ttu-id="69ee1-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="69ee1-106">Event Data</span></span>

<span data-ttu-id="69ee1-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromBurnErrorEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="69ee1-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEventHandler**.</span></span> <span data-ttu-id="69ee1-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromBurnErrorEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="69ee1-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="69ee1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="69ee1-109">Property</span></span>   | <span data-ttu-id="69ee1-110">描述</span><span class="sxs-lookup"><span data-stu-id="69ee1-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ee1-111">hrError</span><span class="sxs-lookup"><span data-stu-id="69ee1-111">hrError</span></span>    | <span data-ttu-id="69ee1-112">**System.object** 引發事件的錯誤。</span><span class="sxs-lookup"><span data-stu-id="69ee1-112">**System.Int32** The error that raised the event.</span></span><br/>                                               |
| <span data-ttu-id="69ee1-113">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="69ee1-113">pCdromBurn</span></span> | <span data-ttu-id="69ee1-114">代表引發錯誤之燒錄作業的 WMPLib IWMPCdromBurnThe 介面。</span><span class="sxs-lookup"><span data-stu-id="69ee1-114">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69ee1-115">備註</span><span class="sxs-lookup"><span data-stu-id="69ee1-115">Remarks</span></span>

<span data-ttu-id="69ee1-116">若要捕獲媒體特定的錯誤，請處理 AxWMPLib。 \_WMPOCXEvents \_ CdromBurnMediaError 事件。</span><span class="sxs-lookup"><span data-stu-id="69ee1-116">To capture media specific errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ee1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="69ee1-117">Requirements</span></span>



| <span data-ttu-id="69ee1-118">需求</span><span class="sxs-lookup"><span data-stu-id="69ee1-118">Requirement</span></span> | <span data-ttu-id="69ee1-119">值</span><span class="sxs-lookup"><span data-stu-id="69ee1-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ee1-120">版本</span><span class="sxs-lookup"><span data-stu-id="69ee1-120">Version</span></span><br/>   | <span data-ttu-id="69ee1-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="69ee1-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="69ee1-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="69ee1-122">Namespace</span></span><br/> | <span data-ttu-id="69ee1-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="69ee1-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="69ee1-124">組件</span><span class="sxs-lookup"><span data-stu-id="69ee1-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69ee1-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="69ee1-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ee1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69ee1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ee1-127">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69ee1-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69ee1-128">**AxWindowsMediaPlayer CdromBurnMediaError 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69ee1-128">**AxWindowsMediaPlayer.CdromBurnMediaError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[<span data-ttu-id="69ee1-129">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69ee1-129">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





