---
title: AxWindowsMediaPlayer 物件的 LibraryConnect 事件
description: 當程式庫變成可用時，就會發生 LibraryConnect 事件。
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- AxWindowsMediaPlayer 物件的 LibraryConnect 事件 Windows Media Player
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993229"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="35c5c-104">AxWindowsMediaPlayer 物件的 LibraryConnect 事件</span><span class="sxs-lookup"><span data-stu-id="35c5c-104">LibraryConnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="35c5c-105">當程式庫變成可用時，就會發生 LibraryConnect 事件。</span><span class="sxs-lookup"><span data-stu-id="35c5c-105">The LibraryConnect event occurs when a library becomes available.</span></span>

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a><span data-ttu-id="35c5c-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="35c5c-106">Event Data</span></span>

<span data-ttu-id="35c5c-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ LibraryConnectEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="35c5c-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEventHandler**.</span></span> <span data-ttu-id="35c5c-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ LibraryConnectEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="35c5c-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="35c5c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="35c5c-109">Property</span></span> | <span data-ttu-id="35c5c-110">描述</span><span class="sxs-lookup"><span data-stu-id="35c5c-110">Description</span></span>                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c5c-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="35c5c-111">pLibrary</span></span> | <span data-ttu-id="35c5c-112">**WMPLib. IWMPLibrary** 表示連接程式庫的介面。</span><span class="sxs-lookup"><span data-stu-id="35c5c-112">**WMPLib.IWMPLibrary** The interface that represents the library that connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35c5c-113">備註</span><span class="sxs-lookup"><span data-stu-id="35c5c-113">Remarks</span></span>

<span data-ttu-id="35c5c-114">本機程式庫不會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="35c5c-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c5c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="35c5c-115">Requirements</span></span>



| <span data-ttu-id="35c5c-116">需求</span><span class="sxs-lookup"><span data-stu-id="35c5c-116">Requirement</span></span> | <span data-ttu-id="35c5c-117">值</span><span class="sxs-lookup"><span data-stu-id="35c5c-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c5c-118">版本</span><span class="sxs-lookup"><span data-stu-id="35c5c-118">Version</span></span><br/>   | <span data-ttu-id="35c5c-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="35c5c-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="35c5c-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="35c5c-120">Namespace</span></span><br/> | <span data-ttu-id="35c5c-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="35c5c-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="35c5c-122">組件</span><span class="sxs-lookup"><span data-stu-id="35c5c-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="35c5c-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="35c5c-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35c5c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35c5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c5c-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="35c5c-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="35c5c-126">**IWMPLibrary 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="35c5c-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





