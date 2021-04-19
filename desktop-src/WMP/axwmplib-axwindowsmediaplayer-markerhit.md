---
title: AxWindowsMediaPlayer 物件的 MarkerHit 事件
description: 當到達標記時，就會發生 MarkerHit 事件。 |AxWindowsMediaPlayer 物件的 MarkerHit 事件
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- AxWindowsMediaPlayer 物件的 MarkerHit 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996450"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="16725-105">AxWindowsMediaPlayer 物件的 MarkerHit 事件</span><span class="sxs-lookup"><span data-stu-id="16725-105">MarkerHit Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="16725-106">當到達標記時，就會發生 MarkerHit 事件。</span><span class="sxs-lookup"><span data-stu-id="16725-106">The MarkerHit event occurs when a marker is reached.</span></span>

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a><span data-ttu-id="16725-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="16725-107">Event Data</span></span>

<span data-ttu-id="16725-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MarkerHitEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="16725-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEventHandler**.</span></span> <span data-ttu-id="16725-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MarkerHitEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="16725-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="16725-110">屬性</span><span class="sxs-lookup"><span data-stu-id="16725-110">Property</span></span>      | <span data-ttu-id="16725-111">描述</span><span class="sxs-lookup"><span data-stu-id="16725-111">Description</span></span>                                                             |
|---------------|-------------------------------------------------------------------------|
| <span data-ttu-id="16725-112">**MarkerNum**</span><span class="sxs-lookup"><span data-stu-id="16725-112">**MarkerNum**</span></span> | <span data-ttu-id="16725-113">Int32Indicates 已點擊的標記數目。</span><span class="sxs-lookup"><span data-stu-id="16725-113">System.Int32Indicates the number of the marker that was hit.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16725-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="16725-114">Requirements</span></span>



| <span data-ttu-id="16725-115">需求</span><span class="sxs-lookup"><span data-stu-id="16725-115">Requirement</span></span> | <span data-ttu-id="16725-116">值</span><span class="sxs-lookup"><span data-stu-id="16725-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16725-117">版本</span><span class="sxs-lookup"><span data-stu-id="16725-117">Version</span></span><br/>   | <span data-ttu-id="16725-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="16725-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="16725-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="16725-119">Namespace</span></span><br/> | <span data-ttu-id="16725-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="16725-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="16725-121">組件</span><span class="sxs-lookup"><span data-stu-id="16725-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="16725-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="16725-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16725-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16725-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16725-124">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="16725-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





