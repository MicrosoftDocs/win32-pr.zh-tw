---
title: AxWindowsMediaPlayer 物件的 CdromRipMediaError 事件
description: 從 CD 翻錄個別播放軌時發生錯誤，就會發生 CdromRipMediaError 事件。
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- AxWindowsMediaPlayer 物件的 CdromRipMediaError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981088"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="182bf-104">AxWindowsMediaPlayer 物件的 CdromRipMediaError 事件</span><span class="sxs-lookup"><span data-stu-id="182bf-104">CdromRipMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="182bf-105">從 CD 翻錄個別播放軌時發生錯誤，就會發生 CdromRipMediaError 事件。</span><span class="sxs-lookup"><span data-stu-id="182bf-105">The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.</span></span>

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a><span data-ttu-id="182bf-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="182bf-106">Event Data</span></span>

<span data-ttu-id="182bf-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromRipMediaErrorEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="182bf-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEventHandler**.</span></span> <span data-ttu-id="182bf-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromRipMediaErrorEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="182bf-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="182bf-109">屬性</span><span class="sxs-lookup"><span data-stu-id="182bf-109">Property</span></span>  | <span data-ttu-id="182bf-110">描述</span><span class="sxs-lookup"><span data-stu-id="182bf-110">Description</span></span>                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="182bf-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="182bf-111">pCdromRip</span></span> | <span data-ttu-id="182bf-112">代表引發錯誤之翻錄作業的 WMPLib IWMPCdromRipThe 介面。</span><span class="sxs-lookup"><span data-stu-id="182bf-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/>                |
| <span data-ttu-id="182bf-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="182bf-113">pMedia</span></span>    | <span data-ttu-id="182bf-114">引發錯誤的 ObjectThe 媒體專案。</span><span class="sxs-lookup"><span data-stu-id="182bf-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="182bf-115">您可以將此轉換成 IWMPMedia 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="182bf-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="182bf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="182bf-116">Requirements</span></span>



| <span data-ttu-id="182bf-117">需求</span><span class="sxs-lookup"><span data-stu-id="182bf-117">Requirement</span></span> | <span data-ttu-id="182bf-118">值</span><span class="sxs-lookup"><span data-stu-id="182bf-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="182bf-119">版本</span><span class="sxs-lookup"><span data-stu-id="182bf-119">Version</span></span><br/>   | <span data-ttu-id="182bf-120">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="182bf-120">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="182bf-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="182bf-121">Namespace</span></span><br/> | <span data-ttu-id="182bf-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="182bf-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="182bf-123">組件</span><span class="sxs-lookup"><span data-stu-id="182bf-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="182bf-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="182bf-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="182bf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="182bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182bf-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="182bf-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="182bf-127">**IWMPCdromRip 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="182bf-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="182bf-128">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="182bf-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





