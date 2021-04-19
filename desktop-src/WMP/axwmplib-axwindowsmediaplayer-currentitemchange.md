---
title: AxWindowsMediaPlayer 物件的 CurrentItemChange 事件
description: IWMPControls. currentItem 的值變更時，就會發生 CurrentItemChange 事件。
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- AxWindowsMediaPlayer 物件的 CurrentItemChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c33bb3e9c4c1e512e742c0e679f3c5b53a29735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989707"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a5630-104">AxWindowsMediaPlayer 物件的 CurrentItemChange 事件</span><span class="sxs-lookup"><span data-stu-id="a5630-104">CurrentItemChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a5630-105">IWMPControls 的值時，就會發生 CurrentItemChange 事件。**currentItem** 變更。</span><span class="sxs-lookup"><span data-stu-id="a5630-105">The CurrentItemChange event occurs when the value of IWMPControls.**currentItem** changes.</span></span>

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a><span data-ttu-id="a5630-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="a5630-106">Event Data</span></span>

<span data-ttu-id="a5630-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CurrentItemChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="a5630-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEventHandler**.</span></span> <span data-ttu-id="a5630-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CurrentItemChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a5630-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a5630-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a5630-109">Property</span></span>   | <span data-ttu-id="a5630-110">描述</span><span class="sxs-lookup"><span data-stu-id="a5630-110">Description</span></span>                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5630-111">pdispMedia</span><span class="sxs-lookup"><span data-stu-id="a5630-111">pdispMedia</span></span> | <span data-ttu-id="a5630-112">ObjectThe 新的目前媒體專案。</span><span class="sxs-lookup"><span data-stu-id="a5630-112">System.ObjectThe new current media item.</span></span> <span data-ttu-id="a5630-113">您可以將此轉換成 IWMPMedia 介面來存取它。</span><span class="sxs-lookup"><span data-stu-id="a5630-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="a5630-114">範例</span><span class="sxs-lookup"><span data-stu-id="a5630-114">Examples</span></span>

<span data-ttu-id="a5630-115">下列範例示範 CurrentItemChange 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="a5630-115">The following example demonstrates an event handler for the CurrentItemChange event.</span></span> <span data-ttu-id="a5630-116">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="a5630-116">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a5630-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5630-117">Requirements</span></span>



| <span data-ttu-id="a5630-118">需求</span><span class="sxs-lookup"><span data-stu-id="a5630-118">Requirement</span></span> | <span data-ttu-id="a5630-119">值</span><span class="sxs-lookup"><span data-stu-id="a5630-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5630-120">版本</span><span class="sxs-lookup"><span data-stu-id="a5630-120">Version</span></span><br/>   | <span data-ttu-id="a5630-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a5630-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a5630-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="a5630-122">Namespace</span></span><br/> | <span data-ttu-id="a5630-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a5630-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a5630-124">組件</span><span class="sxs-lookup"><span data-stu-id="a5630-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a5630-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a5630-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5630-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5630-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5630-127">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a5630-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5630-128">**IWMPControls. currentItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a5630-128">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5630-129">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a5630-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





