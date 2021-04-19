---
title: AxWindowsMediaPlayer-全螢幕屬性
description: 全螢幕屬性會取得或設定值，指出是否以全螢幕模式播放影片內容。
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- 全螢幕屬性 Windows Media Player
- 全螢幕屬性 Windows Media Player、AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，全螢幕屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992378"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a><span data-ttu-id="22f11-106">AxWindowsMediaPlayer-全螢幕屬性</span><span class="sxs-lookup"><span data-stu-id="22f11-106">AxWindowsMediaPlayer.fullScreen property</span></span>

<span data-ttu-id="22f11-107">全螢幕屬性會取得或設定值，指出是否以全螢幕模式播放影片內容。</span><span class="sxs-lookup"><span data-stu-id="22f11-107">The fullScreen property gets or sets a value indicating whether video content is played in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="22f11-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="22f11-108">Syntax</span></span>


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="22f11-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="22f11-109">Property value</span></span>

<span data-ttu-id="22f11-110">指出內容是否以全螢幕模式播放的布林值。</span><span class="sxs-lookup"><span data-stu-id="22f11-110">A System.Boolean value that indicates whether content is played in full-screen mode.</span></span> <span data-ttu-id="22f11-111">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="22f11-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="22f11-112">備註</span><span class="sxs-lookup"><span data-stu-id="22f11-112">Remarks</span></span>

<span data-ttu-id="22f11-113">若要在內嵌 Windows Media Player 控制項時讓全螢幕模式正常運作，影片顯示區域必須具有至少一個圖元的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="22f11-113">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="22f11-114">如果 **uiMode** 設定為「迷你」或「完整」，則控制項本身的高度必須是65或更大，才能容納除了使用者介面之外的影片顯示區域。</span><span class="sxs-lookup"><span data-stu-id="22f11-114">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="22f11-115">如果 **uiMode** 設為「隱藏」，則將這個屬性設定為 true 會引發錯誤，而且不會影響控制項的行為。</span><span class="sxs-lookup"><span data-stu-id="22f11-115">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="22f11-116">在全螢幕播放期間，Windows Media Player 會在 [enableCoNtextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="22f11-116">During full-screen playback, Windows Media Player hides the mouse cursor when [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="22f11-117">如果 **uiMode** 設為「完整」或「迷你」，Windows Media Player 在滑鼠游標移動時，以全螢幕模式顯示傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="22f11-117">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="22f11-118">在不移動滑鼠的短暫間隔之後，就會隱藏傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="22f11-118">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="22f11-119">如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。</span><span class="sxs-lookup"><span data-stu-id="22f11-119">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="22f11-120">以全螢幕模式顯示傳輸控制項需要 Windows XP 作業系統。</span><span class="sxs-lookup"><span data-stu-id="22f11-120">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

 

<span data-ttu-id="22f11-121">如果傳輸控制項未以全螢幕模式顯示，則 Windows Media Player 會在播放停止時自動離開全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="22f11-121">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

## <a name="examples"></a><span data-ttu-id="22f11-122">範例</span><span class="sxs-lookup"><span data-stu-id="22f11-122">Examples</span></span>

<span data-ttu-id="22f11-123">下列範例會建立一個按鈕，使用 [全螢幕] 屬性將內嵌的播放機物件切換至全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="22f11-123">The following example creates a button that uses the fullScreen property to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="22f11-124">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="22f11-124">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="22f11-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="22f11-125">Requirements</span></span>



| <span data-ttu-id="22f11-126">需求</span><span class="sxs-lookup"><span data-stu-id="22f11-126">Requirement</span></span> | <span data-ttu-id="22f11-127">值</span><span class="sxs-lookup"><span data-stu-id="22f11-127">Value</span></span> |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22f11-128">版本</span><span class="sxs-lookup"><span data-stu-id="22f11-128">Version</span></span><br/>   | <span data-ttu-id="22f11-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="22f11-129">Windows Media Player 9 Series or later</span></span><br/>                                                                  |
| <span data-ttu-id="22f11-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="22f11-130">Namespace</span></span><br/> | <span data-ttu-id="22f11-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="22f11-131">**AxWMPLib**</span></span><br/>                                                                                            |
| <span data-ttu-id="22f11-132">組件</span><span class="sxs-lookup"><span data-stu-id="22f11-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="22f11-133"><dt>AxInterop. WMPLib (AxInterop.WMPLib.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="22f11-133"><dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22f11-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22f11-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22f11-135">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="22f11-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="22f11-136">**AxWindowsMediaPlayer. uiMode (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="22f11-136">**AxWindowsMediaPlayer.uiMode (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





