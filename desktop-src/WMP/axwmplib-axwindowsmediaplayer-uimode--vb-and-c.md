---
title: AxWindowsMediaPlayer. uiMode 屬性
description: UiMode 屬性會取得或設定值，指出使用者介面中顯示的控制項。
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- uiMode 屬性 Windows Media Player
- uiMode 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，uiMode 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996224"
---
# <a name="axwindowsmediaplayeruimode-property"></a><span data-ttu-id="95405-106">AxWindowsMediaPlayer. uiMode 屬性</span><span class="sxs-lookup"><span data-stu-id="95405-106">AxWindowsMediaPlayer.uiMode property</span></span>

<span data-ttu-id="95405-107">UiMode 屬性會取得或設定值，指出使用者介面中顯示的控制項。</span><span class="sxs-lookup"><span data-stu-id="95405-107">The uiMode property gets or sets a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="95405-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95405-108">Syntax</span></span>


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a><span data-ttu-id="95405-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="95405-109">Property value</span></span>

<span data-ttu-id="95405-110">System.string，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="95405-110">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="95405-111">值</span><span class="sxs-lookup"><span data-stu-id="95405-111">Value</span></span>     | <span data-ttu-id="95405-112">描述</span><span class="sxs-lookup"><span data-stu-id="95405-112">Description</span></span>                                                                                                                                                                                                     | <span data-ttu-id="95405-113">音訊範例</span><span class="sxs-lookup"><span data-stu-id="95405-113">Audio example</span></span>                                                   | <span data-ttu-id="95405-114">影片範例</span><span class="sxs-lookup"><span data-stu-id="95405-114">Video example</span></span>                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="95405-115">不可見的</span><span class="sxs-lookup"><span data-stu-id="95405-115">invisible</span></span> | <span data-ttu-id="95405-116">Windows Media Player 內嵌時，不會有任何可見的使用者介面 (控制項、影片或視覺效果視窗) 。</span><span class="sxs-lookup"><span data-stu-id="95405-116">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                  | <span data-ttu-id="95405-117"> (不會顯示任何內容。 ) </span><span class="sxs-lookup"><span data-stu-id="95405-117">(Nothing is displayed.)</span></span>                                         | <span data-ttu-id="95405-118"> (不會顯示任何內容。 ) </span><span class="sxs-lookup"><span data-stu-id="95405-118">(Nothing is displayed.)</span></span>                                         |
| <span data-ttu-id="95405-119">無</span><span class="sxs-lookup"><span data-stu-id="95405-119">none</span></span>      | <span data-ttu-id="95405-120">Windows Media Player 內嵌時沒有控制項，而且只會顯示 [影片] 或 [視覺效果] 視窗。</span><span class="sxs-lookup"><span data-stu-id="95405-120">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                   | ![uimode = 具有音訊的 ' none '](images/uimode-none-audio-v11.png) | ![uimode = 含影片的 ' none '](images/uimode-none-video-v11.png) |
| <span data-ttu-id="95405-123">迷你</span><span class="sxs-lookup"><span data-stu-id="95405-123">mini</span></span>      | <span data-ttu-id="95405-124">除了 [影片] 或 [視覺效果] 視窗之外，Windows Media Player 還會以狀態視窗、播放/暫停、停止、靜音和音量控制項來內嵌。</span><span class="sxs-lookup"><span data-stu-id="95405-124">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                    | ![uimode = 具有音訊的 ' 迷你 '](images/uimode-mini-audio-v11.png) | ![uimode = 影片的 ' 迷你 '](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="95405-127">完整</span><span class="sxs-lookup"><span data-stu-id="95405-127">full</span></span>      | <span data-ttu-id="95405-128">預設值。</span><span class="sxs-lookup"><span data-stu-id="95405-128">Default.</span></span> <span data-ttu-id="95405-129">除了影片或視覺效果視窗之外，Windows Media Player 內嵌了狀態視窗、搜尋列、播放/暫停、停止、靜音、下、上、向前、向前、倒轉和音量控制項。</span><span class="sxs-lookup"><span data-stu-id="95405-129">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, rewind, and volume controls in addition to the video or visualization window.</span></span> | ![uimode = 具有音訊的 ' full '](images/uimode-full-audio-v11.png) | ![uimode = 「full」影片](images/uimode-full-video-v11.png) |
| <span data-ttu-id="95405-132">自訂</span><span class="sxs-lookup"><span data-stu-id="95405-132">custom</span></span>    | <span data-ttu-id="95405-133">Windows Media Player 內嵌自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="95405-133">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="95405-134">只能在 c + + 程式中使用。</span><span class="sxs-lookup"><span data-stu-id="95405-134">Can only be used in C++ programs.</span></span>                                                                                                                | <span data-ttu-id="95405-135"> (的自訂使用者介面隨即顯示。 ) </span><span class="sxs-lookup"><span data-stu-id="95405-135">(Custom user interface is displayed.)</span></span>                           | <span data-ttu-id="95405-136"> (的自訂使用者介面隨即顯示。 ) </span><span class="sxs-lookup"><span data-stu-id="95405-136">(Custom user interface is displayed.)</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="95405-137">備註</span><span class="sxs-lookup"><span data-stu-id="95405-137">Remarks</span></span>

<span data-ttu-id="95405-138">這個屬性會指定內嵌 Windows Media Player 的外觀。</span><span class="sxs-lookup"><span data-stu-id="95405-138">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="95405-139">當 **uiMode** 設定為「無」、「迷你」或「完整」時，顯示影片剪輯和音訊視覺效果的視窗就會出現。</span><span class="sxs-lookup"><span data-stu-id="95405-139">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="95405-140">您可以將 **物件** 標記的 **height** 屬性設為40（從底部測量），並將使用者介面的控制項部分保持可見，以將此視窗隱藏在迷你或完整模式中。</span><span class="sxs-lookup"><span data-stu-id="95405-140">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="95405-141">如果沒有想要的內嵌介面，請將 [ **寬度** ] 和 [ **高度** ] 屬性都設定為零。</span><span class="sxs-lookup"><span data-stu-id="95405-141">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="95405-142">如果 **uiMode** 設為「隱藏」，則不會顯示任何使用者介面，但在頁面上的空間仍會保留在 **寬度** 和 **高度** 所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="95405-142">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="95405-143">這適用于在 **uiMode** 可以變更時保留頁面配置。</span><span class="sxs-lookup"><span data-stu-id="95405-143">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="95405-144">此外，保留的空間是透明的，因此會顯示控制項背後的任何元素。</span><span class="sxs-lookup"><span data-stu-id="95405-144">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="95405-145">如果 **uiMode** 設定為「完整」或「迷你」，Windows Media Player 會以全螢幕模式顯示傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="95405-145">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="95405-146">如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。</span><span class="sxs-lookup"><span data-stu-id="95405-146">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="95405-147">如果視窗顯示並播放音訊內容，顯示的視覺效果將會是最近在 Windows Media Player 中使用的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="95405-147">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="95405-148">如果在執行 **IWMPRemoteMediaServices** 的 c + + 程式中， **uiMode** 設為 "custom"，則會顯示 **IWMPRemoteMediaServices** 所指出的面板檔案。</span><span class="sxs-lookup"><span data-stu-id="95405-148">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices.GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="95405-149">在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="95405-149">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="95405-150">範例</span><span class="sxs-lookup"><span data-stu-id="95405-150">Examples</span></span>

<span data-ttu-id="95405-151">下列範例會建立一個清單方塊，讓使用者變更內嵌 Windows Media Player 物件的使用者介面模式。</span><span class="sxs-lookup"><span data-stu-id="95405-151">The following example creates a list box that allows the user to change the user interface mode for an embedded Windows Media Player object.</span></span> <span data-ttu-id="95405-152">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="95405-152">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a><span data-ttu-id="95405-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="95405-153">Requirements</span></span>



| <span data-ttu-id="95405-154">需求</span><span class="sxs-lookup"><span data-stu-id="95405-154">Requirement</span></span> | <span data-ttu-id="95405-155">值</span><span class="sxs-lookup"><span data-stu-id="95405-155">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95405-156">版本</span><span class="sxs-lookup"><span data-stu-id="95405-156">Version</span></span><br/>   | <span data-ttu-id="95405-157">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="95405-157">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="95405-158">Windows Media Player 9 系列或更新版本，表示「隱藏」或「自訂」</span><span class="sxs-lookup"><span data-stu-id="95405-158">Windows Media Player 9 Series or later for "invisible" or "custom"</span></span><br/>   |
| <span data-ttu-id="95405-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="95405-159">Namespace</span></span><br/> | <span data-ttu-id="95405-160">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="95405-160">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="95405-161">組件</span><span class="sxs-lookup"><span data-stu-id="95405-161">Assembly</span></span><br/>  | <dl> <span data-ttu-id="95405-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="95405-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95405-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95405-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95405-164">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="95405-164">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95405-165">**AxWindowsMediaPlayer. enableCoNtextMenu (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="95405-165">**AxWindowsMediaPlayer.enableContextMenu (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





