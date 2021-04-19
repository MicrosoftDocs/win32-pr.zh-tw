---
title: IWMPNetwork receivedPackets 屬性
description: ReceivedPackets 屬性會取得已接收的封包數目。
ms.assetid: 2a79dc81-4c7a-45d6-bc2b-b19ff5704c3b
keywords:
- receivedPackets 屬性 Windows Media Player
- receivedPackets 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，receivedPackets 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.receivedPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c62b4d90039f07177e8fcdc971cb66e0044aee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991245"
---
# <a name="iwmpnetworkreceivedpackets-property"></a><span data-ttu-id="0284f-106">IWMPNetwork：： receivedPackets 屬性</span><span class="sxs-lookup"><span data-stu-id="0284f-106">IWMPNetwork::receivedPackets property</span></span>

<span data-ttu-id="0284f-107">**ReceivedPackets** 屬性會取得已接收的封包數目。</span><span class="sxs-lookup"><span data-stu-id="0284f-107">The **receivedPackets** property gets the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="0284f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0284f-108">Syntax</span></span>


```CSharp
public System.Int32 receivedPackets {get; set;}
```


```VB

Public ReadOnly Property receivedPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0284f-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="0284f-109">Property value</span></span>

<span data-ttu-id="0284f-110">已接收的封包數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="0284f-110">A **System.Int32** that is the number of packets received.</span></span>

## <a name="remarks"></a><span data-ttu-id="0284f-111">備註</span><span class="sxs-lookup"><span data-stu-id="0284f-111">Remarks</span></span>

<span data-ttu-id="0284f-112">每次播放都會停止並重新啟動，這個屬性會重設為零。</span><span class="sxs-lookup"><span data-stu-id="0284f-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="0284f-113">如果播放暫停，則不會重設此值。</span><span class="sxs-lookup"><span data-stu-id="0284f-113">The value is not reset if playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="0284f-114">範例</span><span class="sxs-lookup"><span data-stu-id="0284f-114">Examples</span></span>

<span data-ttu-id="0284f-115">下列範例會使用 **receivedPackets** 來顯示已接收的封包數目。</span><span class="sxs-lookup"><span data-stu-id="0284f-115">The following example uses **receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="0284f-116">這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="0284f-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="0284f-117">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="0284f-117">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="0284f-118">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="0284f-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether packets may be arriving.
    switch (e.newState)
    {
        // If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
        // or Transitioning then stop the timer. 
        case 1: 
        case 2: 
        case 4: 
        case 5: 
        case 7: 
        case 8: 
        case 9: 
            timer.Stop();
            break;

        // If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        default:
            timer.Interval = 1000;
            timer.Start();
            break;
    }
}

private void UpdateReceivedPackets(object sender, EventArgs e)
{
    receivedPacketsLabel.Text = ("Packets received: " + player.network.receivedPackets.ToString());
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

Public Sub UpdateReceivedPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receivedPacketsLabel.Text = (&quot;Packets received: &quot; + player.network.receivedPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0284f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0284f-119">Requirements</span></span>



| <span data-ttu-id="0284f-120">需求</span><span class="sxs-lookup"><span data-stu-id="0284f-120">Requirement</span></span> | <span data-ttu-id="0284f-121">值</span><span class="sxs-lookup"><span data-stu-id="0284f-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0284f-122">版本</span><span class="sxs-lookup"><span data-stu-id="0284f-122">Version</span></span><br/>   | <span data-ttu-id="0284f-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="0284f-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0284f-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="0284f-124">Namespace</span></span><br/> | <span data-ttu-id="0284f-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0284f-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0284f-126">組件</span><span class="sxs-lookup"><span data-stu-id="0284f-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0284f-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="0284f-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0284f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0284f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0284f-129">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0284f-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





