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
ms.openlocfilehash: 51f1d716d36aafbd3625ae1144e0adde1abf0898bee4cbe6831d627cea97bb9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618768"
---
# <a name="axwindowsmediaplayeruimode-property"></a>AxWindowsMediaPlayer. uiMode 屬性

UiMode 屬性會取得或設定值，指出使用者介面中顯示的控制項。

## <a name="syntax"></a>Syntax


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>屬性值

System.string，這是下列其中一個值。



| 值     | 描述                                                                                                                                                                                                     | 音訊範例                                                   | 影片範例                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| 不可見的 | Windows Media Player 內嵌時，不會有任何可見的使用者介面 (控制項、影片或視覺效果視窗) 。                                                                                                  |  (不會顯示任何內容。 )                                          |  (不會顯示任何內容。 )                                          |
| 無      | Windows Media Player 內嵌時沒有控制項，而且只會顯示 [影片] 或 [視覺效果] 視窗。                                                                                                   | ![uimode = 具有音訊的 ' none '](images/uimode-none-audio-v11.png) | ![uimode = 含影片的 ' none '](images/uimode-none-video-v11.png) |
| 迷你      | 除了 [影片] 或 [視覺效果] 視窗之外，Windows Media Player 還會以狀態視窗、播放/暫停、停止、靜音和音量控制項來內嵌。                                                    | ![uimode = 具有音訊的 ' 迷你 '](images/uimode-mini-audio-v11.png) | ![uimode = 影片的 ' 迷你 '](images/uimode-mini-video-v11.png) |
| 完整      | 預設值。 除了影片或視覺效果視窗之外，Windows Media Player 內嵌了狀態視窗、搜尋列、播放/暫停、停止、靜音、下、上、向前、向前、倒轉和音量控制項。 | ![uimode = 具有音訊的 ' full '](images/uimode-full-audio-v11.png) | ![uimode = 「full」影片](images/uimode-full-video-v11.png) |
| 自訂    | Windows Media Player 內嵌自訂使用者介面。 只能在 c + + 程式中使用。                                                                                                                |  (的自訂使用者介面隨即顯示。 )                            |  (的自訂使用者介面隨即顯示。 )                            |



 

## <a name="remarks"></a>備註

這個屬性會指定內嵌 Windows Media Player 的外觀。 當 **uiMode** 設定為「無」、「迷你」或「完整」時，顯示影片剪輯和音訊視覺效果的視窗就會出現。 您可以將 **物件** 標記的 **height** 屬性設為40（從底部測量），並將使用者介面的控制項部分保持可見，以將此視窗隱藏在迷你或完整模式中。 如果沒有想要的內嵌介面，請將 [ **寬度** ] 和 [ **高度** ] 屬性都設定為零。

如果 **uiMode** 設為「隱藏」，則不會顯示任何使用者介面，但在頁面上的空間仍會保留在 **寬度** 和 **高度** 所指定的位置。 這適用于在 **uiMode** 可以變更時保留頁面配置。 此外，保留的空間是透明的，因此會顯示控制項背後的任何元素。

如果 **uiMode** 設定為「完整」或「迷你」，Windows Media Player 會以全螢幕模式顯示傳輸控制項。 如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。

如果視窗顯示並播放音訊內容，顯示的視覺效果將會是最近在 Windows Media Player 中使用的視覺效果。

如果在執行 **IWMPRemoteMediaServices** 的 c + + 程式中， **uiMode** 設為 "custom"，則會顯示 **IWMPRemoteMediaServices** 所指出的面板檔案。

在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 false 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。

## <a name="examples"></a>範例

下列範例會建立一個清單方塊，讓使用者變更內嵌 Windows Media Player 物件的使用者介面模式。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


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





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 7.0 版或更新版本。 Windows Media Player 9 系列或更新版本，表示「隱藏」或「自訂」<br/>   |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. enableCoNtextMenu (VB 和 c # )**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





