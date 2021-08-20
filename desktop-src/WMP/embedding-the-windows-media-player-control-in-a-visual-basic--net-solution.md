---
title: 在 Visual Basic .net 方案中內嵌 Windows Media Player 控制項
description: 在 Visual Basic .net 方案中內嵌 Windows Media Player 控制項
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player，內嵌 ActiveX 控制項
- Windows Media Player 物件模型，內嵌 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media PlayerMobile、內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項、內嵌
- Windows Media PlayerMobile ActiveX 控制項，內嵌
- ActiveX 控制項，內嵌
- Windows Media Player，Visual Basic .net
- Windows Media Player 物件模型，Visual Basic .net
- 物件模型，Visual Basic .net
- Windows Media Player行動裝置、Visual Basic .net
- Windows Media Player ActiveX 控制項 Visual Basic .net
- Windows Media PlayerMobile ActiveX 控制項，Visual Basic .net
- ActiveX 控制項，Visual Basic .net
- 內嵌、Visual Basic .net 程式
- Visual Basic .net 程式內嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819387ac9d04f1ff229ff3665257324eddd042b15dff562a55f085a0fc86ca48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935250"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a>在 Visual Basic .net 方案中內嵌 Windows Media Player 控制項

若要在 Visual Basic .net 應用程式中使用 Windows Media Player 9 系列或更新版本的功能，請先將元件新增至表單，如[使用 Windows Media Player 控制項搭配 Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)所述。

本節說明如何建立可播放影片並擁有自訂 [播放] 和 [停止] 按鈕的應用程式。

## <a name="add-the-video-window"></a>新增影片視窗

將 Windows Media Player 控制項新增至表單。 調整控制項的大小，然後將它放在您想要顯示影片視窗的位置。

選取 Windows Media Player 控制項，然後將 [ **uiMode** ] 屬性變更為 [無]。 此設定會隱藏 UI 控制項。 當使用者播放影片時，它會出現在視窗中。 針對僅限音訊的內容，將會出現視覺效果。

## <a name="add-two-buttons-and-adjust-the-form"></a>新增兩個按鈕並調整表單

現在將兩個按鈕加入表單中。 選取第一個按鈕，並將 [ **Text** ] 屬性變更為 [Play]。 選取第二個按鈕，並將其 [ **Text** ] 屬性變更為 [停止]。

## <a name="add-the-play-code"></a>新增播放程式碼

按兩下 [ **播放** ] 按鈕以顯示程式碼視窗。 隨即顯示下列程式碼：


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



將這一行新增至副程式：


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



在上述程式碼範例中，"axWindowsMediaPlayer1" 是 Windows Media Player 控制項的預設名稱，而 "c： \\ mediafile .wmv" 是您想要播放之媒體名稱的預留位置。

如果您已將 Windows Media Player SDK 的數位媒體內容新增至 Windows Media Player 中的程式庫，您可以改用此程式碼：


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



由於 **autoStart** 屬性預設為 true，因此當您設定 **currentPlaylist** 或 **URL** 屬性時，Windows Media Player 將會開始播放。

## <a name="add-the-stop-code"></a>新增停止程式碼

按兩下 [ **停止** ] 按鈕，以顯示程式碼視窗。 隨即顯示下列程式碼：


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



將這一行新增至副程式：


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> Windows Media Player 控制項的 managed 程式碼包裝函式會將 **控制項** 物件公開為 **Ctlcontrols** ，以避免與繼承自 System. Windows 的 **控制項** 屬性衝突 **。表單. 控制項**。

 

## <a name="add-error-handling"></a>新增錯誤處理

當 Windows Media Player 控制項遇到錯誤（例如不正確 URL）時，不會引發例外狀況。 相反地，控制項會對事件發出信號。 您的應用程式應該處理播放程式所傳送的錯誤事件。

若要建立事件處理常式，請開啟表單類別的程式碼視窗。 從視窗頂端的下拉式清單中，選取 Windows Media Player 控制項。 事件清單會出現在右邊的下拉式清單中。 從該清單中選取 [ [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md)]。 隨即顯示下列程式碼：


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



下列程式碼可以插入副程式中，以提供最基本的錯誤處理功能。 請注意，有關此錯誤的資訊可以從 **\_ WMPOCXEvents \_ MediaErrorEvent** 引數中取出。


```VB
Try
    ' If the file is corrupt or missing, show the 
    ' hexadecimal error code and URL.
    Dim errSource As WMPLib.IWMPMedia2 = e.pMediaObject
    Dim errorItem As WMPLib.IWMPErrorItem = errSource.Error
    MessageBox.Show("Media error " + errorItem.errorCode.ToString("X") _
                    + " in " + errSource.sourceURL)
Catch ex As InvalidCastException
    ' In case pMediaObject is not an IWMPMedia item.
    MessageBox.Show("Player error.")
End Try

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




