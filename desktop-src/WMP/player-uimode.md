---
title: UiMode
description: UiMode 屬性會指定或抓取值，指出使用者介面中顯示的控制項。
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- UiMode Windows Media Player
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994039"
---
# <a name="playeruimode"></a><span data-ttu-id="3df86-104">UiMode</span><span class="sxs-lookup"><span data-stu-id="3df86-104">Player.uiMode</span></span>

<span data-ttu-id="3df86-105">**UiMode** 屬性會指定或抓取值，指出使用者介面中顯示的控制項。</span><span class="sxs-lookup"><span data-stu-id="3df86-105">The **uiMode** property specifies or retrieves a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df86-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3df86-106">Syntax</span></span>

<span data-ttu-id="3df86-107">*玩家* 。**uiMode**</span><span class="sxs-lookup"><span data-stu-id="3df86-107">*player* .**uiMode**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3df86-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="3df86-108">Possible Values</span></span>

<span data-ttu-id="3df86-109">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="3df86-109">This property is a read/write **String**.</span></span>



| <span data-ttu-id="3df86-110">值</span><span class="sxs-lookup"><span data-stu-id="3df86-110">Value</span></span>     | <span data-ttu-id="3df86-111">描述</span><span class="sxs-lookup"><span data-stu-id="3df86-111">Description</span></span>                                                                                                                                                                                                           | <span data-ttu-id="3df86-112">音訊範例</span><span class="sxs-lookup"><span data-stu-id="3df86-112">Audio Example</span></span>                                          | <span data-ttu-id="3df86-113">影片範例</span><span class="sxs-lookup"><span data-stu-id="3df86-113">Video Example</span></span>                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="3df86-114">不可見的</span><span class="sxs-lookup"><span data-stu-id="3df86-114">invisible</span></span> | <span data-ttu-id="3df86-115">Windows Media Player 內嵌時，不會有任何可見的使用者介面 (控制項、影片或視覺效果視窗) 。</span><span class="sxs-lookup"><span data-stu-id="3df86-115">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                        | <span data-ttu-id="3df86-116"> (不會顯示任何內容。 ) </span><span class="sxs-lookup"><span data-stu-id="3df86-116">(Nothing is displayed.)</span></span>                                | <span data-ttu-id="3df86-117"> (不會顯示任何內容。 ) </span><span class="sxs-lookup"><span data-stu-id="3df86-117">(Nothing is displayed.)</span></span>                                |
| <span data-ttu-id="3df86-118">無</span><span class="sxs-lookup"><span data-stu-id="3df86-118">none</span></span>      | <span data-ttu-id="3df86-119">Windows Media Player 內嵌時沒有控制項，而且只會顯示 [影片] 或 [視覺效果] 視窗。</span><span class="sxs-lookup"><span data-stu-id="3df86-119">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                         | ![具有音訊的 "none"](images/uimode-none-audio-v11.png) | ![影片為 "none"](images/uimode-none-video-v11.png) |
| <span data-ttu-id="3df86-122">迷你</span><span class="sxs-lookup"><span data-stu-id="3df86-122">mini</span></span>      | <span data-ttu-id="3df86-123">除了 [影片] 或 [視覺效果] 視窗之外，Windows Media Player 還會以狀態視窗、播放/暫停、停止、靜音和音量控制項來內嵌。</span><span class="sxs-lookup"><span data-stu-id="3df86-123">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                          | ![具有音訊的「迷你」](images/uimode-mini-audio-v11.png) | ![含影片的「迷你」](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="3df86-126">完整</span><span class="sxs-lookup"><span data-stu-id="3df86-126">full</span></span>      | <span data-ttu-id="3df86-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="3df86-127">Default.</span></span> <span data-ttu-id="3df86-128">除了影片或視覺效果視窗之外，Windows Media Player 是以狀態視窗、搜尋列、播放/暫停、停止、靜音、下一個、向前、向前、向前、向前、向前、向前、向前、向前、更快速、更快速的方式，以及音量控制項</span><span class="sxs-lookup"><span data-stu-id="3df86-128">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</span></span> | ![具有音訊的「完整」](images/uimode-full-audio-v11.png) | ![「full」影片](images/uimode-full-video-v11.png) |
| <span data-ttu-id="3df86-131">自訂</span><span class="sxs-lookup"><span data-stu-id="3df86-131">custom</span></span>    | <span data-ttu-id="3df86-132">Windows Media Player 內嵌自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="3df86-132">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="3df86-133">只能在 c + + 程式中使用。</span><span class="sxs-lookup"><span data-stu-id="3df86-133">Can only be used in C++ programs.</span></span>                                                                                                                      | <span data-ttu-id="3df86-134"> (的自訂使用者介面隨即顯示。 ) </span><span class="sxs-lookup"><span data-stu-id="3df86-134">(Custom user interface is displayed.)</span></span>                  | <span data-ttu-id="3df86-135"> (的自訂使用者介面隨即顯示。 ) </span><span class="sxs-lookup"><span data-stu-id="3df86-135">(Custom user interface is displayed.)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="3df86-136">備註</span><span class="sxs-lookup"><span data-stu-id="3df86-136">Remarks</span></span>

<span data-ttu-id="3df86-137">這個屬性會指定內嵌 Windows Media Player 的外觀。</span><span class="sxs-lookup"><span data-stu-id="3df86-137">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="3df86-138">當 **uiMode** 設定為「無」、「迷你」或「完整」時，顯示影片剪輯和音訊視覺效果的視窗就會出現。</span><span class="sxs-lookup"><span data-stu-id="3df86-138">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="3df86-139">您可以將 **物件** 標記的 **height** 屬性設為40（從底部測量），並將使用者介面的控制項部分保持可見，以將此視窗隱藏在迷你或完整模式中。</span><span class="sxs-lookup"><span data-stu-id="3df86-139">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="3df86-140">如果沒有想要的內嵌介面，請將 [ **寬度** ] 和 [ **高度** ] 屬性都設定為零。</span><span class="sxs-lookup"><span data-stu-id="3df86-140">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="3df86-141">如果 **uiMode** 設為「隱藏」，則不會顯示任何使用者介面，但在頁面上的空間仍會保留在 **寬度** 和 **高度** 所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="3df86-141">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="3df86-142">這適用于在 **uiMode** 可以變更時保留頁面配置。</span><span class="sxs-lookup"><span data-stu-id="3df86-142">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="3df86-143">此外，保留的空間是透明的，因此會顯示控制項背後的任何元素。</span><span class="sxs-lookup"><span data-stu-id="3df86-143">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="3df86-144">如果 **uiMode** 設定為「完整」或「迷你」，Windows Media Player 會以全螢幕模式顯示傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="3df86-144">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="3df86-145">如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。</span><span class="sxs-lookup"><span data-stu-id="3df86-145">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="3df86-146">如果視窗顯示並播放音訊內容，顯示的視覺效果將會是最近在 Windows Media Player 中使用的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3df86-146">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="3df86-147">如果在執行 **IWMPRemoteMediaServices** 的 c + + 程式中， **uiMode** 設為 "custom"，則會顯示 **IWMPRemoteMediaServices：： GetCustomUIMode** 所指出的面板檔案。</span><span class="sxs-lookup"><span data-stu-id="3df86-147">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices::GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="3df86-148">在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="3df86-148">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="3df86-149">範例</span><span class="sxs-lookup"><span data-stu-id="3df86-149">Examples</span></span>

<span data-ttu-id="3df86-150">下列範例會建立 HTML SELECT 元素，讓使用者可以變更內嵌 **播放機** 物件的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="3df86-150">The following example creates an HTML SELECT element that allows the user to change the user interface for an embedded **Player** object.</span></span> <span data-ttu-id="3df86-151">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="3df86-151">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



<span data-ttu-id="3df86-152">Windows Media Player 10 行動裝置版：此屬性只接受或傳回 "none" 或 "full" 的值。</span><span class="sxs-lookup"><span data-stu-id="3df86-152">Windows Media Player 10 Mobile: This property only accepts or returns values of "none" or "full".</span></span> <span data-ttu-id="3df86-153">在 Smartphone 裝置上，當 *uiMode* 設定為「完整」時，只會顯示播放狀態和計數器。</span><span class="sxs-lookup"><span data-stu-id="3df86-153">On Smartphone devices, only playback status and a counter are displayed when *uiMode* is set to "full".</span></span>

## <a name="requirements"></a><span data-ttu-id="3df86-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="3df86-154">Requirements</span></span>



| <span data-ttu-id="3df86-155">需求</span><span class="sxs-lookup"><span data-stu-id="3df86-155">Requirement</span></span> | <span data-ttu-id="3df86-156">值</span><span class="sxs-lookup"><span data-stu-id="3df86-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df86-157">版本</span><span class="sxs-lookup"><span data-stu-id="3df86-157">Version</span></span><br/> | <span data-ttu-id="3df86-158">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3df86-158">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="3df86-159">Windows Media Player 9 系列或更新版本，表示「不可見」或「自訂」。</span><span class="sxs-lookup"><span data-stu-id="3df86-159">Windows Media Player 9 Series or later for "invisible" or "custom".</span></span><br/> |
| <span data-ttu-id="3df86-160">DLL</span><span class="sxs-lookup"><span data-stu-id="3df86-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="3df86-161"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df86-161"><dt>Wmp.dll</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="3df86-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3df86-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df86-163">**IWMPRemoteMediaServices 介面**</span><span class="sxs-lookup"><span data-stu-id="3df86-163">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[<span data-ttu-id="3df86-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span><span class="sxs-lookup"><span data-stu-id="3df86-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[<span data-ttu-id="3df86-165">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="3df86-165">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





