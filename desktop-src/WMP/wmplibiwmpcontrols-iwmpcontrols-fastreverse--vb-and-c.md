---
title: IWMPControls fastReverse 方法
description: FastReverse 方法會以反向方向啟動媒體專案的快速播放。
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- fastReverse 方法 Windows Media Player
- fastReverse 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，fastReverse 方法
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998676"
---
# <a name="iwmpcontrolsfastreverse-method"></a><span data-ttu-id="d79a6-106">IWMPControls：： fastReverse 方法</span><span class="sxs-lookup"><span data-stu-id="d79a6-106">IWMPControls::fastReverse method</span></span>

<span data-ttu-id="d79a6-107">**FastReverse** 方法會以反向方向啟動媒體專案的快速播放。</span><span class="sxs-lookup"><span data-stu-id="d79a6-107">The **fastReverse** method starts fast play of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="d79a6-108">語法</span><span class="sxs-lookup"><span data-stu-id="d79a6-108">Syntax</span></span>


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a><span data-ttu-id="d79a6-109">參數</span><span class="sxs-lookup"><span data-stu-id="d79a6-109">Parameters</span></span>

<span data-ttu-id="d79a6-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d79a6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d79a6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d79a6-111">Return value</span></span>

<span data-ttu-id="d79a6-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d79a6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d79a6-113">備註</span><span class="sxs-lookup"><span data-stu-id="d79a6-113">Remarks</span></span>

<span data-ttu-id="d79a6-114">**FastReverse** 方法會以正常速度的五倍反向掃描剪輯，如果是影片檔案，則只會顯示主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="d79a6-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="d79a6-115">呼叫 **fastReverse** 相當於藉由設定 **IWMPSettings 的速率** 屬性，為速率指定-5.0。</span><span class="sxs-lookup"><span data-stu-id="d79a6-115">Calling **fastReverse** is equivalent to specifying -5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="d79a6-116">如果後續的速率有所變更，或呼叫 **IWMPControls** 或 **IWMPControls** ，Windows Media Player 將會停止快速反轉。</span><span class="sxs-lookup"><span data-stu-id="d79a6-116">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="d79a6-117">如果專案是播放清單的一部分， **fastReverse** 就會在目前的播放軌開始時停止。比方說，如果 track 3 是在 **fastReverse** 中，當到達 track 3 的開頭時，Windows Media Player 將不會移至「追蹤2」。</span><span class="sxs-lookup"><span data-stu-id="d79a6-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="d79a6-118">呼叫 **fastReverse** 時，播放次數不會遞增。</span><span class="sxs-lookup"><span data-stu-id="d79a6-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="d79a6-119">如果您在 **fastReverse** 執行時呼叫 **IWMPControls fastForward** ， **fastReverse** 將會停止，而且 **IWMPControls** 將會開始。</span><span class="sxs-lookup"><span data-stu-id="d79a6-119">If you call **IWMPControls.fastForward** while **fastReverse** is running, **fastReverse** will be stopped and **IWMPControls.fastForward** will begin.</span></span>

<span data-ttu-id="d79a6-120">這個方法不適用於即時廣播和某些數位媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d79a6-120">This method does not work for live broadcasts and certain digital media types.</span></span> <span data-ttu-id="d79a6-121">若要判斷您是否可以在剪輯中使用快速反轉，請將 **system.string** 值 "FastReverse" 傳遞給 **IWMPControls. isAvailable** 屬性， (**IWMPControls. Get \_ isAvailable** 方法（c # ) ）。</span><span class="sxs-lookup"><span data-stu-id="d79a6-121">To determine whether you can use fast reverse in a clip, pass the **System.String** value "FastReverse" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="d79a6-122">範例</span><span class="sxs-lookup"><span data-stu-id="d79a6-122">Examples</span></span>

<span data-ttu-id="d79a6-123">下列範例會使用 **fastReverse** 來反轉目前的媒體專案，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="d79a6-123">The following example uses **fastReverse** to reverse the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="d79a6-124">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="d79a6-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d79a6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d79a6-125">Requirements</span></span>



| <span data-ttu-id="d79a6-126">需求</span><span class="sxs-lookup"><span data-stu-id="d79a6-126">Requirement</span></span> | <span data-ttu-id="d79a6-127">值</span><span class="sxs-lookup"><span data-stu-id="d79a6-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d79a6-128">版本</span><span class="sxs-lookup"><span data-stu-id="d79a6-128">Version</span></span><br/>   | <span data-ttu-id="d79a6-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d79a6-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d79a6-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="d79a6-130">Namespace</span></span><br/> | <span data-ttu-id="d79a6-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d79a6-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d79a6-132">組件</span><span class="sxs-lookup"><span data-stu-id="d79a6-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d79a6-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d79a6-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d79a6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d79a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d79a6-135">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d79a6-135">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d79a6-136">**IWMPControls. fastForward (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d79a6-136">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d79a6-137">**IWMPControls. isAvailable (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d79a6-137">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d79a6-138">**IWMPControls (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d79a6-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d79a6-139">**IWMPControls。停止 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d79a6-139">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d79a6-140">**IWMPSettings (VB 和 c # 的速率 )**</span><span class="sxs-lookup"><span data-stu-id="d79a6-140">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





