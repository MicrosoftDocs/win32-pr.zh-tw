---
title: 在 C 方案中內嵌 Windows Media Player 控制項
description: 在 C \ 方案中內嵌 Windows Media Player 控制項
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player、C
- Windows Media Player 物件模型，C
- 物件模型、C
- Windows Media Player Mobile、C
- Windows Media Player ActiveX 控制項，C
- Windows Media Player 行動 ActiveX 控制項，C
- ActiveX 控制項，C
- 內嵌、C 程式
- C 程式內嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "106995145"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>在 c # 方案中內嵌 Windows Media Player 控制項

若要使用 c # 應用程式中 Windows Media Player 的功能，請先將元件新增至表單，如搭配[使用 Windows Media Player 控制項和 Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)所述。

下列各節說明如何建立可播放影片並使用自訂 [播放] 和 [停止] 按鈕的應用程式。

## <a name="add-the-video-window"></a>新增影片視窗

將 Windows Media Player 的 ActiveX 控制項新增至表單。 調整控制項的大小，然後將它放在您想要顯示影片視窗的位置。

選取 Windows Media Player 控制項，然後將 [ **uiMode** ] 屬性變更為 [無]。 此設定會隱藏 UI 控制項。 當使用者播放影片時，它會出現在視窗中。 針對僅限音訊的內容，將會出現視覺效果。

## <a name="add-two-buttons-and-adjust-the-form"></a>新增兩個按鈕並調整表單

現在，在表單中新增兩個按鈕。 選取第一個按鈕，並將 [ **Text** ] 屬性變更為 [Play]。 選取第二個按鈕，並將其 [ **Text** ] 屬性變更為 [停止]。

## <a name="add-the-play-code"></a>新增播放程式碼

按兩下 [ **播放** ] 按鈕以顯示程式碼視窗。 在 c # 中，將會顯示下列程式碼：


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



在兩個大括弧之間新增這一行：


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



在上述程式碼範例中，"axWindowsMediaPlayer1" 是 Windows Media Player 控制項的預設名稱，而 "c： \\ mediafile .wmv" 是您想要播放之媒體專案名稱的預留位置。 您可以使用任何有效的檔案路徑。 @ 符號會指示編譯器不要將反斜線解讀為 escape 字元。

如果您已將 Windows Media Player SDK 的數位媒體內容新增至 Windows Media Player 中的程式庫，您可以改用此程式碼：


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



由於 **autoStart** 屬性預設為 true，因此當您設定 **currentPlaylist** 或 **URL** 屬性時，Windows Media Player 將會開始播放。

## <a name="add-the-stop-code"></a>新增停止程式碼

按兩下 [ **停止** ] 按鈕，以顯示程式碼視窗。 在 c # 中，將會顯示下列程式碼：


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



在兩個大括弧之間新增這一行：


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> Windows Media Player 控制項的 managed 程式碼包裝函式會將 **控制項** 物件公開為 **Ctlcontrols** ，以避免與繼承自 **system.object** 的 **控制項** 屬性衝突。

 

## <a name="add-error-handling"></a>新增錯誤處理

當 Windows Media Player 控制項遇到錯誤（例如不正確 URL）時，不會引發例外狀況。 相反地，它會對事件發出信號。 您的應用程式應該處理播放程式所傳送的錯誤事件。

若要建立事件處理常式，請先開啟 Windows Media Player 控制項的屬性視窗。 在事件清單中，按兩下 [ **MediaError**]。 隨即顯示下列程式碼：


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



您可以在方法中插入下列程式碼，以提供最基本的錯誤處理功能。 請注意，有關此錯誤的資訊可以從 **\_ WMPOCXEvents \_ MediaErrorEvent** 引數中取出。


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




