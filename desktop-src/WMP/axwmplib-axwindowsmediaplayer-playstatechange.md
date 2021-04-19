---
title: AxWindowsMediaPlayer 物件的 PlayStateChange 事件
description: 當 Windows Media Player 控制項的播放狀態變更時，就會發生 PlayStateChange 事件。
ms.assetid: f8823c90-2084-4771-a2fe-7081d4e49e63
keywords:
- AxWindowsMediaPlayer 物件的 PlayStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlayStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af97803224df89287847ee2b9ef83d8e976d91b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990562"
---
# <a name="playstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2cacb-104">AxWindowsMediaPlayer 物件的 PlayStateChange 事件</span><span class="sxs-lookup"><span data-stu-id="2cacb-104">PlayStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2cacb-105">當 Windows Media Player 控制項的播放狀態變更時，就會發生 PlayStateChange 事件。</span><span class="sxs-lookup"><span data-stu-id="2cacb-105">The PlayStateChange event occurs when the play state of the Windows Media Player control changes.</span></span>

``` syntax
[C#]
private void player_PlayStateChange(
  object sender,
  _WMPOCXEvents_PlayStateChangeEvent e
)

[Visual Basic]
 Private Sub player_PlayStateChange(   
 sender As Object,  
 e As _WMPOCXEvents_PlayStateChangeEvent 
 ) Handles player.PlayStateChange
 
```

## <a name="event-data"></a><span data-ttu-id="2cacb-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="2cacb-106">Event Data</span></span>

<span data-ttu-id="2cacb-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlayStateChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="2cacb-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEventHandler**.</span></span> <span data-ttu-id="2cacb-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlayStateChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2cacb-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="2cacb-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2cacb-109">Property</span></span>     | <span data-ttu-id="2cacb-110">描述</span><span class="sxs-lookup"><span data-stu-id="2cacb-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="2cacb-111">**newState**</span><span class="sxs-lookup"><span data-stu-id="2cacb-111">**newState**</span></span> | <span data-ttu-id="2cacb-112">Int32Specifies 新狀態。</span><span class="sxs-lookup"><span data-stu-id="2cacb-112">System.Int32Specifies the new state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2cacb-113">備註</span><span class="sxs-lookup"><span data-stu-id="2cacb-113">Remarks</span></span>

<span data-ttu-id="2cacb-114">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="2cacb-114">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="2cacb-115">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="2cacb-115">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="2cacb-116">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="2cacb-116">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="2cacb-117">範例</span><span class="sxs-lookup"><span data-stu-id="2cacb-117">Examples</span></span>

<span data-ttu-id="2cacb-118">下列範例會示範 PlayStateChange 事件的事件處理常式，此事件會在標籤中顯示目前的播放狀態。</span><span class="sxs-lookup"><span data-stu-id="2cacb-118">The following example demonstrates an event handler for the PlayStateChange Event that displays the current play state in a label.</span></span> <span data-ttu-id="2cacb-119">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="2cacb-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test the current state of the player and display a message for each state.
    switch (e.newState)
    {
        case 0:    // Undefined
            currentStateLabel.Text = "Undefined";
            break;

        case 1:    // Stopped
            currentStateLabel.Text = "Stopped";
            break;

        case 2:    // Paused
            currentStateLabel.Text = "Paused";
            break;

        case 3:    // Playing
            currentStateLabel.Text = "Playing";
            break;

        case 4:    // ScanForward
            currentStateLabel.Text = "ScanForward";
            break;

        case 5:    // ScanReverse
            currentStateLabel.Text = "ScanReverse";
            break;

        case 6:    // Buffering
            currentStateLabel.Text = "Buffering";
            break;

        case 7:    // Waiting
            currentStateLabel.Text = "Waiting";
            break;

        case 8:    // MediaEnded
            currentStateLabel.Text = "MediaEnded";
            break;

        case 9:    // Transitioning
            currentStateLabel.Text = "Transitioning";
            break;

        case 10:   // Ready
            currentStateLabel.Text = "Ready";
            break;

        case 11:   // Reconnecting
            currentStateLabel.Text = "Reconnecting";
            break;

        case 12:   // Last
            currentStateLabel.Text = "Last";
            break;

        default:
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString());
            break;
    }
}
```




```VB
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    ' Test the current state of the player, display a message for each state.
    Select Case e.newState

        Case 0 ' Undefined
            currentStateLabel.Text = "Undefined"

        Case 1 ' Stopped
            currentStateLabel.Text = "Stopped"

        Case 2 ' Paused
            currentStateLabel.Text = "Paused"

        Case 3 ' Playing
            currentStateLabel.Text = "Playing"

        Case 4 ' ScanForward
            currentStateLabel.Text = "ScanForward"

        Case 5 ' ScanReverse
            currentStateLabel.Text = "ScanReverse"

        Case 6 ' Buffering
            currentStateLabel.Text = "Buffering"

        Case 7 ' Waiting
            currentStateLabel.Text = "Waiting"

        Case 8 ' MediaEnded
            currentStateLabel.Text = "MediaEnded"

        Case 9 ' Transitioning
            currentStateLabel.Text = "Transitioning"

        Case 10 ' Ready
            currentStateLabel.Text = "Ready"

        Case 11 ' Reconnecting
            currentStateLabel.Text = "Reconnecting"

        Case 12 ' Last
            currentStateLabel.Text = "Last"

        Case Else
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString())

    End Select

End Sub
```



## <a name="requirements"></a><span data-ttu-id="2cacb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cacb-120">Requirements</span></span>



| <span data-ttu-id="2cacb-121">需求</span><span class="sxs-lookup"><span data-stu-id="2cacb-121">Requirement</span></span> | <span data-ttu-id="2cacb-122">值</span><span class="sxs-lookup"><span data-stu-id="2cacb-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cacb-123">版本</span><span class="sxs-lookup"><span data-stu-id="2cacb-123">Version</span></span><br/>   | <span data-ttu-id="2cacb-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2cacb-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2cacb-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="2cacb-125">Namespace</span></span><br/> | <span data-ttu-id="2cacb-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2cacb-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2cacb-127">組件</span><span class="sxs-lookup"><span data-stu-id="2cacb-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2cacb-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2cacb-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cacb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cacb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cacb-130">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2cacb-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cacb-131">**AxWindowsMediaPlayer. playState (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2cacb-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> </dl>

 

 





