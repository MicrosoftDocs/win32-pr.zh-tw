---
title: AxWindowsMediaPlayer 物件的 LibraryDisconnect 事件
description: 當程式庫不再可用時，就會發生 LibraryDisconnect 事件。
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- AxWindowsMediaPlayer 物件的 LibraryDisconnect 事件 Windows Media Player
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999476"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="48085-104">AxWindowsMediaPlayer 物件的 LibraryDisconnect 事件</span><span class="sxs-lookup"><span data-stu-id="48085-104">LibraryDisconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="48085-105">當程式庫不再可用時，就會發生 LibraryDisconnect 事件。</span><span class="sxs-lookup"><span data-stu-id="48085-105">The LibraryDisconnect event occurs when a library is no longer available.</span></span>

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a><span data-ttu-id="48085-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="48085-106">Event Data</span></span>

<span data-ttu-id="48085-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ LibraryDisconnectEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="48085-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEventHandler**.</span></span> <span data-ttu-id="48085-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ LibraryDisconnectEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="48085-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="48085-109">屬性</span><span class="sxs-lookup"><span data-stu-id="48085-109">Property</span></span> | <span data-ttu-id="48085-110">描述</span><span class="sxs-lookup"><span data-stu-id="48085-110">Description</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48085-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="48085-111">pLibrary</span></span> | <span data-ttu-id="48085-112">**WMPLib. IWMPLibrary** 表示已中斷連結之程式庫的介面。</span><span class="sxs-lookup"><span data-stu-id="48085-112">**WMPLib.IWMPLibrary** The interface that represents the library that disconnected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48085-113">備註</span><span class="sxs-lookup"><span data-stu-id="48085-113">Remarks</span></span>

<span data-ttu-id="48085-114">本機程式庫不會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="48085-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="48085-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="48085-115">Requirements</span></span>



| <span data-ttu-id="48085-116">需求</span><span class="sxs-lookup"><span data-stu-id="48085-116">Requirement</span></span> | <span data-ttu-id="48085-117">值</span><span class="sxs-lookup"><span data-stu-id="48085-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48085-118">版本</span><span class="sxs-lookup"><span data-stu-id="48085-118">Version</span></span><br/>   | <span data-ttu-id="48085-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="48085-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="48085-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="48085-120">Namespace</span></span><br/> | <span data-ttu-id="48085-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="48085-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="48085-122">組件</span><span class="sxs-lookup"><span data-stu-id="48085-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="48085-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="48085-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48085-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48085-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48085-125">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48085-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48085-126">**IWMPLibrary 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48085-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





