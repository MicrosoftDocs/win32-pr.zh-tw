---
title: 在 Visual Basic .NET 方案中內嵌 Windows Media Player 控制項
description: 在 Visual Basic .NET 方案中內嵌 Windows Media Player 控制項
ms.assetid: e6428b42-5d8b-48ef-9f7a-c90a4625b745
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，Visual Basic .NET
- Windows Media Player 物件模型，Visual Basic .NET
- 物件模型，Visual Basic .NET
- Windows Media Player 行動裝置，Visual Basic .NET
- Windows Media Player ActiveX 控制項，Visual Basic .NET
- Windows Media Player 的行動 ActiveX 控制項，Visual Basic .NET
- ActiveX 控制項，Visual Basic .NET
- 內嵌、Visual Basic .NET 程式
- Visual Basic .NET 程式內嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d578b456a5064f1846ead7f074f178753dbc7c97
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311690"
---
# <a name="embedding-the-windows-media-player-control-in-a-visual-basic-net-solution"></a><span data-ttu-id="f34d1-119">在 Visual Basic .NET 方案中內嵌 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="f34d1-119">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>

<span data-ttu-id="f34d1-120">若要在 Visual Basic .NET 應用程式中使用 Windows Media Player 9 系列或更新版本的功能，請先將元件新增至表單，如[使用 Windows Media Player 控制項搭配 Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)所述。</span><span class="sxs-lookup"><span data-stu-id="f34d1-120">To use the functionality of Windows Media Player 9 Series or later in a Visual Basic .NET application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="f34d1-121">本節說明如何建立可播放影片並擁有自訂 [播放] 和 [停止] 按鈕的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f34d1-121">This section describes how to create an application that plays video and has custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="f34d1-122">新增影片視窗</span><span class="sxs-lookup"><span data-stu-id="f34d1-122">Add the Video Window</span></span>

<span data-ttu-id="f34d1-123">將 Windows Media Player 控制項新增至表單。</span><span class="sxs-lookup"><span data-stu-id="f34d1-123">Add the Windows Media Player control to a form.</span></span> <span data-ttu-id="f34d1-124">調整控制項的大小，然後將它放在您想要顯示影片視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="f34d1-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="f34d1-125">選取 Windows Media Player 控制項，然後將 [ **uiMode** ] 屬性變更為 [無]。</span><span class="sxs-lookup"><span data-stu-id="f34d1-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="f34d1-126">此設定會隱藏 UI 控制項。</span><span class="sxs-lookup"><span data-stu-id="f34d1-126">This setting hides the UI controls.</span></span> <span data-ttu-id="f34d1-127">當使用者播放影片時，它會出現在視窗中。</span><span class="sxs-lookup"><span data-stu-id="f34d1-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="f34d1-128">針對僅限音訊的內容，將會出現視覺效果。</span><span class="sxs-lookup"><span data-stu-id="f34d1-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="f34d1-129">新增兩個按鈕並調整表單</span><span class="sxs-lookup"><span data-stu-id="f34d1-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="f34d1-130">現在將兩個按鈕加入表單中。</span><span class="sxs-lookup"><span data-stu-id="f34d1-130">Now add two buttons to the form.</span></span> <span data-ttu-id="f34d1-131">選取第一個按鈕，並將 [ **Text** ] 屬性變更為 [Play]。</span><span class="sxs-lookup"><span data-stu-id="f34d1-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="f34d1-132">選取第二個按鈕，並將其 [ **Text** ] 屬性變更為 [停止]。</span><span class="sxs-lookup"><span data-stu-id="f34d1-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="f34d1-133">新增播放程式碼</span><span class="sxs-lookup"><span data-stu-id="f34d1-133">Add the Play Code</span></span>

<span data-ttu-id="f34d1-134">按兩下 [ **播放** ] 按鈕以顯示程式碼視窗。</span><span class="sxs-lookup"><span data-stu-id="f34d1-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="f34d1-135">隨即顯示下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="f34d1-135">The following code is displayed:</span></span>


```VB
Private Sub Button1_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub
```



