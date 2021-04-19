---
title: AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件
description: 當媒體集合變更時，就會發生 MediaCollectionChange 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720207de3475544074b87c56686d0a47da97785c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000944"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="bc081-105">AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件</span><span class="sxs-lookup"><span data-stu-id="bc081-105">MediaCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="bc081-106">當媒體集合變更時，就會發生 MediaCollectionChange 事件。</span><span class="sxs-lookup"><span data-stu-id="bc081-106">The MediaCollectionChange event occurs when the media collection changes.</span></span>

``` syntax
[C#]
private void player_MediaCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_MediaCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.MediaCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="bc081-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="bc081-107">Event Data</span></span>

<span data-ttu-id="bc081-108">此事件不包含資料。</span><span class="sxs-lookup"><span data-stu-id="bc081-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc081-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc081-109">Requirements</span></span>



| <span data-ttu-id="bc081-110">需求</span><span class="sxs-lookup"><span data-stu-id="bc081-110">Requirement</span></span> | <span data-ttu-id="bc081-111">值</span><span class="sxs-lookup"><span data-stu-id="bc081-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc081-112">版本</span><span class="sxs-lookup"><span data-stu-id="bc081-112">Version</span></span><br/>   | <span data-ttu-id="bc081-113">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="bc081-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="bc081-114">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc081-114">Namespace</span></span><br/> | <span data-ttu-id="bc081-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="bc081-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="bc081-116">組件</span><span class="sxs-lookup"><span data-stu-id="bc081-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bc081-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="bc081-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc081-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc081-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc081-119">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bc081-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc081-120">**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bc081-120">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc081-121">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bc081-121">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





