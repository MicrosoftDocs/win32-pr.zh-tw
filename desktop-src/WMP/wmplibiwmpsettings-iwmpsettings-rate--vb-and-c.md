---
title: IWMPSettings rate 屬性
description: Rate 屬性可取得或設定影片目前的播放速率。
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- rate 屬性 Windows Media Player
- rate 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，速率屬性
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978636"
---
# <a name="iwmpsettingsrate-property"></a><span data-ttu-id="69dcb-106">IWMPSettings：： rate 屬性</span><span class="sxs-lookup"><span data-stu-id="69dcb-106">IWMPSettings::rate property</span></span>

<span data-ttu-id="69dcb-107">**Rate** 屬性可取得或設定影片目前的播放速率。</span><span class="sxs-lookup"><span data-stu-id="69dcb-107">The **rate** property gets or sets the current playback rate for video.</span></span>

## <a name="syntax"></a><span data-ttu-id="69dcb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="69dcb-108">Syntax</span></span>


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a><span data-ttu-id="69dcb-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="69dcb-109">Property value</span></span>

<span data-ttu-id="69dcb-110">這是播放速率的 **雙精度浮點數** ，預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="69dcb-110">A **System.Double** that is the playback rate, with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="69dcb-111">備註</span><span class="sxs-lookup"><span data-stu-id="69dcb-111">Remarks</span></span>

<span data-ttu-id="69dcb-112">這個屬性所抓取的值會作為乘數值，讓您以更快或較慢的速率播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="69dcb-112">The value retrieved by this property acts as a multiplier value that enables you to play a media item at a faster or slower rate.</span></span> <span data-ttu-id="69dcb-113">預設值1.0 表示撰寫的速度。</span><span class="sxs-lookup"><span data-stu-id="69dcb-113">The default value of 1.0 indicates the authored speed.</span></span>

<span data-ttu-id="69dcb-114">請注意，在低於0.5 或高於1.5 的速率中，音訊播放軌會變得很難理解。</span><span class="sxs-lookup"><span data-stu-id="69dcb-114">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="69dcb-115">播放速率2表示正常播放速度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="69dcb-115">A playback rate of 2 indicates twice the normal playback speed.</span></span>

<span data-ttu-id="69dcb-116">Windows Media Player 將嘗試使用下列四種不同播放模式的最有效方式</span><span class="sxs-lookup"><span data-stu-id="69dcb-116">Windows Media Player will attempt to use the most effective of the following four different playback modes</span></span>

-   <span data-ttu-id="69dcb-117">維持音訊音調的流暢播放影片</span><span class="sxs-lookup"><span data-stu-id="69dcb-117">Smooth video playback with audio pitch maintained</span></span>
-   <span data-ttu-id="69dcb-118">不維持音訊音調的流暢播放影片</span><span class="sxs-lookup"><span data-stu-id="69dcb-118">Smooth video playback with audio pitch not maintained</span></span>
-   <span data-ttu-id="69dcb-119">無音訊的流暢播放影片</span><span class="sxs-lookup"><span data-stu-id="69dcb-119">Smooth video playback with no audio</span></span>
-   <span data-ttu-id="69dcb-120">沒有音訊的主要畫面格影片播放</span><span class="sxs-lookup"><span data-stu-id="69dcb-120">Keyframe video playback with no audio</span></span>

<span data-ttu-id="69dcb-121">Windows Media Player 選擇的模式取決於許多因素，包括檔案類型和位置、作業系統、網路和伺服器。</span><span class="sxs-lookup"><span data-stu-id="69dcb-121">The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="69dcb-122">其他考慮也適用，視用來建立內容的數位媒體格式而定：</span><span class="sxs-lookup"><span data-stu-id="69dcb-122">Other considerations apply as well, depending on the digital media format used to create the content:</span></span>

