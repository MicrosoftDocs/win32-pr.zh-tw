---
title: AxWindowsMediaPlayer 物件的 CdromRipStateChange 事件
description: 當 CD 翻錄操作變更狀態時，就會發生 CdromRipStateChange 事件。
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- AxWindowsMediaPlayer 物件的 CdromRipStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974905"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d73d3-104">AxWindowsMediaPlayer 物件的 CdromRipStateChange 事件</span><span class="sxs-lookup"><span data-stu-id="d73d3-104">CdromRipStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d73d3-105">當 CD 翻錄操作變更狀態時，就會發生 CdromRipStateChange 事件。</span><span class="sxs-lookup"><span data-stu-id="d73d3-105">The CdromRipStateChange event occurs when a CD ripping operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a><span data-ttu-id="d73d3-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="d73d3-106">Event Data</span></span>

<span data-ttu-id="d73d3-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromRipStateChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="d73d3-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEventHandler**.</span></span> <span data-ttu-id="d73d3-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromRipStateChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="d73d3-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="d73d3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d73d3-109">Property</span></span>  | <span data-ttu-id="d73d3-110">描述</span><span class="sxs-lookup"><span data-stu-id="d73d3-110">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d73d3-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="d73d3-111">pCdromRip</span></span> | <span data-ttu-id="d73d3-112">代表引發錯誤之翻錄作業的 WMPLib IWMPCdromRipThe 介面。</span><span class="sxs-lookup"><span data-stu-id="d73d3-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/> |
| <span data-ttu-id="d73d3-113">wmprs</span><span class="sxs-lookup"><span data-stu-id="d73d3-113">wmprs</span></span>     | <span data-ttu-id="d73d3-114">WMPLib，表示新狀態的 WMPRipStateThe 列舉值。</span><span class="sxs-lookup"><span data-stu-id="d73d3-114">WMPLib.WMPRipStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="d73d3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d73d3-115">Requirements</span></span>



| <span data-ttu-id="d73d3-116">需求</span><span class="sxs-lookup"><span data-stu-id="d73d3-116">Requirement</span></span> | <span data-ttu-id="d73d3-117">值</span><span class="sxs-lookup"><span data-stu-id="d73d3-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d73d3-118">版本</span><span class="sxs-lookup"><span data-stu-id="d73d3-118">Version</span></span><br/>   | <span data-ttu-id="d73d3-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="d73d3-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="d73d3-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="d73d3-120">Namespace</span></span><br/> | <span data-ttu-id="d73d3-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d73d3-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d73d3-122">組件</span><span class="sxs-lookup"><span data-stu-id="d73d3-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d73d3-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d73d3-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d73d3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d73d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73d3-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d73d3-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d73d3-126">**IWMPCdromRip 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d73d3-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d73d3-127">**WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="d73d3-127">**WMPRipState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





