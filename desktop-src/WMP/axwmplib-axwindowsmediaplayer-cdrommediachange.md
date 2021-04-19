---
title: AxWindowsMediaPlayer 物件的 CdromMediaChange 事件
description: 從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 CdromMediaChange 事件。 |AxWindowsMediaPlayer 物件的 CdromMediaChange 事件
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- AxWindowsMediaPlayer 物件的 CdromMediaChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992138"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d625b-105">AxWindowsMediaPlayer 物件的 CdromMediaChange 事件</span><span class="sxs-lookup"><span data-stu-id="d625b-105">CdromMediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d625b-106">從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 **CdromMediaChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="d625b-106">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a><span data-ttu-id="d625b-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="d625b-107">Event Data</span></span>

<span data-ttu-id="d625b-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromMediaChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="d625b-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEventHandler**.</span></span> <span data-ttu-id="d625b-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromMediaChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="d625b-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d625b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d625b-110">Property</span></span> | <span data-ttu-id="d625b-111">描述</span><span class="sxs-lookup"><span data-stu-id="d625b-111">Description</span></span>                                                        |
|----------|--------------------------------------------------------------------|
| <span data-ttu-id="d625b-112">CdromNum</span><span class="sxs-lookup"><span data-stu-id="d625b-112">CdromNum</span></span> | <span data-ttu-id="d625b-113">Int32Specifies CD 或 DVD 光碟機的索引。</span><span class="sxs-lookup"><span data-stu-id="d625b-113">System.Int32Specifies the index of the CD or DVD drive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d625b-114">備註</span><span class="sxs-lookup"><span data-stu-id="d625b-114">Remarks</span></span>

<span data-ttu-id="d625b-115">CD 光碟機的索引會對應到可透過 IWMPCdromCollection 介面存取之 IWMPCdrom 介面的索引。</span><span class="sxs-lookup"><span data-stu-id="d625b-115">The index of the CD drive corresponds to the index of an IWMPCdrom interface accessible through the IWMPCdromCollection interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d625b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d625b-116">Requirements</span></span>



| <span data-ttu-id="d625b-117">需求</span><span class="sxs-lookup"><span data-stu-id="d625b-117">Requirement</span></span> | <span data-ttu-id="d625b-118">值</span><span class="sxs-lookup"><span data-stu-id="d625b-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d625b-119">版本</span><span class="sxs-lookup"><span data-stu-id="d625b-119">Version</span></span><br/>   | <span data-ttu-id="d625b-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d625b-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d625b-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="d625b-121">Namespace</span></span><br/> | <span data-ttu-id="d625b-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d625b-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d625b-123">組件</span><span class="sxs-lookup"><span data-stu-id="d625b-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d625b-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d625b-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d625b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d625b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d625b-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d625b-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d625b-127">**IWMPCdrom 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d625b-127">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d625b-128">**IWMPCdromCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d625b-128">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





