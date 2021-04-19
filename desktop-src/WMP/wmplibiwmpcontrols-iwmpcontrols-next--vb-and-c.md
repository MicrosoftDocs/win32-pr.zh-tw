---
title: IWMPControls next 方法
description: 下一個方法會將播放清單中的下一個專案設定為目前的專案。
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- next 方法 Windows Media Player
- next 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player、next 方法
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984842"
---
# <a name="iwmpcontrolsnext-method"></a><span data-ttu-id="6db30-106">IWMPControls：： next 方法</span><span class="sxs-lookup"><span data-stu-id="6db30-106">IWMPControls::next method</span></span>

<span data-ttu-id="6db30-107">**下一個** 方法會將播放清單中的下一個專案設定為目前的專案。</span><span class="sxs-lookup"><span data-stu-id="6db30-107">The **next** method sets the next item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db30-108">語法</span><span class="sxs-lookup"><span data-stu-id="6db30-108">Syntax</span></span>


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a><span data-ttu-id="6db30-109">參數</span><span class="sxs-lookup"><span data-stu-id="6db30-109">Parameters</span></span>

<span data-ttu-id="6db30-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6db30-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6db30-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6db30-111">Return value</span></span>

<span data-ttu-id="6db30-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6db30-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6db30-113">備註</span><span class="sxs-lookup"><span data-stu-id="6db30-113">Remarks</span></span>

<span data-ttu-id="6db30-114">如果叫用 [ **下一步]** 時，播放清單是最後一個專案，播放清單中的第一個專案就會成為目前的專案。</span><span class="sxs-lookup"><span data-stu-id="6db30-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="6db30-115">針對伺服器端播放清單，這個方法會跳至伺服器端播放清單中的下一個專案，而不是用戶端播放清單。</span><span class="sxs-lookup"><span data-stu-id="6db30-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="6db30-116">播放 DVD 時，此方法會跳到播放順序中的下一個邏輯章節，這可能不是播放清單中的下一章。</span><span class="sxs-lookup"><span data-stu-id="6db30-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="6db30-117">播放 DVD 的靜止影像時，此方法會跳到下一個影像。</span><span class="sxs-lookup"><span data-stu-id="6db30-117">When playing DVD still images, this method skips to the next image.</span></span>

## <a name="examples"></a><span data-ttu-id="6db30-118">範例</span><span class="sxs-lookup"><span data-stu-id="6db30-118">Examples</span></span>

<span data-ttu-id="6db30-119">下列範例會使用 **[下一步]** 移至目前播放清單中的下一個專案，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="6db30-119">The following example uses **next** to move to the next item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="6db30-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="6db30-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6db30-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6db30-121">Requirements</span></span>



| <span data-ttu-id="6db30-122">需求</span><span class="sxs-lookup"><span data-stu-id="6db30-122">Requirement</span></span> | <span data-ttu-id="6db30-123">值</span><span class="sxs-lookup"><span data-stu-id="6db30-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db30-124">版本</span><span class="sxs-lookup"><span data-stu-id="6db30-124">Version</span></span><br/>   | <span data-ttu-id="6db30-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6db30-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6db30-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="6db30-126">Namespace</span></span><br/> | <span data-ttu-id="6db30-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6db30-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6db30-128">組件</span><span class="sxs-lookup"><span data-stu-id="6db30-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6db30-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6db30-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db30-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6db30-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db30-131">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6db30-131">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6db30-132">**IWMPControls 之前 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6db30-132">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6db30-133">**IWMPControls。停止 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6db30-133">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





