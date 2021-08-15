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
ms.openlocfilehash: f082da34ffc3b77869e84ceb576b4e6273ccaff15a5f95e66d98cae93697c251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835330"
---
# <a name="playeruimode"></a>UiMode

**UiMode** 屬性會指定或抓取值，指出使用者介面中顯示的控制項。

## <a name="syntax"></a>Syntax

*玩家* 。**uiMode**

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。



| 值     | 描述                                                                                                                                                                                                           | 音訊範例                                          | 影片範例                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| 不可見的 | Windows Media Player 內嵌時，不會有任何可見的使用者介面 (控制項、影片或視覺效果視窗) 。                                                                                                        |  (不會顯示任何內容。 )                                 |  (不會顯示任何內容。 )                                 |
| 無      | Windows Media Player 內嵌時沒有控制項，而且只會顯示 [影片] 或 [視覺效果] 視窗。                                                                                                         | ![具有音訊的 "none"](images/uimode-none-audio-v11.png) | ![影片為 "none"](images/uimode-none-video-v11.png) |
| 迷你      | 除了 [影片] 或 [視覺效果] 視窗之外，Windows Media Player 還會以狀態視窗、播放/暫停、停止、靜音和音量控制項來內嵌。                                                          | ![具有音訊的「迷你」](images/uimode-mini-audio-v11.png) | ![含影片的「迷你」](images/uimode-mini-video-v11.png) |
| 完整      | 預設值。 除了影片或視覺效果視窗之外，Windows Media Player 是以狀態視窗、搜尋列、播放/暫停、停止、靜音、下一個、向前、向前、向前、向前、向前、向前、向前、向前、更快速、更快速的方式，以及音量控制項 | ![具有音訊的「完整」](images/uimode-full-audio-v11.png) | ![「full」影片](images/uimode-full-video-v11.png) |
| 自訂    | Windows Media Player 內嵌自訂使用者介面。 只能在 c + + 程式中使用。                                                                                                                      |  (的自訂使用者介面隨即顯示。 )                   |  (的自訂使用者介面隨即顯示。 )                   |



 

## <a name="remarks"></a>備註

這個屬性會指定內嵌 Windows Media Player 的外觀。 當 **uiMode** 設定為「無」、「迷你」或「完整」時，顯示影片剪輯和音訊視覺效果的視窗就會出現。 您可以將 **物件** 標記的 **height** 屬性設為40（從底部測量），並將使用者介面的控制項部分保持可見，以將此視窗隱藏在迷你或完整模式中。 如果沒有想要的內嵌介面，請將 [ **寬度** ] 和 [ **高度** ] 屬性都設定為零。

如果 **uiMode** 設為「隱藏」，則不會顯示任何使用者介面，但在頁面上的空間仍會保留在 **寬度** 和 **高度** 所指定的位置。 這適用于在 **uiMode** 可以變更時保留頁面配置。 此外，保留的空間是透明的，因此會顯示控制項背後的任何元素。

如果 **uiMode** 設定為「完整」或「迷你」，Windows Media Player 會以全螢幕模式顯示傳輸控制項。 如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。

如果視窗顯示並播放音訊內容，顯示的視覺效果將會是最近在 Windows Media Player 中使用的視覺效果。

如果在執行 **IWMPRemoteMediaServices** 的 c + + 程式中， **uiMode** 設為 "custom"，則會顯示 **IWMPRemoteMediaServices：： GetCustomUIMode** 所指出的面板檔案。

在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 false 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。

## <a name="examples"></a>範例

下列範例會建立 HTML SELECT 元素，讓使用者可以變更內嵌 **播放機** 物件的使用者介面。 使用 ID = "Player" 建立 **player** 物件。


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



Windows Media Player 10 行動裝置版：此屬性只接受或傳回 "none" 或 "full" 的值。 在 Smartphone 裝置上，當 *uiMode* 設定為「完整」時，只會顯示播放狀態和計數器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。 Windows Media Player 9 系列或更新版本，表示「不可見」或「自訂」。<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPRemoteMediaServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





