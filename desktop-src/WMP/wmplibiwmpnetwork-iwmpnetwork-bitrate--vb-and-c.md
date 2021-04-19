---
title: IWMPNetwork 位元速率屬性
description: 位元速率屬性會取得目前所接收的位元速率。
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- 位元速率屬性 Windows Media Player
- 位元速率屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，位元速率屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998732"
---
# <a name="iwmpnetworkbitrate-property"></a><span data-ttu-id="1005d-106">IWMPNetwork：：位元速率屬性</span><span class="sxs-lookup"><span data-stu-id="1005d-106">IWMPNetwork::bitRate property</span></span>

<span data-ttu-id="1005d-107">**位元速率** 屬性會取得目前所接收的位元速率。</span><span class="sxs-lookup"><span data-stu-id="1005d-107">The **bitRate** property gets the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="1005d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1005d-108">Syntax</span></span>


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="1005d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1005d-109">Property value</span></span>

<span data-ttu-id="1005d-110">位元速率的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="1005d-110">A **System.Int32** that is the bit rate.</span></span>

## <a name="remarks"></a><span data-ttu-id="1005d-111">備註</span><span class="sxs-lookup"><span data-stu-id="1005d-111">Remarks</span></span>

<span data-ttu-id="1005d-112">這個屬性的值是影片和音訊串流的位元速率組合。</span><span class="sxs-lookup"><span data-stu-id="1005d-112">The value of this property is a combination of the bit rates of both video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="1005d-113">範例</span><span class="sxs-lookup"><span data-stu-id="1005d-113">Examples</span></span>

<span data-ttu-id="1005d-114">下列範例會使用 **位元速率** 來顯示目前的媒體位元速率。</span><span class="sxs-lookup"><span data-stu-id="1005d-114">The following example uses **bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="1005d-115">這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="1005d-115">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="1005d-116">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="1005d-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1005d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1005d-117">Requirements</span></span>



| <span data-ttu-id="1005d-118">需求</span><span class="sxs-lookup"><span data-stu-id="1005d-118">Requirement</span></span> | <span data-ttu-id="1005d-119">值</span><span class="sxs-lookup"><span data-stu-id="1005d-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1005d-120">版本</span><span class="sxs-lookup"><span data-stu-id="1005d-120">Version</span></span><br/>   | <span data-ttu-id="1005d-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1005d-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1005d-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="1005d-122">Namespace</span></span><br/> | <span data-ttu-id="1005d-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1005d-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1005d-124">組件</span><span class="sxs-lookup"><span data-stu-id="1005d-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1005d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="1005d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1005d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1005d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1005d-127">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1005d-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





