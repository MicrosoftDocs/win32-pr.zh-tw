---
title: AxWindowsMediaPlayer 物件的 StatusChange 事件
description: 當 status 屬性變更值時，就會發生 StatusChange 事件。 |AxWindowsMediaPlayer 物件的 StatusChange 事件
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- AxWindowsMediaPlayer 物件的 StatusChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000811"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6d57b-105">AxWindowsMediaPlayer 物件的 StatusChange 事件</span><span class="sxs-lookup"><span data-stu-id="6d57b-105">StatusChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6d57b-106">當 **status** 屬性變更值時，就會發生 **StatusChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="6d57b-106">The **StatusChange** event occurs when the **status** property changes value.</span></span>

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a><span data-ttu-id="6d57b-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="6d57b-107">Event Data</span></span>

<span data-ttu-id="6d57b-108">此事件不包含資料。</span><span class="sxs-lookup"><span data-stu-id="6d57b-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d57b-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d57b-109">Requirements</span></span>



| <span data-ttu-id="6d57b-110">需求</span><span class="sxs-lookup"><span data-stu-id="6d57b-110">Requirement</span></span> | <span data-ttu-id="6d57b-111">值</span><span class="sxs-lookup"><span data-stu-id="6d57b-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d57b-112">版本</span><span class="sxs-lookup"><span data-stu-id="6d57b-112">Version</span></span><br/>   | <span data-ttu-id="6d57b-113">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6d57b-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6d57b-114">命名空間</span><span class="sxs-lookup"><span data-stu-id="6d57b-114">Namespace</span></span><br/> | <span data-ttu-id="6d57b-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6d57b-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6d57b-116">組件</span><span class="sxs-lookup"><span data-stu-id="6d57b-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6d57b-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6d57b-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d57b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d57b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d57b-119">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6d57b-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d57b-120">**AxWindowsMediaPlayer： VB 和 c # 的狀態 ()**</span><span class="sxs-lookup"><span data-stu-id="6d57b-120">**AxWindowsMediaPlayer.status (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





