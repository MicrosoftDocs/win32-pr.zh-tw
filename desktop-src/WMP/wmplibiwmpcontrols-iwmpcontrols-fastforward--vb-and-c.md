---
title: IWMPControls fastForward 方法
description: FastForward 方法會以正向方向啟動媒體專案的快速播放。 |IWMPControls fastForward 方法
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- fastForward 方法 Windows Media Player
- fastForward 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，fastForward 方法
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978484"
---
# <a name="iwmpcontrolsfastforward-method"></a><span data-ttu-id="b8942-107">IWMPControls：： fastForward 方法</span><span class="sxs-lookup"><span data-stu-id="b8942-107">IWMPControls::fastForward method</span></span>

<span data-ttu-id="b8942-108">**FastForward** 方法會以正向方向啟動媒體專案的快速播放。</span><span class="sxs-lookup"><span data-stu-id="b8942-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8942-109">語法</span><span class="sxs-lookup"><span data-stu-id="b8942-109">Syntax</span></span>


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a><span data-ttu-id="b8942-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8942-110">Parameters</span></span>

<span data-ttu-id="b8942-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b8942-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8942-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8942-112">Return value</span></span>

<span data-ttu-id="b8942-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b8942-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8942-114">備註</span><span class="sxs-lookup"><span data-stu-id="b8942-114">Remarks</span></span>

<span data-ttu-id="b8942-115">**FastForward** 方法會以正常速度的五倍來播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="b8942-115">The **fastForward** method plays the clip at five times the normal speed.</span></span> <span data-ttu-id="b8942-116">呼叫 **fastForward** 相當於藉由設定 **IWMPSettings 的速率** 屬性來指定5.0 的速率。</span><span class="sxs-lookup"><span data-stu-id="b8942-116">Calling **fastForward** is equivalent to specifying 5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="b8942-117">如果後續的速率有所變更，或呼叫 **IWMPControls** 或 **IWMPControls** ，Windows Media Player 將會停止快速轉送。</span><span class="sxs-lookup"><span data-stu-id="b8942-117">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="b8942-118">**FastForward** 方法不適用於即時廣播和特定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b8942-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="b8942-119">若要判斷您是否可以在剪輯中向前快轉，請將 **system.string** 值 "FastForward" 傳遞給 **IWMPControls. isAvailable** 屬性， (**IWMPControls. Get \_ isAvailable** 方法 in c # ) 。</span><span class="sxs-lookup"><span data-stu-id="b8942-119">To determine whether you can fast forward in a clip, pass the **System.String** value "FastForward" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="b8942-120">範例</span><span class="sxs-lookup"><span data-stu-id="b8942-120">Examples</span></span>

<span data-ttu-id="b8942-121">下列範例會使用 **fastForward** 來向前快轉目前的媒體專案，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="b8942-121">The following example uses **fastForward** to fast-forward the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="b8942-122">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="b8942-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b8942-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8942-123">Requirements</span></span>



| <span data-ttu-id="b8942-124">需求</span><span class="sxs-lookup"><span data-stu-id="b8942-124">Requirement</span></span> | <span data-ttu-id="b8942-125">值</span><span class="sxs-lookup"><span data-stu-id="b8942-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8942-126">版本</span><span class="sxs-lookup"><span data-stu-id="b8942-126">Version</span></span><br/>   | <span data-ttu-id="b8942-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b8942-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b8942-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8942-128">Namespace</span></span><br/> | <span data-ttu-id="b8942-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b8942-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b8942-130">組件</span><span class="sxs-lookup"><span data-stu-id="b8942-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8942-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b8942-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8942-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8942-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8942-133">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8942-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8942-134">**IWMPControls. isAvailable (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8942-134">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8942-135">**IWMPControls (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8942-135">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8942-136">**IWMPControls。停止 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8942-136">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8942-137">**IWMPSettings (VB 和 c # 的速率 )**</span><span class="sxs-lookup"><span data-stu-id="b8942-137">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





