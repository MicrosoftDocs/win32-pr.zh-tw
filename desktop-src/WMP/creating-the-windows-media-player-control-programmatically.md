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
# <a name="creating-the-windows-media-player-control-programmatically"></a><span data-ttu-id="ff664-111">以程式設計方式建立 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="ff664-111">Creating the Windows Media Player Control Programmatically</span></span>

<span data-ttu-id="ff664-112">當您從 [工具箱] 將 Windows Media Player 控制項加入表單時，會建立類別 **AxWMPLib AxWindowsMediaPlayer** 的物件。</span><span class="sxs-lookup"><span data-stu-id="ff664-112">When you add the Windows Media Player control to a form from the Toolbox, an object of the class **AxWMPLib.AxWindowsMediaPlayer** is created.</span></span> <span data-ttu-id="ff664-113">這個包裝函式類別會為播放程式提供 ActiveX 控制項的所有功能，包括存取 UI 屬性，例如 **位置** 和 **大小**。</span><span class="sxs-lookup"><span data-stu-id="ff664-113">This wrapper class gives the Player all the functionality of an ActiveX control, including access to UI properties such as **Location** and **Size**.</span></span>

<span data-ttu-id="ff664-114">如果您不需要 **AxWindowsMediaPlayer** 所公開的屬性，或您的應用程式沒有圖形化使用者介面，您可以透過程式設計的方式建立播放機控制項。</span><span class="sxs-lookup"><span data-stu-id="ff664-114">If you do not require the properties exposed by **AxWindowsMediaPlayer**, or if your application does not have a graphical user interface, you can create a Player control programmatically.</span></span> <span data-ttu-id="ff664-115">在此情況下，您會建立 **WMPLib. WindowsMediaPlayer** 類別的物件。</span><span class="sxs-lookup"><span data-stu-id="ff664-115">In this case, you create an object of the **WMPLib.WindowsMediaPlayer** class.</span></span>

> [!Note]  
> <span data-ttu-id="ff664-116">由於 **WindowsMediaPlayer** 物件未包裝為 ActiveX 控制項，因此沒有任何繼承自 **system.object** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="ff664-116">Because the **WindowsMediaPlayer** object is not wrapped as an ActiveX control, it does not have any properties inherited from **System.Windows.Forms.Control**.</span></span> <span data-ttu-id="ff664-117">因此， **控制項** 屬性不會重新命名為 **CtlControls**，因為它位於 **AxWindowsMediaPlayer** 中。</span><span class="sxs-lookup"><span data-stu-id="ff664-117">As a result, the **Controls** property is not renamed to **CtlControls**, as it is in **AxWindowsMediaPlayer**.</span></span>

 

<span data-ttu-id="ff664-118">若要以程式設計方式建立 Windows Media Player 控制項，您必須先加入 wmp.dll 的參考，這是在 \\ Windows \\ system32 資料夾中找到的。</span><span class="sxs-lookup"><span data-stu-id="ff664-118">To create the Windows Media Player control programmatically, you must first add a reference to wmp.dll, which is found in the \\Windows\\system32 folder.</span></span> <span data-ttu-id="ff664-119">新增此參考會在您的專案資料夾中建立 WMPLib.dll，並在方案總管中顯示 WMPLib 的參考。</span><span class="sxs-lookup"><span data-stu-id="ff664-119">Adding this reference creates WMPLib.dll in your project folder, and a reference to WMPLib appears in Solution Explorer.</span></span>

<span data-ttu-id="ff664-120">下列範例程式碼（Form1 類別的一部分）會示範如何建立 **Player** 物件並播放檔案。</span><span class="sxs-lookup"><span data-stu-id="ff664-120">The following example code, part of a Form1 class, shows how to create a **Player** object and play a file.</span></span> <span data-ttu-id="ff664-121">當播放結束時，或如果無法播放檔案，就會關閉表單。</span><span class="sxs-lookup"><span data-stu-id="ff664-121">When playback ends, or if the file cannot be played, the form is closed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ff664-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff664-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff664-123">**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="ff664-123">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




