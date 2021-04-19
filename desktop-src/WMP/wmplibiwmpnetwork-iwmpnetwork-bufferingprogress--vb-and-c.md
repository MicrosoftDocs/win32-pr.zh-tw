---
title: IWMPNetwork bufferingProgress 屬性
description: BufferingProgress 屬性會取得緩衝處理已完成的百分比。
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- bufferingProgress 屬性 Windows Media Player
- bufferingProgress 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，bufferingProgress 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998851"
---
# <a name="iwmpnetworkbufferingprogress-property"></a><span data-ttu-id="90e12-106">IWMPNetwork：： bufferingProgress 屬性</span><span class="sxs-lookup"><span data-stu-id="90e12-106">IWMPNetwork::bufferingProgress property</span></span>

<span data-ttu-id="90e12-107">**BufferingProgress** 屬性會取得緩衝處理已完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="90e12-107">The **bufferingProgress** property gets the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e12-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="90e12-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="90e12-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="90e12-109">Property value</span></span>

<span data-ttu-id="90e12-110">表示以百分比表示之緩衝進度的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="90e12-110">A **System.Int32** that is the buffering progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="90e12-111">備註</span><span class="sxs-lookup"><span data-stu-id="90e12-111">Remarks</span></span>

<span data-ttu-id="90e12-112">每次播放都會停止並重新啟動，這個屬性會重設為零。</span><span class="sxs-lookup"><span data-stu-id="90e12-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="90e12-113">如果播放暫停，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="90e12-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="90e12-114">緩衝處理只適用于串流內容。</span><span class="sxs-lookup"><span data-stu-id="90e12-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="90e12-115">這個屬性只會在執行時間期間取得有效的資訊。當播放的 URL 是使用 **AxWindowsMediaPlayer** 屬性設定時。</span><span class="sxs-lookup"><span data-stu-id="90e12-115">This property gets valid information only during run time when the URL for playback is set using the **AxWindowsMediaPlayer.URL** property.</span></span>

<span data-ttu-id="90e12-116">使用 **AxWindowsMediaPlayer。 \_WMPOCXEvents \_ BufferingEvent** ，以判斷何時啟動或停止緩衝。</span><span class="sxs-lookup"><span data-stu-id="90e12-116">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="90e12-117">範例</span><span class="sxs-lookup"><span data-stu-id="90e12-117">Examples</span></span>

<span data-ttu-id="90e12-118">下列範例會使用 **bufferingProgress** 來顯示在標籤中完成的緩衝百分比，以回應緩衝事件。</span><span class="sxs-lookup"><span data-stu-id="90e12-118">The following example uses **bufferingProgress** to display the percentage of buffering completed in a label, in response to the Buffering Event.</span></span> <span data-ttu-id="90e12-119">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="90e12-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="90e12-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="90e12-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="90e12-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="90e12-121">Requirements</span></span>



| <span data-ttu-id="90e12-122">需求</span><span class="sxs-lookup"><span data-stu-id="90e12-122">Requirement</span></span> | <span data-ttu-id="90e12-123">值</span><span class="sxs-lookup"><span data-stu-id="90e12-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90e12-124">版本</span><span class="sxs-lookup"><span data-stu-id="90e12-124">Version</span></span><br/>   | <span data-ttu-id="90e12-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="90e12-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="90e12-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="90e12-126">Namespace</span></span><br/> | <span data-ttu-id="90e12-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="90e12-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="90e12-128">組件</span><span class="sxs-lookup"><span data-stu-id="90e12-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="90e12-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="90e12-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e12-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90e12-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e12-131">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="90e12-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="90e12-132">**AxWindowsMediaPlayer (VB 和 c # ) 的緩衝事件**</span><span class="sxs-lookup"><span data-stu-id="90e12-132">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="90e12-133">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="90e12-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





