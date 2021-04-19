---
title: AxWindowsMediaPlayer 物件的 EndOfStream 事件
description: EndOfStream 事件已保留供日後使用。
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- AxWindowsMediaPlayer 物件的 EndOfStream 事件 Windows Media Player
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993953"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e9cd5-104">AxWindowsMediaPlayer 物件的 EndOfStream 事件</span><span class="sxs-lookup"><span data-stu-id="e9cd5-104">EndOfStream Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e9cd5-105">EndOfStream 事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="e9cd5-105">The EndOfStream event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a><span data-ttu-id="e9cd5-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="e9cd5-106">Event Data</span></span>

<span data-ttu-id="e9cd5-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ EndOfStreamEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="e9cd5-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEventHandler**.</span></span> <span data-ttu-id="e9cd5-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ EndOfStreamEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="e9cd5-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="e9cd5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e9cd5-109">Property</span></span> | <span data-ttu-id="e9cd5-110">描述</span><span class="sxs-lookup"><span data-stu-id="e9cd5-110">Description</span></span>                           |
|----------|---------------------------------------|
| <span data-ttu-id="e9cd5-111">result</span><span class="sxs-lookup"><span data-stu-id="e9cd5-111">result</span></span>   | <span data-ttu-id="e9cd5-112">支援 Int32Not。</span><span class="sxs-lookup"><span data-stu-id="e9cd5-112">System.Int32Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9cd5-113">備註</span><span class="sxs-lookup"><span data-stu-id="e9cd5-113">Remarks</span></span>

<span data-ttu-id="e9cd5-114">此事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="e9cd5-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9cd5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9cd5-115">Requirements</span></span>



| <span data-ttu-id="e9cd5-116">需求</span><span class="sxs-lookup"><span data-stu-id="e9cd5-116">Requirement</span></span> | <span data-ttu-id="e9cd5-117">值</span><span class="sxs-lookup"><span data-stu-id="e9cd5-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cd5-118">版本</span><span class="sxs-lookup"><span data-stu-id="e9cd5-118">Version</span></span><br/>   | <span data-ttu-id="e9cd5-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e9cd5-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e9cd5-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9cd5-120">Namespace</span></span><br/> | <span data-ttu-id="e9cd5-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e9cd5-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e9cd5-122">組件</span><span class="sxs-lookup"><span data-stu-id="e9cd5-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e9cd5-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="e9cd5-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9cd5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9cd5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cd5-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e9cd5-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





