---
title: AxWindowsMediaPlayer 物件的 CdromBurnMediaError 事件
description: 將個別媒體專案燒錄至 CD 時，發生錯誤時，就會發生 CdromBurnMediaError 事件。
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- AxWindowsMediaPlayer 物件的 CdromBurnMediaError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986779"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8a591-104">AxWindowsMediaPlayer 物件的 CdromBurnMediaError 事件</span><span class="sxs-lookup"><span data-stu-id="8a591-104">CdromBurnMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8a591-105">將個別媒體專案燒錄至 CD 時，發生錯誤時，就會發生 CdromBurnMediaError 事件。</span><span class="sxs-lookup"><span data-stu-id="8a591-105">The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.</span></span>

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a><span data-ttu-id="8a591-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="8a591-106">Event Data</span></span>

<span data-ttu-id="8a591-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="8a591-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEventHandler**.</span></span> <span data-ttu-id="8a591-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromBurnMediaErrorEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8a591-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="8a591-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8a591-109">Property</span></span>   | <span data-ttu-id="8a591-110">描述</span><span class="sxs-lookup"><span data-stu-id="8a591-110">Description</span></span>                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a591-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="8a591-111">pCdromBurn</span></span> | <span data-ttu-id="8a591-112">代表引發錯誤之燒錄作業的 WMPLib IWMPCdromBurnThe 介面。</span><span class="sxs-lookup"><span data-stu-id="8a591-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/>               |
| <span data-ttu-id="8a591-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="8a591-113">pMedia</span></span>     | <span data-ttu-id="8a591-114">引發錯誤的 ObjectThe 媒體專案。</span><span class="sxs-lookup"><span data-stu-id="8a591-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="8a591-115">您可以將此轉換成 IWMPMedia 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="8a591-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a591-116">備註</span><span class="sxs-lookup"><span data-stu-id="8a591-116">Remarks</span></span>

<span data-ttu-id="8a591-117">若要捕獲一般錯誤，請處理 AxWMPLib。 \_WMPOCXEvents \_ CdromBurnError 事件。</span><span class="sxs-lookup"><span data-stu-id="8a591-117">To capture generic errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a591-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a591-118">Requirements</span></span>



| <span data-ttu-id="8a591-119">需求</span><span class="sxs-lookup"><span data-stu-id="8a591-119">Requirement</span></span> | <span data-ttu-id="8a591-120">值</span><span class="sxs-lookup"><span data-stu-id="8a591-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a591-121">版本</span><span class="sxs-lookup"><span data-stu-id="8a591-121">Version</span></span><br/>   | <span data-ttu-id="8a591-122">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="8a591-122">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="8a591-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="8a591-123">Namespace</span></span><br/> | <span data-ttu-id="8a591-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8a591-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8a591-125">組件</span><span class="sxs-lookup"><span data-stu-id="8a591-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a591-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="8a591-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a591-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a591-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a591-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8a591-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a591-129">**AxWindowsMediaPlayer CdromBurnError 事件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8a591-129">**AxWindowsMediaPlayer.CdromBurnError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[<span data-ttu-id="8a591-130">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8a591-130">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a591-131">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8a591-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





