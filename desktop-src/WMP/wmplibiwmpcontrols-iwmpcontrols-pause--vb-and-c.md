---
title: IWMPControls pause 方法
description: Pause 方法會暫停播放媒體專案。 |IWMPControls pause 方法
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- pause 方法 Windows Media Player
- pause 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，pause 方法
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998640"
---
# <a name="iwmpcontrolspause-method"></a><span data-ttu-id="a4f22-107">IWMPControls：:p ause 方法</span><span class="sxs-lookup"><span data-stu-id="a4f22-107">IWMPControls::pause method</span></span>

<span data-ttu-id="a4f22-108">**Pause** 方法會暫停播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="a4f22-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f22-109">語法</span><span class="sxs-lookup"><span data-stu-id="a4f22-109">Syntax</span></span>


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a><span data-ttu-id="a4f22-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4f22-110">Parameters</span></span>

<span data-ttu-id="a4f22-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a4f22-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4f22-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4f22-112">Return value</span></span>

<span data-ttu-id="a4f22-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a4f22-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f22-114">備註</span><span class="sxs-lookup"><span data-stu-id="a4f22-114">Remarks</span></span>

<span data-ttu-id="a4f22-115">當檔案暫停時，Windows Media Player 不會提供任何系統資源，例如音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="a4f22-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="a4f22-116">若要判斷特定媒體類型是否可以暫停，請將 **system.string** 值 "pause" 傳遞給 **IWMPControls. isAvailable** 屬性， (c # ) 中的 **IWMPControls. get \_ isAvailable** 方法。</span><span class="sxs-lookup"><span data-stu-id="a4f22-116">To determine whether a particular media type can be paused, pass the **System.String** value "pause" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="a4f22-117">範例</span><span class="sxs-lookup"><span data-stu-id="a4f22-117">Examples</span></span>

<span data-ttu-id="a4f22-118">下列範例會使用 **pause** 來暫停播放目前媒體專案，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="a4f22-118">The following example uses **pause** to pause playback of the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="a4f22-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="a4f22-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a4f22-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4f22-120">Requirements</span></span>



| <span data-ttu-id="a4f22-121">需求</span><span class="sxs-lookup"><span data-stu-id="a4f22-121">Requirement</span></span> | <span data-ttu-id="a4f22-122">值</span><span class="sxs-lookup"><span data-stu-id="a4f22-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f22-123">版本</span><span class="sxs-lookup"><span data-stu-id="a4f22-123">Version</span></span><br/>   | <span data-ttu-id="a4f22-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a4f22-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a4f22-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4f22-125">Namespace</span></span><br/> | <span data-ttu-id="a4f22-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a4f22-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a4f22-127">組件</span><span class="sxs-lookup"><span data-stu-id="a4f22-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a4f22-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a4f22-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f22-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4f22-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f22-130">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a4f22-130">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4f22-131">**IWMPControls. isAvailable (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a4f22-131">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