<span data-ttu-id="f34d1-136">將這一行新增至副程式：</span><span class="sxs-lookup"><span data-stu-id="f34d1-136">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.URL = "c:\mediafile.wmv"
```



<span data-ttu-id="f34d1-137">在上述程式碼範例中，"axWindowsMediaPlayer1" 是 Windows Media Player 控制項的預設名稱，而 "c： \\ mediafile .wmv" 是您想要播放之媒體名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="f34d1-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control and "c:\\mediafile.wmv" is a placeholder for the name of the media you want to play.</span></span>

<span data-ttu-id="f34d1-138">如果您已將 Windows Media Player SDK 的數位媒體內容新增至 Windows Media Player 中的程式庫，您可以改用此程式碼：</span><span class="sxs-lookup"><span data-stu-id="f34d1-138">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```VB
axWindowsMediaPlayer1.currentPlaylist = _
    axWindowsMediaPlayer1.mediaCollection.getByName("mediafile")

```



<span data-ttu-id="f34d1-139">由於 **autoStart** 屬性預設為 true，因此當您設定 **currentPlaylist** 或 **URL** 屬性時，Windows Media Player 將會開始播放。</span><span class="sxs-lookup"><span data-stu-id="f34d1-139">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="f34d1-140">新增停止程式碼</span><span class="sxs-lookup"><span data-stu-id="f34d1-140">Add the Stop Code</span></span>

<span data-ttu-id="f34d1-141">按兩下 [ **停止** ] 按鈕，以顯示程式碼視窗。</span><span class="sxs-lookup"><span data-stu-id="f34d1-141">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="f34d1-142">隨即顯示下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="f34d1-142">The following code is displayed:</span></span>


```VB
Private Sub Button2_Click(ByVal sender As System.Object, _
        ByVal e As System.EventArgs) Handles Button1.Click

End Sub

```



<span data-ttu-id="f34d1-143">將這一行新增至副程式：</span><span class="sxs-lookup"><span data-stu-id="f34d1-143">Add this line to the subroutine:</span></span>


```VB
AxWindowsMediaPlayer1.Ctlcontrols.stop()

```



> [!Note]  
> <span data-ttu-id="f34d1-144">Windows Media Player 控制項的 managed 程式碼包裝函式會將 **控制項** 物件公開為 **Ctlcontrols** ，以避免與繼承自 **system.object** 的 **控制項** 屬性衝突。</span><span class="sxs-lookup"><span data-stu-id="f34d1-144">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="f34d1-145">新增錯誤處理</span><span class="sxs-lookup"><span data-stu-id="f34d1-145">Add Error-handling</span></span>

<span data-ttu-id="f34d1-146">當 Windows Media Player 控制項遇到錯誤（例如不正確 URL）時，不會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f34d1-146">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="f34d1-147">相反地，控制項會對事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="f34d1-147">Instead, the control signals an event.</span></span> <span data-ttu-id="f34d1-148">您的應用程式應該處理播放程式所傳送的錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="f34d1-148">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="f34d1-149">若要建立事件處理常式，請開啟表單類別的程式碼視窗。</span><span class="sxs-lookup"><span data-stu-id="f34d1-149">To create an event handler, open the code window for your form class.</span></span> <span data-ttu-id="f34d1-150">從視窗頂端的下拉式清單中，選取 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="f34d1-150">From the drop-down list at the top of the window, select the Windows Media Player control.</span></span> <span data-ttu-id="f34d1-151">事件清單會出現在右邊的下拉式清單中。</span><span class="sxs-lookup"><span data-stu-id="f34d1-151">A list of events appears in the drop-down list to the right.</span></span> <span data-ttu-id="f34d1-152">從該清單中選取 [ [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md)]。</span><span class="sxs-lookup"><span data-stu-id="f34d1-152">From that list, select [**MediaError**](axwmplib-axwindowsmediaplayer-mediaerror.md).</span></span> <span data-ttu-id="f34d1-153">隨即顯示下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="f34d1-153">The following code is displayed:</span></span>


```VB
Private Sub AxWindowsMediaPlayer1_MediaError(ByVal sender As Object, _
    ByVal e As _WMPOCXEvents_MediaErrorEvent) Handles AxWindowsMediaPlayer1.MediaError

End Sub

```



<span data-ttu-id="f34d1-154">下列程式碼可以插入副程式中，以提供最基本的錯誤處理功能。</span><span class="sxs-lookup"><span data-stu-id="f34d1-154">The following code could be inserted in the subroutine to provide minimal error-handling capability.</span></span> <span data-ttu-id="f34d1-155">請注意，有關此錯誤的資訊可以從 **\_ WMPOCXEvents \_ MediaErrorEvent** 引數中取出。</span><span class="sxs-lookup"><span data-stu-id="f34d1-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f34d1-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="f34d1-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f34d1-157">**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="f34d1-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




