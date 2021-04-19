---
title: AxWindowsMediaPlayer 物件的 StringCollectionChange 事件
description: 當字串集合變更時，就會發生 StringCollectionChange 事件。 |AxWindowsMediaPlayer 物件的 StringCollectionChange 事件
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- AxWindowsMediaPlayer 物件的 StringCollectionChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986568"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b6dad-105">AxWindowsMediaPlayer 物件的 StringCollectionChange 事件</span><span class="sxs-lookup"><span data-stu-id="b6dad-105">StringCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b6dad-106">當字串集合變更時，就會發生 StringCollectionChange 事件。</span><span class="sxs-lookup"><span data-stu-id="b6dad-106">The StringCollectionChange event occurs when a string collection changes.</span></span>

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="b6dad-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="b6dad-107">Event Data</span></span>

<span data-ttu-id="b6dad-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ StringCollectionChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="b6dad-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEventHandler**.</span></span> <span data-ttu-id="b6dad-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ StringCollectionChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="b6dad-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="b6dad-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b6dad-110">Property</span></span>              | <span data-ttu-id="b6dad-111">描述</span><span class="sxs-lookup"><span data-stu-id="b6dad-111">Description</span></span>                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dad-112">pdispStringCollection</span><span class="sxs-lookup"><span data-stu-id="b6dad-112">pdispStringCollection</span></span> | <span data-ttu-id="b6dad-113">已變更的 ObjectThe 字串集合專案。</span><span class="sxs-lookup"><span data-stu-id="b6dad-113">System.ObjectThe string collection item that changed.</span></span> <span data-ttu-id="b6dad-114">您可以將此轉換成 IWMPStringCollection 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="b6dad-114">You can cast this to an IWMPStringCollection interface to access it.</span></span><br/> |
| <span data-ttu-id="b6dad-115">lCollectionIndex</span><span class="sxs-lookup"><span data-stu-id="b6dad-115">lCollectionIndex</span></span>      | <span data-ttu-id="b6dad-116">已變更之字串收集項目的 Int32The 索引。</span><span class="sxs-lookup"><span data-stu-id="b6dad-116">System.Int32The index of the string collection item that changed.</span></span><br/>                                                          |
| <span data-ttu-id="b6dad-117">變更</span><span class="sxs-lookup"><span data-stu-id="b6dad-117">change</span></span>                | <span data-ttu-id="b6dad-118">WMPLib. WMPStringCollectionChangeEventTypeAn 列舉值，表示發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="b6dad-118">WMPLib.WMPStringCollectionChangeEventTypeAn enumeration value indicating the type of change that occurred.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="b6dad-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6dad-119">Requirements</span></span>



| <span data-ttu-id="b6dad-120">需求</span><span class="sxs-lookup"><span data-stu-id="b6dad-120">Requirement</span></span> | <span data-ttu-id="b6dad-121">值</span><span class="sxs-lookup"><span data-stu-id="b6dad-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dad-122">版本</span><span class="sxs-lookup"><span data-stu-id="b6dad-122">Version</span></span><br/>   | <span data-ttu-id="b6dad-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b6dad-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b6dad-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="b6dad-124">Namespace</span></span><br/> | <span data-ttu-id="b6dad-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b6dad-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b6dad-126">組件</span><span class="sxs-lookup"><span data-stu-id="b6dad-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6dad-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b6dad-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6dad-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6dad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6dad-129">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b6dad-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6dad-130">**IWMPStringCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b6dad-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6dad-131">**WMPStringCollectionChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="b6dad-131">**WMPStringCollectionChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





