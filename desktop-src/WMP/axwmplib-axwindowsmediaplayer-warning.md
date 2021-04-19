---
title: AxWindowsMediaPlayer 物件的警告事件
description: 警告事件已保留供日後使用。
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- AxWindowsMediaPlayer 物件的警告事件 Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987878"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f7f70-104">AxWindowsMediaPlayer 物件的警告事件</span><span class="sxs-lookup"><span data-stu-id="f7f70-104">Warning Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f7f70-105">警告事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="f7f70-105">The Warning event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a><span data-ttu-id="f7f70-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="f7f70-106">Event Data</span></span>

<span data-ttu-id="f7f70-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ WarningEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="f7f70-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_WarningEventHandler**.</span></span> <span data-ttu-id="f7f70-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ WarningEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f7f70-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_WarningEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="f7f70-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f7f70-109">Property</span></span>    | <span data-ttu-id="f7f70-110">描述</span><span class="sxs-lookup"><span data-stu-id="f7f70-110">Description</span></span>                                |
|-------------|--------------------------------------------|
| <span data-ttu-id="f7f70-111">warningType</span><span class="sxs-lookup"><span data-stu-id="f7f70-111">warningType</span></span> | <span data-ttu-id="f7f70-112">**System.object** 不支援。</span><span class="sxs-lookup"><span data-stu-id="f7f70-112">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="f7f70-113">參數</span><span class="sxs-lookup"><span data-stu-id="f7f70-113">param</span></span>       | <span data-ttu-id="f7f70-114">**System.object** 不支援。</span><span class="sxs-lookup"><span data-stu-id="f7f70-114">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="f7f70-115">description</span><span class="sxs-lookup"><span data-stu-id="f7f70-115">description</span></span> | <span data-ttu-id="f7f70-116">**System.string** 不支援。</span><span class="sxs-lookup"><span data-stu-id="f7f70-116">**System.String** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7f70-117">備註</span><span class="sxs-lookup"><span data-stu-id="f7f70-117">Remarks</span></span>

<span data-ttu-id="f7f70-118">此事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="f7f70-118">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7f70-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7f70-119">Requirements</span></span>



| <span data-ttu-id="f7f70-120">需求</span><span class="sxs-lookup"><span data-stu-id="f7f70-120">Requirement</span></span> | <span data-ttu-id="f7f70-121">值</span><span class="sxs-lookup"><span data-stu-id="f7f70-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f70-122">版本</span><span class="sxs-lookup"><span data-stu-id="f7f70-122">Version</span></span><br/>   | <span data-ttu-id="f7f70-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f7f70-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f7f70-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="f7f70-124">Namespace</span></span><br/> | <span data-ttu-id="f7f70-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f7f70-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f7f70-126">組件</span><span class="sxs-lookup"><span data-stu-id="f7f70-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f7f70-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="f7f70-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7f70-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7f70-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f70-129">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f7f70-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





