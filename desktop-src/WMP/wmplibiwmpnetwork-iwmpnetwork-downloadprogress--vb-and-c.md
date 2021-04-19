---
title: IWMPNetwork downloadProgress 屬性
description: DownloadProgress 屬性會取得下載已完成的百分比。
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- downloadProgress 屬性 Windows Media Player
- downloadProgress 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，downloadProgress 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997665"
---
# <a name="iwmpnetworkdownloadprogress-property"></a><span data-ttu-id="0b100-106">IWMPNetwork：:d ownloadProgress 屬性</span><span class="sxs-lookup"><span data-stu-id="0b100-106">IWMPNetwork::downloadProgress property</span></span>

<span data-ttu-id="0b100-107">**DownloadProgress** 屬性會取得下載已完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="0b100-107">The **downloadProgress** property gets the percentage of downloading completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b100-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b100-108">Syntax</span></span>


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0b100-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="0b100-109">Property value</span></span>

<span data-ttu-id="0b100-110">以百分比表示的下載進度的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="0b100-110">A **System.Int32** that is the download progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b100-111">備註</span><span class="sxs-lookup"><span data-stu-id="0b100-111">Remarks</span></span>

<span data-ttu-id="0b100-112">當 Windows Media Player 控制項連接到可同時播放和下載的數位媒體檔案時， **downloadProgress** 屬性會取得已下載的檔案總數百分比。</span><span class="sxs-lookup"><span data-stu-id="0b100-112">When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the **downloadProgress** property gets the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="0b100-113">這項功能目前僅支援從 web 伺服器下載的數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="0b100-113">This feature is currently supported only for digital media files downloaded from web servers.</span></span> <span data-ttu-id="0b100-114">您可以同時下載並播放下列任何格式的檔案：</span><span class="sxs-lookup"><span data-stu-id="0b100-114">A file of any of the following formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="0b100-115">進階系統格式 (ASF)</span><span class="sxs-lookup"><span data-stu-id="0b100-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="0b100-116">Windows Media 音訊 (WMA)</span><span class="sxs-lookup"><span data-stu-id="0b100-116">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="0b100-117">Windows Media 視訊 (WMV)</span><span class="sxs-lookup"><span data-stu-id="0b100-117">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="0b100-118">MP3</span><span class="sxs-lookup"><span data-stu-id="0b100-118">MP3</span></span>
-   <span data-ttu-id="0b100-119">MPEG</span><span class="sxs-lookup"><span data-stu-id="0b100-119">MPEG</span></span>
-   <span data-ttu-id="0b100-120">WAV</span><span class="sxs-lookup"><span data-stu-id="0b100-120">WAV</span></span>

<span data-ttu-id="0b100-121">此外，也可以同時下載並播放某些 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="0b100-121">In addition, some AVI files can be downloaded and played simultaneously.</span></span>

<span data-ttu-id="0b100-122">使用 **AxWindowsMediaPlayer。 \_WMPOCXEvents \_ BufferingEvent** ，以判斷何時啟動或停止緩衝。</span><span class="sxs-lookup"><span data-stu-id="0b100-122">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="0b100-123">範例</span><span class="sxs-lookup"><span data-stu-id="0b100-123">Examples</span></span>

<span data-ttu-id="0b100-124">下列程式碼範例會使用 **downloadProgress** 來顯示已完成下載的百分比。</span><span class="sxs-lookup"><span data-stu-id="0b100-124">The following code example uses **downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="0b100-125">這項資訊會顯示在標籤中，以回應 **緩衝** 事件。</span><span class="sxs-lookup"><span data-stu-id="0b100-125">The information is displayed in a label, in response to the **Buffering** Event.</span></span> <span data-ttu-id="0b100-126">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="0b100-126">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="0b100-127">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="0b100-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0b100-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b100-128">Requirements</span></span>



| <span data-ttu-id="0b100-129">需求</span><span class="sxs-lookup"><span data-stu-id="0b100-129">Requirement</span></span> | <span data-ttu-id="0b100-130">值</span><span class="sxs-lookup"><span data-stu-id="0b100-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b100-131">版本</span><span class="sxs-lookup"><span data-stu-id="0b100-131">Version</span></span><br/>   | <span data-ttu-id="0b100-132">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="0b100-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0b100-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="0b100-133">Namespace</span></span><br/> | <span data-ttu-id="0b100-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0b100-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0b100-135">組件</span><span class="sxs-lookup"><span data-stu-id="0b100-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0b100-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="0b100-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b100-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b100-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b100-138">**AxWindowsMediaPlayer (VB 和 c # ) 的緩衝事件**</span><span class="sxs-lookup"><span data-stu-id="0b100-138">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="0b100-139">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0b100-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





