---
title: IWMPNetwork receptionQuality 屬性
description: ReceptionQuality 屬性會取得過去30秒內未遺失的封包百分比。
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- receptionQuality 屬性 Windows Media Player
- receptionQuality 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，receptionQuality 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978512"
---
# <a name="iwmpnetworkreceptionquality-property"></a><span data-ttu-id="d6fb4-106">IWMPNetwork：： receptionQuality 屬性</span><span class="sxs-lookup"><span data-stu-id="d6fb4-106">IWMPNetwork::receptionQuality property</span></span>

<span data-ttu-id="d6fb4-107">**ReceptionQuality** 屬性會取得過去30秒內未遺失的封包百分比。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-107">The **receptionQuality** property gets the percentage of packets not lost in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6fb4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6fb4-108">Syntax</span></span>


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="d6fb4-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d6fb4-109">Property value</span></span>

<span data-ttu-id="d6fb4-110">表示接收品質的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-110">A **System.Int32** that is the reception quality.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6fb4-111">備註</span><span class="sxs-lookup"><span data-stu-id="d6fb4-111">Remarks</span></span>

<span data-ttu-id="d6fb4-112">串流期間接收、遺失和復原的封包數目會每秒監視一次。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-112">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="d6fb4-113">**ReceptionQuality** 屬性會取得過去30秒內未遺失的封包百分比。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-113">The **receptionQuality** property gets the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="d6fb4-114">每次播放都會停止並重新啟動，這個屬性會重設為零。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="d6fb4-115">如果播放暫停，則不會重設此值。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-115">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="d6fb4-116">這個屬性只會在執行時間使用 **AxWindowsMediaPlayer** url 屬性來設定播放的 URL 時，才會取得有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="d6fb4-117">範例</span><span class="sxs-lookup"><span data-stu-id="d6fb4-117">Examples</span></span>

<span data-ttu-id="d6fb4-118">下列範例會使用 **receptionQuality** 來顯示標籤中收到的封包百分比，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-118">The following example uses **receptionQuality** to display the percentage of packets received in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="d6fb4-119">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="d6fb4-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="d6fb4-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d6fb4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6fb4-121">Requirements</span></span>



| <span data-ttu-id="d6fb4-122">需求</span><span class="sxs-lookup"><span data-stu-id="d6fb4-122">Requirement</span></span> | <span data-ttu-id="d6fb4-123">值</span><span class="sxs-lookup"><span data-stu-id="d6fb4-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fb4-124">版本</span><span class="sxs-lookup"><span data-stu-id="d6fb4-124">Version</span></span><br/>   | <span data-ttu-id="d6fb4-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d6fb4-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d6fb4-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="d6fb4-126">Namespace</span></span><br/> | <span data-ttu-id="d6fb4-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d6fb4-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d6fb4-128">組件</span><span class="sxs-lookup"><span data-stu-id="d6fb4-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d6fb4-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d6fb4-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6fb4-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6fb4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fb4-131">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d6fb4-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d6fb4-132">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d6fb4-132">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





