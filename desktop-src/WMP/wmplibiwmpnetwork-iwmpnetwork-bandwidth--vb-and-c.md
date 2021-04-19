---
title: IWMPNetwork 頻寬屬性
description: 頻寬屬性會取得媒體專案目前的頻寬。
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- 頻寬屬性 Windows Media Player
- 頻寬屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，頻寬屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000011"
---
# <a name="iwmpnetworkbandwidth-property"></a><span data-ttu-id="919f7-106">IWMPNetwork：：頻寬屬性</span><span class="sxs-lookup"><span data-stu-id="919f7-106">IWMPNetwork::bandWidth property</span></span>

<span data-ttu-id="919f7-107">**頻寬** 屬性會取得媒體專案目前的頻寬。</span><span class="sxs-lookup"><span data-stu-id="919f7-107">The **bandWidth** property gets the current bandwidth of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="919f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="919f7-108">Syntax</span></span>


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="919f7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="919f7-109">Property value</span></span>

<span data-ttu-id="919f7-110">是頻寬的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="919f7-110">A **System.Int32** that is the bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="919f7-111">備註</span><span class="sxs-lookup"><span data-stu-id="919f7-111">Remarks</span></span>

<span data-ttu-id="919f7-112">如果未設定 URL，則透過 AxWindowsMediaPlayer 抓取的值將會是零 **。**</span><span class="sxs-lookup"><span data-stu-id="919f7-112">The value retrieved through **AxWindowsMediaPlayer.URL** will be zero if the URL is not set.</span></span> <span data-ttu-id="919f7-113">這個屬性只對串流媒體有效。</span><span class="sxs-lookup"><span data-stu-id="919f7-113">This property is valid only for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="919f7-114">範例</span><span class="sxs-lookup"><span data-stu-id="919f7-114">Examples</span></span>

<span data-ttu-id="919f7-115">下列範例會使用 **頻寬** 來顯示目前的媒體頻寬。</span><span class="sxs-lookup"><span data-stu-id="919f7-115">The following example uses **bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="919f7-116">這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="919f7-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="919f7-117">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="919f7-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
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

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="919f7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="919f7-118">Requirements</span></span>



| <span data-ttu-id="919f7-119">需求</span><span class="sxs-lookup"><span data-stu-id="919f7-119">Requirement</span></span> | <span data-ttu-id="919f7-120">值</span><span class="sxs-lookup"><span data-stu-id="919f7-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="919f7-121">版本</span><span class="sxs-lookup"><span data-stu-id="919f7-121">Version</span></span><br/>   | <span data-ttu-id="919f7-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="919f7-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="919f7-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="919f7-123">Namespace</span></span><br/> | <span data-ttu-id="919f7-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="919f7-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="919f7-125">組件</span><span class="sxs-lookup"><span data-stu-id="919f7-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="919f7-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="919f7-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="919f7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="919f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919f7-128">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="919f7-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="919f7-129">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="919f7-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





