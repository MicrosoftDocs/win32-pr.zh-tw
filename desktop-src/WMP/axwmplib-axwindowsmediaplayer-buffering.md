---
title: AxWindowsMediaPlayer 物件的緩衝事件
description: 當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生緩衝事件。 |AxWindowsMediaPlayer 物件的緩衝事件
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- AxWindowsMediaPlayer 物件的緩衝事件 Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986141"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="96cef-105">AxWindowsMediaPlayer 物件的緩衝事件</span><span class="sxs-lookup"><span data-stu-id="96cef-105">Buffering Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="96cef-106">當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生緩衝事件。</span><span class="sxs-lookup"><span data-stu-id="96cef-106">The Buffering event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a><span data-ttu-id="96cef-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="96cef-107">Event Data</span></span>

<span data-ttu-id="96cef-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ BufferingEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="96cef-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_BufferingEventHandler**.</span></span> <span data-ttu-id="96cef-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ BufferingEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="96cef-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_BufferingEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="96cef-110">屬性</span><span class="sxs-lookup"><span data-stu-id="96cef-110">Property</span></span> | <span data-ttu-id="96cef-111">描述</span><span class="sxs-lookup"><span data-stu-id="96cef-111">Description</span></span>                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96cef-112">Start</span><span class="sxs-lookup"><span data-stu-id="96cef-112">Start</span></span>    | <span data-ttu-id="96cef-113">BooleanSpecifies，表示緩衝是否已開始或結束。</span><span class="sxs-lookup"><span data-stu-id="96cef-113">System.BooleanSpecifies whether buffering has begun or ended.</span></span> <span data-ttu-id="96cef-114">True 值表示它已開始;值為 false 表示它已結束。</span><span class="sxs-lookup"><span data-stu-id="96cef-114">A value of true indicates that it has begun; a value of false indicates that it has ended.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96cef-115">備註</span><span class="sxs-lookup"><span data-stu-id="96cef-115">Remarks</span></span>

<span data-ttu-id="96cef-116">您可以使用此事件來判斷何時啟動或停止緩衝或下載。</span><span class="sxs-lookup"><span data-stu-id="96cef-116">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="96cef-117">您可以針對這兩種案例和測試 *IWMPNetwork* 使用相同的事件區塊。**bufferingProgress** 和 *IWMPNetwork*。**downloadProgress** ，以判斷 Windows Media Player 目前是否正在緩衝或正在下載內容。</span><span class="sxs-lookup"><span data-stu-id="96cef-117">You can use the same event block for both cases and test *IWMPNetwork*.**bufferingProgress** and *IWMPNetwork*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

## <a name="requirements"></a><span data-ttu-id="96cef-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="96cef-118">Requirements</span></span>



| <span data-ttu-id="96cef-119">需求</span><span class="sxs-lookup"><span data-stu-id="96cef-119">Requirement</span></span> | <span data-ttu-id="96cef-120">值</span><span class="sxs-lookup"><span data-stu-id="96cef-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96cef-121">版本</span><span class="sxs-lookup"><span data-stu-id="96cef-121">Version</span></span><br/>   | <span data-ttu-id="96cef-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="96cef-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="96cef-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="96cef-123">Namespace</span></span><br/> | <span data-ttu-id="96cef-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="96cef-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="96cef-125">組件</span><span class="sxs-lookup"><span data-stu-id="96cef-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="96cef-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="96cef-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96cef-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96cef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96cef-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="96cef-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="96cef-129">**IWMPNetwork. bufferingProgress (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="96cef-129">**IWMPNetwork.bufferingProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="96cef-130">**IWMPNetwork. downloadProgress (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="96cef-130">**IWMPNetwork.downloadProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