-   <span data-ttu-id="69dcb-123">**Windows Media 視訊 (WMV) 和 ASF。**</span><span class="sxs-lookup"><span data-stu-id="69dcb-123">**Windows Media Video (WMV) and ASF.**</span></span> <span data-ttu-id="69dcb-124">**速率** 屬性的最佳值是從1到10，或從1到10以進行反向播放。</span><span class="sxs-lookup"><span data-stu-id="69dcb-124">Optimal values for the **rate** property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="69dcb-125">從0.5 到1.0 或從-0.5 到-1.0 的值可能也適用于可以維持音訊音調的情況，例如播放位於本機電腦上的檔案時。</span><span class="sxs-lookup"><span data-stu-id="69dcb-125">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer.</span></span> <span data-ttu-id="69dcb-126">允許絕對值大於10的值，但沒有什麼意義。</span><span class="sxs-lookup"><span data-stu-id="69dcb-126">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="69dcb-127">**其他影片格式。**</span><span class="sxs-lookup"><span data-stu-id="69dcb-127">**Other video formats.**</span></span> <span data-ttu-id="69dcb-128">**Rate** 屬性的範圍可以從0到9。</span><span class="sxs-lookup"><span data-stu-id="69dcb-128">The **rate** property can range from 0 to 9.</span></span> <span data-ttu-id="69dcb-129">不允許負數值。</span><span class="sxs-lookup"><span data-stu-id="69dcb-129">Negative values are not allowed.</span></span> <span data-ttu-id="69dcb-130">小於1的值表示緩慢的移動。</span><span class="sxs-lookup"><span data-stu-id="69dcb-130">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="69dcb-131">允許超過9個值，但沒有什麼意義。</span><span class="sxs-lookup"><span data-stu-id="69dcb-131">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="69dcb-132">**IWMPControls. fastForward** 方法會將 **速率** 的值變更為5.0，而 **IWMPControls. fastReverse** 方法會將 **速率** 的值變更為5.0。</span><span class="sxs-lookup"><span data-stu-id="69dcb-132">The **IWMPControls.fastForward** method changes the value of **rate** to 5.0, while the **IWMPControls.fastReverse** method changes the value of **rate** to  5.0.</span></span>

<span data-ttu-id="69dcb-133">某些數位媒體格式的播放速率無法改變。</span><span class="sxs-lookup"><span data-stu-id="69dcb-133">The playback rate of some digital media formats cannot be altered.</span></span> <span data-ttu-id="69dcb-134">使用 c # 中的 **IWMPSettings. isAvailable** 屬性 (**IWMPSettings. get \_ isAvailable** 方法) 來找出是否可以針對特定媒體專案指定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="69dcb-134">Use the **IWMPSettings.isAvailable** property (In C# the **IWMPSettings.get\_isAvailable** method) to discover whether this property can be specified for a particular media item.</span></span>

## <a name="examples"></a><span data-ttu-id="69dcb-135">範例</span><span class="sxs-lookup"><span data-stu-id="69dcb-135">Examples</span></span>

<span data-ttu-id="69dcb-136">下列範例使用數值上下按鈕控制項，可讓使用者變更目前媒體的播放速度。</span><span class="sxs-lookup"><span data-stu-id="69dcb-136">The following example uses a numeric updown control that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="69dcb-137">當使用者按一下控制項的向上或向下箭號時，[ **速率** ] 屬性會設定為新的值。</span><span class="sxs-lookup"><span data-stu-id="69dcb-137">When the user clicks the up or down arrows of the control, the **rate** property is set to the new value.</span></span> <span data-ttu-id="69dcb-138">控制項中的可能值範圍為 0.5 (半高速) 至 2.0 (雙速度) 。</span><span class="sxs-lookup"><span data-stu-id="69dcb-138">The possible range of values in the control are 0.5 (half-speed) to 2.0 (double-speed).</span></span> <span data-ttu-id="69dcb-139">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="69dcb-139">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="69dcb-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="69dcb-140">Requirements</span></span>



| <span data-ttu-id="69dcb-141">需求</span><span class="sxs-lookup"><span data-stu-id="69dcb-141">Requirement</span></span> | <span data-ttu-id="69dcb-142">值</span><span class="sxs-lookup"><span data-stu-id="69dcb-142">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69dcb-143">版本</span><span class="sxs-lookup"><span data-stu-id="69dcb-143">Version</span></span><br/>   | <span data-ttu-id="69dcb-144">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="69dcb-144">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="69dcb-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="69dcb-145">Namespace</span></span><br/> | <span data-ttu-id="69dcb-146">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="69dcb-146">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="69dcb-147">組件</span><span class="sxs-lookup"><span data-stu-id="69dcb-147">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69dcb-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="69dcb-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69dcb-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69dcb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69dcb-150">**IWMPControls. fastForward (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69dcb-150">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69dcb-151">**IWMPControls. fastReverse (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69dcb-151">**IWMPControls.fastReverse (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69dcb-152">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69dcb-152">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69dcb-153">**IWMPSettings. isAvailable (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69dcb-153">**IWMPSettings.isAvailable (VB and C#)**</span></span>](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69dcb-154">**IWMPSettings (VB 和 c # ) 靜音**</span><span class="sxs-lookup"><span data-stu-id="69dcb-154">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





