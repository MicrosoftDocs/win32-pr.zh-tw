---
title: IWMPControls stop 方法
description: Stop 方法會停止播放媒體專案。 |IWMPControls stop 方法
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- stop 方法 Windows Media Player
- stop 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，stop 方法
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999388"
---
# <a name="iwmpcontrolsstop-method"></a><span data-ttu-id="f4561-107">IWMPControls：： stop 方法</span><span class="sxs-lookup"><span data-stu-id="f4561-107">IWMPControls::stop method</span></span>

<span data-ttu-id="f4561-108">**Stop** 方法會停止播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f4561-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4561-109">語法</span><span class="sxs-lookup"><span data-stu-id="f4561-109">Syntax</span></span>


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a><span data-ttu-id="f4561-110">參數</span><span class="sxs-lookup"><span data-stu-id="f4561-110">Parameters</span></span>

<span data-ttu-id="f4561-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f4561-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4561-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4561-112">Return value</span></span>

<span data-ttu-id="f4561-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f4561-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4561-114">備註</span><span class="sxs-lookup"><span data-stu-id="f4561-114">Remarks</span></span>

<span data-ttu-id="f4561-115">這個方法會使 Windows Media Player 釋出它所使用的任何系統資源，例如音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="f4561-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="f4561-116">但目前的媒體專案則不會釋出。</span><span class="sxs-lookup"><span data-stu-id="f4561-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="f4561-117">當 Windows Media Player 停止時，媒體專案中目前的播放位置會重設為專案的開頭。</span><span class="sxs-lookup"><span data-stu-id="f4561-117">When Windows Media Player is stopped, the current playback position in the media item is reset to the beginning of the item.</span></span> <span data-ttu-id="f4561-118">接著呼叫 **IWMPControls** ，就會開始從媒體專案的開頭播放。</span><span class="sxs-lookup"><span data-stu-id="f4561-118">Subsequently calling **IWMPControls.play** will start playback from the beginning of the media item.</span></span> <span data-ttu-id="f4561-119">若要停止播放作業而不變更目前的位置，請使用 **IWMPControls** 方法。</span><span class="sxs-lookup"><span data-stu-id="f4561-119">To halt a play operation without changing the current position, use the **IWMPControls.pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="f4561-120">範例</span><span class="sxs-lookup"><span data-stu-id="f4561-120">Examples</span></span>

<span data-ttu-id="f4561-121">下列範例會使用 [ **停止** ] 來停止目前的媒體專案，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="f4561-121">The following example uses **stop** to stop the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="f4561-122">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="f4561-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f4561-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4561-123">Requirements</span></span>



| <span data-ttu-id="f4561-124">需求</span><span class="sxs-lookup"><span data-stu-id="f4561-124">Requirement</span></span> | <span data-ttu-id="f4561-125">值</span><span class="sxs-lookup"><span data-stu-id="f4561-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4561-126">版本</span><span class="sxs-lookup"><span data-stu-id="f4561-126">Version</span></span><br/>   | <span data-ttu-id="f4561-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f4561-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f4561-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="f4561-128">Namespace</span></span><br/> | <span data-ttu-id="f4561-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f4561-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f4561-130">組件</span><span class="sxs-lookup"><span data-stu-id="f4561-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f4561-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="f4561-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4561-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4561-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4561-133">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4561-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4561-134">**IWMPControls：接下來 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4561-134">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4561-135">**IWMPControls： pause (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4561-135">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4561-136">**IWMPControls (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4561-136">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4561-137">**IWMPControls 之前 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4561-137">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





