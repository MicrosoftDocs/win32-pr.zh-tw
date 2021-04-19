---
title: AxWindowsMediaPlayer 物件的 CdromBurnStateChange 事件
description: 當 CD 燒錄操作變更狀態時，就會發生 CdromBurnStateChange 事件。
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- AxWindowsMediaPlayer 物件的 CdromBurnStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976757"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="957c1-104">AxWindowsMediaPlayer 物件的 CdromBurnStateChange 事件</span><span class="sxs-lookup"><span data-stu-id="957c1-104">CdromBurnStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="957c1-105">當 CD 燒錄操作變更狀態時，就會發生 CdromBurnStateChange 事件。</span><span class="sxs-lookup"><span data-stu-id="957c1-105">The CdromBurnStateChange event occurs when a CD burning operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a><span data-ttu-id="957c1-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="957c1-106">Event Data</span></span>

<span data-ttu-id="957c1-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromBurnStateChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="957c1-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEventHandler**.</span></span> <span data-ttu-id="957c1-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromBurnStateChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="957c1-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="957c1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="957c1-109">Property</span></span>   | <span data-ttu-id="957c1-110">描述</span><span class="sxs-lookup"><span data-stu-id="957c1-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="957c1-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="957c1-111">pCdromBurn</span></span> | <span data-ttu-id="957c1-112">代表引發錯誤之燒錄作業的 WMPLib IWMPCdromBurnThe 介面。</span><span class="sxs-lookup"><span data-stu-id="957c1-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |
| <span data-ttu-id="957c1-113">wmpbs</span><span class="sxs-lookup"><span data-stu-id="957c1-113">wmpbs</span></span>      | <span data-ttu-id="957c1-114">WMPLib，表示新狀態的 WMPBurnStateThe 列舉值。</span><span class="sxs-lookup"><span data-stu-id="957c1-114">WMPLib.WMPBurnStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="957c1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="957c1-115">Requirements</span></span>



| <span data-ttu-id="957c1-116">需求</span><span class="sxs-lookup"><span data-stu-id="957c1-116">Requirement</span></span> | <span data-ttu-id="957c1-117">值</span><span class="sxs-lookup"><span data-stu-id="957c1-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="957c1-118">版本</span><span class="sxs-lookup"><span data-stu-id="957c1-118">Version</span></span><br/>   | <span data-ttu-id="957c1-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="957c1-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="957c1-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="957c1-120">Namespace</span></span><br/> | <span data-ttu-id="957c1-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="957c1-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="957c1-122">組件</span><span class="sxs-lookup"><span data-stu-id="957c1-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="957c1-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="957c1-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="957c1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="957c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957c1-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="957c1-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="957c1-126">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="957c1-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="957c1-127">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="957c1-127">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





