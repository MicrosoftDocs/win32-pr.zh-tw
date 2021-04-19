---
title: IWMPControls play 方法
description: Play 方法會開始播放目前的媒體專案，或繼續播放暫停的專案。
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- play 方法 Windows Media Player
- play 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player、play 方法
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987939"
---
# <a name="iwmpcontrolsplay-method"></a><span data-ttu-id="272dd-106">IWMPControls：:p 排放方法</span><span class="sxs-lookup"><span data-stu-id="272dd-106">IWMPControls::play method</span></span>

<span data-ttu-id="272dd-107">**Play** 方法會開始播放目前的媒體專案，或繼續播放暫停的專案。</span><span class="sxs-lookup"><span data-stu-id="272dd-107">The **play** method begins playback of the current media item, or resumes playback of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="272dd-108">語法</span><span class="sxs-lookup"><span data-stu-id="272dd-108">Syntax</span></span>


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a><span data-ttu-id="272dd-109">參數</span><span class="sxs-lookup"><span data-stu-id="272dd-109">Parameters</span></span>

<span data-ttu-id="272dd-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="272dd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="272dd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="272dd-111">Return value</span></span>

<span data-ttu-id="272dd-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="272dd-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="272dd-113">備註</span><span class="sxs-lookup"><span data-stu-id="272dd-113">Remarks</span></span>

<span data-ttu-id="272dd-114">如果在快速轉送或倒轉時呼叫這個方法，則播放速率 () **IWMPSettings** 的值會設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="272dd-114">If this method is called while fast-forwarding or rewinding, the rate of playback (the value of **IWMPSettings.rate**) is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="272dd-115">範例</span><span class="sxs-lookup"><span data-stu-id="272dd-115">Examples</span></span>

<span data-ttu-id="272dd-116">下列範例會使用 **播放** 來播放目前的媒體專案，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="272dd-116">The following example uses **play** to play the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="272dd-117">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="272dd-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="272dd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="272dd-118">Requirements</span></span>



| <span data-ttu-id="272dd-119">需求</span><span class="sxs-lookup"><span data-stu-id="272dd-119">Requirement</span></span> | <span data-ttu-id="272dd-120">值</span><span class="sxs-lookup"><span data-stu-id="272dd-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="272dd-121">版本</span><span class="sxs-lookup"><span data-stu-id="272dd-121">Version</span></span><br/>   | <span data-ttu-id="272dd-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="272dd-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="272dd-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="272dd-123">Namespace</span></span><br/> | <span data-ttu-id="272dd-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="272dd-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="272dd-125">組件</span><span class="sxs-lookup"><span data-stu-id="272dd-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="272dd-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="272dd-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="272dd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="272dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="272dd-128">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="272dd-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="272dd-129">**IWMPControls. playItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="272dd-129">**IWMPControls.playItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="272dd-130">**IWMPSettings (VB 和 c # 的速率 )**</span><span class="sxs-lookup"><span data-stu-id="272dd-130">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





