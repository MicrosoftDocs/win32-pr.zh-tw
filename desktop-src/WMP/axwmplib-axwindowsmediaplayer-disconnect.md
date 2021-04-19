---
title: AxWindowsMediaPlayer 物件的中斷線上活動
description: 中斷線上活動是保留供日後使用。
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- AxWindowsMediaPlayer 物件的中斷線上活動 Windows Media Player
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001504"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="db228-104">AxWindowsMediaPlayer 物件的中斷線上活動</span><span class="sxs-lookup"><span data-stu-id="db228-104">Disconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="db228-105">中斷線上活動是保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="db228-105">The Disconnect event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a><span data-ttu-id="db228-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="db228-106">Event Data</span></span>

<span data-ttu-id="db228-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ DisconnectEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="db228-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEventHandler**.</span></span> <span data-ttu-id="db228-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ DisconnectEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="db228-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="db228-109">屬性</span><span class="sxs-lookup"><span data-stu-id="db228-109">Property</span></span> | <span data-ttu-id="db228-110">描述</span><span class="sxs-lookup"><span data-stu-id="db228-110">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="db228-111">result</span><span class="sxs-lookup"><span data-stu-id="db228-111">result</span></span>   | <span data-ttu-id="db228-112">**System.object** 不支援。</span><span class="sxs-lookup"><span data-stu-id="db228-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db228-113">備註</span><span class="sxs-lookup"><span data-stu-id="db228-113">Remarks</span></span>

<span data-ttu-id="db228-114">此事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="db228-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="db228-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="db228-115">Requirements</span></span>



| <span data-ttu-id="db228-116">需求</span><span class="sxs-lookup"><span data-stu-id="db228-116">Requirement</span></span> | <span data-ttu-id="db228-117">值</span><span class="sxs-lookup"><span data-stu-id="db228-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db228-118">版本</span><span class="sxs-lookup"><span data-stu-id="db228-118">Version</span></span><br/>   | <span data-ttu-id="db228-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="db228-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="db228-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="db228-120">Namespace</span></span><br/> | <span data-ttu-id="db228-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="db228-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="db228-122">組件</span><span class="sxs-lookup"><span data-stu-id="db228-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="db228-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="db228-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db228-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db228-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db228-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="db228-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





