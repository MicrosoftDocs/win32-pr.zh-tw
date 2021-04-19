---
title: IWMPNetwork 畫面播放速率屬性
description: '[畫面播放速率] 屬性會取得目前的影片畫面播放速率。'
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- 速率屬性 Windows Media Player
- IWMPNetwork 介面的畫面播放速率屬性 Windows Media Player
- IWMPNetwork 介面 Windows Media Player、畫面播放速率屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990515"
---
# <a name="iwmpnetworkframerate-property"></a><span data-ttu-id="44a93-106">IWMPNetwork：：幀屬性</span><span class="sxs-lookup"><span data-stu-id="44a93-106">IWMPNetwork::frameRate property</span></span>

<span data-ttu-id="44a93-107">[ **幀** 速率] 屬性會取得目前的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="44a93-107">The **frameRate** property gets the current video frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a93-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="44a93-108">Syntax</span></span>


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="44a93-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="44a93-109">Property value</span></span>

<span data-ttu-id="44a93-110">在每一百秒框架中的目前畫面播放速率的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="44a93-110">A **System.Int32** that is the current frame rate in frames per hundred seconds.</span></span>

> [!Note]  
> <span data-ttu-id="44a93-111">雖然 **encodedFrameRate** 屬性會測量每秒畫面格的編碼畫面播放速率，但 [ **幀** 速率] 屬性會測量目前的畫面播放速率（以每一百秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="44a93-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="44a93-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="44a93-112">See Remarks.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="44a93-113">備註</span><span class="sxs-lookup"><span data-stu-id="44a93-113">Remarks</span></span>

<span data-ttu-id="44a93-114">目前的畫面播放速率值會以每一百秒的框架傳回。</span><span class="sxs-lookup"><span data-stu-id="44a93-114">The current frame rate value is returned in frames per hundred seconds.</span></span> <span data-ttu-id="44a93-115">例如，值2998表示每秒29.98 個畫面 (fps) 。</span><span class="sxs-lookup"><span data-stu-id="44a93-115">For example, a value of 2998 indicates 29.98 frames per second (fps).</span></span>

## <a name="examples"></a><span data-ttu-id="44a93-116">範例</span><span class="sxs-lookup"><span data-stu-id="44a93-116">Examples</span></span>

<span data-ttu-id="44a93-117">下列程式碼範例會使用 **幀** 速率來顯示編碼檔案時所指定的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="44a93-117">The following code example uses **frameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="44a93-118">這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="44a93-118">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="44a93-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="44a93-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="44a93-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="44a93-120">Requirements</span></span>



| <span data-ttu-id="44a93-121">需求</span><span class="sxs-lookup"><span data-stu-id="44a93-121">Requirement</span></span> | <span data-ttu-id="44a93-122">值</span><span class="sxs-lookup"><span data-stu-id="44a93-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a93-123">版本</span><span class="sxs-lookup"><span data-stu-id="44a93-123">Version</span></span><br/>   | <span data-ttu-id="44a93-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="44a93-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="44a93-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="44a93-125">Namespace</span></span><br/> | <span data-ttu-id="44a93-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="44a93-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="44a93-127">組件</span><span class="sxs-lookup"><span data-stu-id="44a93-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="44a93-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="44a93-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44a93-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44a93-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a93-130">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="44a93-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="44a93-131">**IWMPNetwork. encodedFrameRate (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="44a93-131">**IWMPNetwork.encodedFrameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





