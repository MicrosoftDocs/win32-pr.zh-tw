---
title: 以程式設計方式建立 Windows Media Player 控制項
description: 以程式設計方式建立 Windows Media Player 控制項
ms.assetid: 9a4856ce-6a44-47fb-b863-59ce4deb0597
keywords:
- Windows Media Player，以程式設計方式建立 ActiveX 控制項
- Windows Media Player 物件模型，以程式設計方式建立 ActiveX 控制項
- 物件模型，以程式設計方式建立 ActiveX 控制項
- Windows Media Player Mobile，以程式設計方式建立 ActiveX 控制項
- Windows Media Player ActiveX 控制項，以程式設計方式建立
- Windows Media Player 的行動 ActiveX 控制項，以程式設計方式建立
- ActiveX 控制項，以程式設計方式建立
- 以程式設計方式建立 ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222c207b33dcc13a5392f79dad267d6ee82a677c
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311684"
---
# <a name="creating-the-windows-media-player-control-programmatically"></a>以程式設計方式建立 Windows Media Player 控制項

當您從 [工具箱] 將 Windows Media Player 控制項加入表單時，會建立類別 **AxWMPLib AxWindowsMediaPlayer** 的物件。 這個包裝函式類別會為播放程式提供 ActiveX 控制項的所有功能，包括存取 UI 屬性，例如 **位置** 和 **大小**。

如果您不需要 **AxWindowsMediaPlayer** 所公開的屬性，或您的應用程式沒有圖形化使用者介面，您可以透過程式設計的方式建立播放機控制項。 在此情況下，您會建立 **WMPLib. WindowsMediaPlayer** 類別的物件。

> [!Note]  
> 由於 **WindowsMediaPlayer** 物件未包裝為 ActiveX 控制項，因此沒有任何繼承自 **system.object** 的屬性。 因此， **控制項** 屬性不會重新命名為 **CtlControls**，因為它位於 **AxWindowsMediaPlayer** 中。

 

若要以程式設計方式建立 Windows Media Player 控制項，您必須先加入 wmp.dll 的參考，這是在 \\ Windows \\ system32 資料夾中找到的。 新增此參考會在您的專案資料夾中建立 WMPLib.dll，並在方案總管中顯示 WMPLib 的參考。

下列範例程式碼（Form1 類別的一部分）會示範如何建立 **Player** 物件並播放檔案。 當播放結束時，或如果無法播放檔案，就會關閉表單。


```VB
Dim WithEvents Player As WMPLib.WindowsMediaPlayer

Private Sub PlayFile(ByVal url As String)
    Player = New WMPLib.WindowsMediaPlayer
    Player.URL = url
    Player.controls.play()
End Sub

Private Sub Form1_Load(ByVal sender As Object, ByVal e As System.EventArgs) _
                       Handles MyBase.Load
    ' TODO  Insert a valid path in the line below.
    PlayFile("c:\media\myaudio.wma")
End Sub

Private Sub Player_MediaError(ByVal pMediaObject As Object) _
                              Handles Player.MediaError
    MessageBox.Show("Cannot play media file.")
    Me.Close()
End Sub

Private Sub Player_PlayStateChange(ByVal NewState As Integer) _
                                   Handles Player.PlayStateChange
    If NewState = WMPLib.WMPPlayState.wmppsStopped Then
        Me.Close()
    End If
End Sub

```




```CSharp
WMPLib.WindowsMediaPlayer Player;

private void PlayFile(String url)
{
    Player = new WMPLib.WindowsMediaPlayer();
    Player.PlayStateChange += 
        new WMPLib._WMPOCXEvents_PlayStateChangeEventHandler(Player_PlayStateChange);
    Player.MediaError += 
        new WMPLib._WMPOCXEvents_MediaErrorEventHandler(Player_MediaError);
    Player.URL = url;
    Player.controls.play();
}

private void Form1_Load(object sender, System.EventArgs e)
{
    // TODO  Insert a valid path in the line below.
    PlayFile(@"c:\myaudio.wma");
}

private void Player_PlayStateChange(int NewState)
{
    if ((WMPLib.WMPPlayState)NewState == WMPLib.WMPPlayState.wmppsStopped)
    {
        this.Close();
    }
}

private void Player_MediaError(object pMediaObject)
{
    MessageBox.Show("Cannot play media file.");
    this.Close();
}


```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




