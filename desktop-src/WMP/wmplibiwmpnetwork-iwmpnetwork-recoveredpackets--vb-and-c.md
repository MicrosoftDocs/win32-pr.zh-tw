---
title: IWMPNetwork recoveredPackets 屬性
description: RecoveredPackets 屬性會取得已復原的封包數目。
ms.assetid: 90fcefcd-2bd7-4fb5-8337-36bec5d44e60
keywords:
- recoveredPackets 屬性 Windows Media Player
- recoveredPackets 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，recoveredPackets 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.recoveredPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe9fb8b44249be30289abb2f8922343285ca074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994907"
---
# <a name="iwmpnetworkrecoveredpackets-property"></a><span data-ttu-id="6b2aa-106">IWMPNetwork：： recoveredPackets 屬性</span><span class="sxs-lookup"><span data-stu-id="6b2aa-106">IWMPNetwork::recoveredPackets property</span></span>

<span data-ttu-id="6b2aa-107">**RecoveredPackets** 屬性會取得已復原的封包數目。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-107">The **recoveredPackets** property gets the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2aa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b2aa-108">Syntax</span></span>


```CSharp
public System.Int32 recoveredPackets {get; set;}
```


```VB

Public ReadOnly Property recoveredPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6b2aa-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6b2aa-109">Property value</span></span>

<span data-ttu-id="6b2aa-110">已復原封包數目的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-110">A **System.Int32** that is the number of recovered packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b2aa-111">備註</span><span class="sxs-lookup"><span data-stu-id="6b2aa-111">Remarks</span></span>

<span data-ttu-id="6b2aa-112">每次播放都會停止並重新啟動，這個屬性會重設為零。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="6b2aa-113">如果播放暫停，則不會重設此值。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-113">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="6b2aa-114">這個屬性只會在執行時間使用 **AxWindowsMediaPlayer** url 屬性來設定播放的 URL 時，才會取得有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-114">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span> <span data-ttu-id="6b2aa-115">使用 HTTP 通訊協定時，值會是零，這會是不失真的。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-115">The value will be zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="6b2aa-116">範例</span><span class="sxs-lookup"><span data-stu-id="6b2aa-116">Examples</span></span>

<span data-ttu-id="6b2aa-117">下列範例會使用 **recoveredPackets** 來顯示標籤中已復原的封包數目，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-117">The following example uses **recoveredPackets** to display the number of recovered packets in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="6b2aa-118">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="6b2aa-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="6b2aa-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateRecoveredPackets(object sender, EventArgs e)
{
    recoveredPacketsLabel.Text = ("Packets recovered: " + player.network.recoveredPackets.ToString());
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateRecoveredPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    recoveredPacketsLabel.Text = (&quot;Packets recovered: &quot; + player.network.recoveredPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6b2aa-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b2aa-120">Requirements</span></span>



| <span data-ttu-id="6b2aa-121">需求</span><span class="sxs-lookup"><span data-stu-id="6b2aa-121">Requirement</span></span> | <span data-ttu-id="6b2aa-122">值</span><span class="sxs-lookup"><span data-stu-id="6b2aa-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2aa-123">版本</span><span class="sxs-lookup"><span data-stu-id="6b2aa-123">Version</span></span><br/>   | <span data-ttu-id="6b2aa-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6b2aa-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6b2aa-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="6b2aa-125">Namespace</span></span><br/> | <span data-ttu-id="6b2aa-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6b2aa-127">組件</span><span class="sxs-lookup"><span data-stu-id="6b2aa-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6b2aa-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6b2aa-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2aa-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b2aa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2aa-130">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6b2aa-131">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





