---
title: IWMPControls currentPositionString 屬性
description: CurrentPositionString 屬性會取得媒體專案中的目前位置，作為格式化為 HH MM SS 的字串， (小時、分鐘和秒) 。
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- currentPositionString 屬性 Windows Media Player
- currentPositionString 屬性 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，currentPositionString 屬性
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999389"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a><span data-ttu-id="facc9-106">IWMPControls：： currentPositionString 屬性</span><span class="sxs-lookup"><span data-stu-id="facc9-106">IWMPControls::currentPositionString property</span></span>

<span data-ttu-id="facc9-107">**CurrentPositionString** 屬性會取得媒體專案中的目前位置，作為格式化為 HH： MM： SS (時、分和秒) 的字串。</span><span class="sxs-lookup"><span data-stu-id="facc9-107">The **currentPositionString** property gets the current position in the media item as a string formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

<span data-ttu-id="facc9-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="facc9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="facc9-109">語法</span><span class="sxs-lookup"><span data-stu-id="facc9-109">Syntax</span></span>


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a><span data-ttu-id="facc9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="facc9-110">Property value</span></span>

<span data-ttu-id="facc9-111">已格式化的 **system.string** ，表示目前的位置。</span><span class="sxs-lookup"><span data-stu-id="facc9-111">A formatted **System.String** that is the current position.</span></span>

## <a name="remarks"></a><span data-ttu-id="facc9-112">備註</span><span class="sxs-lookup"><span data-stu-id="facc9-112">Remarks</span></span>

<span data-ttu-id="facc9-113">如果媒體專案的長度不到一小時，則目前的位置會格式化為 MM： SS (分鐘和秒) 。</span><span class="sxs-lookup"><span data-stu-id="facc9-113">If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).</span></span>

## <a name="examples"></a><span data-ttu-id="facc9-114">範例</span><span class="sxs-lookup"><span data-stu-id="facc9-114">Examples</span></span>

<span data-ttu-id="facc9-115">下列範例會啟動一個以一秒為間隔觸發事件的計時器。</span><span class="sxs-lookup"><span data-stu-id="facc9-115">The following example starts a timer that triggers an event at one-second intervals.</span></span> <span data-ttu-id="facc9-116">在計時器事件處理常式中，標籤會以 **currentPositionString** 進行更新。</span><span class="sxs-lookup"><span data-stu-id="facc9-116">In the timer event handler, a label is updated with the **currentPositionString**.</span></span> <span data-ttu-id="facc9-117">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="facc9-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a><span data-ttu-id="facc9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="facc9-118">Requirements</span></span>



| <span data-ttu-id="facc9-119">需求</span><span class="sxs-lookup"><span data-stu-id="facc9-119">Requirement</span></span> | <span data-ttu-id="facc9-120">值</span><span class="sxs-lookup"><span data-stu-id="facc9-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="facc9-121">版本</span><span class="sxs-lookup"><span data-stu-id="facc9-121">Version</span></span><br/>   | <span data-ttu-id="facc9-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="facc9-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="facc9-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="facc9-123">Namespace</span></span><br/> | <span data-ttu-id="facc9-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="facc9-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="facc9-125">組件</span><span class="sxs-lookup"><span data-stu-id="facc9-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="facc9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="facc9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="facc9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="facc9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="facc9-128">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="facc9-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="facc9-129">**IWMPControls. currentPosition (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="facc9-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





