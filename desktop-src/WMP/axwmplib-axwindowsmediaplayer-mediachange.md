---
title: AxWindowsMediaPlayer 物件的 MediaChange 事件
description: 當媒體專案變更時，就會發生 MediaChange 事件。 |AxWindowsMediaPlayer 物件的 MediaChange 事件
ms.assetid: 0a2380ff-df50-4092-a952-812184822719
keywords:
- AxWindowsMediaPlayer 物件的 MediaChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175a7ed6ca57e3083d307cfe218d09233410053c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978762"
---
# <a name="mediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="04a24-105">AxWindowsMediaPlayer 物件的 MediaChange 事件</span><span class="sxs-lookup"><span data-stu-id="04a24-105">MediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="04a24-106">當媒體專案變更時，就會發生 MediaChange 事件。</span><span class="sxs-lookup"><span data-stu-id="04a24-106">The MediaChange event occurs when a media item changes.</span></span>

``` syntax
[C#]
private void player_MediaChange(
  object sender,
  _WMPOCXEvents_MediaChangeEvent e
)

[Visual Basic]
Private Sub player_MediaChange(  
  sender As Object,  
  e As _WMPOCXEvents_MediaChangeEvent
) Handles player.MediaChange
```

## <a name="event-data"></a><span data-ttu-id="04a24-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="04a24-107">Event Data</span></span>

<span data-ttu-id="04a24-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ MediaChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="04a24-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEventHandler**.</span></span> <span data-ttu-id="04a24-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ MediaChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="04a24-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="04a24-110">屬性</span><span class="sxs-lookup"><span data-stu-id="04a24-110">Property</span></span> | <span data-ttu-id="04a24-111">描述</span><span class="sxs-lookup"><span data-stu-id="04a24-111">Description</span></span>                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a24-112">Item</span><span class="sxs-lookup"><span data-stu-id="04a24-112">Item</span></span>     | <span data-ttu-id="04a24-113">已變更的 ObjectThe 媒體專案。</span><span class="sxs-lookup"><span data-stu-id="04a24-113">System.ObjectThe media item that changed.</span></span> <span data-ttu-id="04a24-114">您可以將此轉換成 IWMPMedia 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="04a24-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="04a24-115">範例</span><span class="sxs-lookup"><span data-stu-id="04a24-115">Examples</span></span>

<span data-ttu-id="04a24-116">下列範例會使用標籤顯示目前媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="04a24-116">The following example uses a label to display the name of the current media item.</span></span> <span data-ttu-id="04a24-117">程式碼會在每次發生 MediaChange 事件時，更新標籤中的文字。</span><span class="sxs-lookup"><span data-stu-id="04a24-117">The code updates the text in the label with each occurrence of the MediaChange Event.</span></span> <span data-ttu-id="04a24-118">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="04a24-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the MediaChange event.
player.MediaChange += new AxWMPLib._WMPOCXEvents_MediaChangeEventHandler(player_MediaChange);

private void player_MediaChange(object sender, AxWMPLib._WMPOCXEvents_MediaChangeEvent e)
{
    // Get an interface to the changed media item that is returned in the event data. 
    WMPLib.IWMPMedia3 changedItem = (WMPLib.IWMPMedia3)e.item;

    // Display the name of the changed media item.
    mediaName.Text = changedItem.name;
}
```


```VB

Public Sub player_MediaChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_MediaChangeEvent) Handles player.MediaChange

    &#39; Get an interface to the changed media item that is returned in the event data.
    Dim changedItem As WMPLib.IWMPMedia3 = e.item

    &#39; Display the name of the changed media item.
    mediaName.Text = changedItem.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="04a24-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="04a24-119">Requirements</span></span>



| <span data-ttu-id="04a24-120">需求</span><span class="sxs-lookup"><span data-stu-id="04a24-120">Requirement</span></span> | <span data-ttu-id="04a24-121">值</span><span class="sxs-lookup"><span data-stu-id="04a24-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a24-122">版本</span><span class="sxs-lookup"><span data-stu-id="04a24-122">Version</span></span><br/>   | <span data-ttu-id="04a24-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="04a24-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="04a24-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="04a24-124">Namespace</span></span><br/> | <span data-ttu-id="04a24-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="04a24-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="04a24-126">組件</span><span class="sxs-lookup"><span data-stu-id="04a24-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="04a24-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="04a24-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04a24-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04a24-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a24-129">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="04a24-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04a24-130">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="04a24-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





