---
title: AxWindowsMediaPlayer 物件的 MediaError 事件
description: 當媒體物件有錯誤情況時，就會發生 MediaError 事件。
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- AxWindowsMediaPlayer 物件的 MediaError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993228"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="11eb7-104">AxWindowsMediaPlayer 物件的 MediaError 事件</span><span class="sxs-lookup"><span data-stu-id="11eb7-104">MediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="11eb7-105">當媒體物件有錯誤情況時，就會發生 MediaError 事件。</span><span class="sxs-lookup"><span data-stu-id="11eb7-105">The MediaError event occurs when a media object has an error condition.</span></span>

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a><span data-ttu-id="11eb7-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="11eb7-106">Event Data</span></span>

<span data-ttu-id="11eb7-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaErrorEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="11eb7-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEventHandler**.</span></span> <span data-ttu-id="11eb7-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaErrorEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="11eb7-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="11eb7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="11eb7-109">Property</span></span>     | <span data-ttu-id="11eb7-110">描述</span><span class="sxs-lookup"><span data-stu-id="11eb7-110">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11eb7-111">pMediaObject</span><span class="sxs-lookup"><span data-stu-id="11eb7-111">pMediaObject</span></span> | <span data-ttu-id="11eb7-112">具有錯誤狀況的 ObjectObject。</span><span class="sxs-lookup"><span data-stu-id="11eb7-112">System.ObjectObject that has an error condition.</span></span> <span data-ttu-id="11eb7-113">您可以將此轉換成 IWMPMedia 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="11eb7-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="11eb7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="11eb7-114">Requirements</span></span>



| <span data-ttu-id="11eb7-115">需求</span><span class="sxs-lookup"><span data-stu-id="11eb7-115">Requirement</span></span> | <span data-ttu-id="11eb7-116">值</span><span class="sxs-lookup"><span data-stu-id="11eb7-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11eb7-117">版本</span><span class="sxs-lookup"><span data-stu-id="11eb7-117">Version</span></span><br/>   | <span data-ttu-id="11eb7-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="11eb7-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="11eb7-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="11eb7-119">Namespace</span></span><br/> | <span data-ttu-id="11eb7-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="11eb7-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="11eb7-121">組件</span><span class="sxs-lookup"><span data-stu-id="11eb7-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="11eb7-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="11eb7-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11eb7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11eb7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11eb7-124">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="11eb7-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="11eb7-125">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="11eb7-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





