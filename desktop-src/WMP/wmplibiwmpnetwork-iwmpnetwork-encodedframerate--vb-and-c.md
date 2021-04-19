---
title: IWMPNetwork encodedFrameRate 屬性
description: EncodedFrameRate 屬性會取得內容作者所指定的影片畫面播放速率。
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- encodedFrameRate 屬性 Windows Media Player
- encodedFrameRate 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，encodedFrameRate 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977396"
---
# <a name="iwmpnetworkencodedframerate-property"></a><span data-ttu-id="b9d88-106">IWMPNetwork：： encodedFrameRate 屬性</span><span class="sxs-lookup"><span data-stu-id="b9d88-106">IWMPNetwork::encodedFrameRate property</span></span>

<span data-ttu-id="b9d88-107">**EncodedFrameRate** 屬性會取得內容作者所指定的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="b9d88-107">The **encodedFrameRate** property gets the video frame rate specified by the content author.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d88-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9d88-108">Syntax</span></span>


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b9d88-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="b9d88-109">Property value</span></span>

<span data-ttu-id="b9d88-110">以每秒畫面格的編碼畫面播放速率 (fps) 的 **Int32。**</span><span class="sxs-lookup"><span data-stu-id="b9d88-110">A **System.Int32** that is the encoded frame rate in frames per second (fps).</span></span>

> [!Note]  
> <span data-ttu-id="b9d88-111">雖然 **encodedFrameRate** 屬性會測量每秒畫面格的編碼畫面播放速率，但 [ **幀** 速率] 屬性會測量目前的畫面播放速率（以每一百秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9d88-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b9d88-112">範例</span><span class="sxs-lookup"><span data-stu-id="b9d88-112">Examples</span></span>

<span data-ttu-id="b9d88-113">下列程式碼範例會使用 **encodedFrameRate** 來顯示編碼檔案時所指定的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="b9d88-113">The following code example uses **encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="b9d88-114">這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="b9d88-114">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="b9d88-115">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="b9d88-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b9d88-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9d88-116">Requirements</span></span>



| <span data-ttu-id="b9d88-117">需求</span><span class="sxs-lookup"><span data-stu-id="b9d88-117">Requirement</span></span> | <span data-ttu-id="b9d88-118">值</span><span class="sxs-lookup"><span data-stu-id="b9d88-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d88-119">版本</span><span class="sxs-lookup"><span data-stu-id="b9d88-119">Version</span></span><br/>   | <span data-ttu-id="b9d88-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b9d88-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b9d88-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9d88-121">Namespace</span></span><br/> | <span data-ttu-id="b9d88-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b9d88-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b9d88-123">組件</span><span class="sxs-lookup"><span data-stu-id="b9d88-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9d88-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b9d88-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d88-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9d88-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d88-126">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b9d88-126">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9d88-127">**(VB 和 c # 的 IWMPNetwork 幀 )**</span><span class="sxs-lookup"><span data-stu-id="b9d88-127">**IWMPNetwork.frameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





