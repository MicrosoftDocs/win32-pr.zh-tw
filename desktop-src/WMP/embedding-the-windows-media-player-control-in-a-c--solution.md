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
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a><span data-ttu-id="3489a-119">在 c # 方案中內嵌 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="3489a-119">Embedding the Windows Media Player Control in a C# Solution</span></span>

<span data-ttu-id="3489a-120">若要使用 c # 應用程式中 Windows Media Player 的功能，請先將元件新增至表單，如搭配[使用 Windows Media Player 控制項和 Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)所述。</span><span class="sxs-lookup"><span data-stu-id="3489a-120">To use the functionality of Windows Media Player in a C# application, first add the component to a form as described in [Using the Windows Media Player Control with Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)</span></span>

<span data-ttu-id="3489a-121">下列各節說明如何建立可播放影片並使用自訂 [播放] 和 [停止] 按鈕的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3489a-121">The following sections describe how to create an application that plays video and uses custom play and stop buttons.</span></span>

## <a name="add-the-video-window"></a><span data-ttu-id="3489a-122">新增影片視窗</span><span class="sxs-lookup"><span data-stu-id="3489a-122">Add the Video Window</span></span>

<span data-ttu-id="3489a-123">將 Windows Media Player 的 ActiveX 控制項新增至表單。</span><span class="sxs-lookup"><span data-stu-id="3489a-123">Add the Windows Media Player ActiveX control to a form.</span></span> <span data-ttu-id="3489a-124">調整控制項的大小，然後將它放在您想要顯示影片視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="3489a-124">Resize the control, and then place it where you want the video window to appear.</span></span>

<span data-ttu-id="3489a-125">選取 Windows Media Player 控制項，然後將 [ **uiMode** ] 屬性變更為 [無]。</span><span class="sxs-lookup"><span data-stu-id="3489a-125">Select the Windows Media Player control, then change the **uiMode** property to "none".</span></span> <span data-ttu-id="3489a-126">此設定會隱藏 UI 控制項。</span><span class="sxs-lookup"><span data-stu-id="3489a-126">This setting hides the UI controls.</span></span> <span data-ttu-id="3489a-127">當使用者播放影片時，它會出現在視窗中。</span><span class="sxs-lookup"><span data-stu-id="3489a-127">When the user plays a video, it will appear in the window.</span></span> <span data-ttu-id="3489a-128">針對僅限音訊的內容，將會出現視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3489a-128">For audio-only content, a visualization will appear.</span></span>

## <a name="add-two-buttons-and-adjust-the-form"></a><span data-ttu-id="3489a-129">新增兩個按鈕並調整表單</span><span class="sxs-lookup"><span data-stu-id="3489a-129">Add Two Buttons and Adjust the Form</span></span>

<span data-ttu-id="3489a-130">現在，在表單中新增兩個按鈕。</span><span class="sxs-lookup"><span data-stu-id="3489a-130">Now, add two buttons to the form.</span></span> <span data-ttu-id="3489a-131">選取第一個按鈕，並將 [ **Text** ] 屬性變更為 [Play]。</span><span class="sxs-lookup"><span data-stu-id="3489a-131">Select the first button and change the **Text** property to "Play".</span></span> <span data-ttu-id="3489a-132">選取第二個按鈕，並將其 [ **Text** ] 屬性變更為 [停止]。</span><span class="sxs-lookup"><span data-stu-id="3489a-132">Select the second button and change its **Text** property to "Stop".</span></span>

## <a name="add-the-play-code"></a><span data-ttu-id="3489a-133">新增播放程式碼</span><span class="sxs-lookup"><span data-stu-id="3489a-133">Add the Play Code</span></span>

<span data-ttu-id="3489a-134">按兩下 [ **播放** ] 按鈕以顯示程式碼視窗。</span><span class="sxs-lookup"><span data-stu-id="3489a-134">Double-click the **Play** button to reveal the Code window.</span></span> <span data-ttu-id="3489a-135">在 c # 中，將會顯示下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="3489a-135">In C#, the following code will be displayed:</span></span>


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="3489a-136">在兩個大括弧之間新增這一行：</span><span class="sxs-lookup"><span data-stu-id="3489a-136">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



<span data-ttu-id="3489a-137">在上述程式碼範例中，"axWindowsMediaPlayer1" 是 Windows Media Player 控制項的預設名稱，而 "c： \\ mediafile .wmv" 是您想要播放之媒體專案名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="3489a-137">In the preceding code example, "axWindowsMediaPlayer1" is the default name of the Windows Media Player control, and "c:\\mediafile.wmv" is a placeholder for the name of the media item you want to play.</span></span> <span data-ttu-id="3489a-138">您可以使用任何有效的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="3489a-138">Any valid file path can be used.</span></span> <span data-ttu-id="3489a-139">@ 符號會指示編譯器不要將反斜線解讀為 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="3489a-139">The @ symbol instructs the compiler to not interpret backslashes as escape characters.</span></span>

<span data-ttu-id="3489a-140">如果您已將 Windows Media Player SDK 的數位媒體內容新增至 Windows Media Player 中的程式庫，您可以改用此程式碼：</span><span class="sxs-lookup"><span data-stu-id="3489a-140">If you have added the digital media content from the Windows Media Player SDK to the library in Windows Media Player, you can use this code instead:</span></span>


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



<span data-ttu-id="3489a-141">由於 **autoStart** 屬性預設為 true，因此當您設定 **currentPlaylist** 或 **URL** 屬性時，Windows Media Player 將會開始播放。</span><span class="sxs-lookup"><span data-stu-id="3489a-141">Because the **autoStart** property is true by default, Windows Media Player will start playing when you set the **currentPlaylist** or **URL** property.</span></span>

## <a name="add-the-stop-code"></a><span data-ttu-id="3489a-142">新增停止程式碼</span><span class="sxs-lookup"><span data-stu-id="3489a-142">Add the Stop Code</span></span>

<span data-ttu-id="3489a-143">按兩下 [ **停止** ] 按鈕，以顯示程式碼視窗。</span><span class="sxs-lookup"><span data-stu-id="3489a-143">Double-click the **Stop** button to reveal the Code window.</span></span> <span data-ttu-id="3489a-144">在 c # 中，將會顯示下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="3489a-144">In C#, the following code will be displayed:</span></span>


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



<span data-ttu-id="3489a-145">在兩個大括弧之間新增這一行：</span><span class="sxs-lookup"><span data-stu-id="3489a-145">Add this line between the two curly braces:</span></span>


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> <span data-ttu-id="3489a-146">Windows Media Player 控制項的 managed 程式碼包裝函式會將 **控制項** 物件公開為 **Ctlcontrols** ，以避免與繼承自 **system.object** 的 **控制項** 屬性衝突。</span><span class="sxs-lookup"><span data-stu-id="3489a-146">The managed-code wrapper for the Windows Media Player control exposes the **Controls** object as **Ctlcontrols** to avoid collision with the **Controls** property inherited from **System.Windows.Forms.Control**.</span></span>

 

## <a name="add-error-handling"></a><span data-ttu-id="3489a-147">新增錯誤處理</span><span class="sxs-lookup"><span data-stu-id="3489a-147">Add Error-handling</span></span>

<span data-ttu-id="3489a-148">當 Windows Media Player 控制項遇到錯誤（例如不正確 URL）時，不會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="3489a-148">The Windows Media Player control does not raise an exception when it encounters an error such as an invalid URL.</span></span> <span data-ttu-id="3489a-149">相反地，它會對事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="3489a-149">Instead, it signals an event.</span></span> <span data-ttu-id="3489a-150">您的應用程式應該處理播放程式所傳送的錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="3489a-150">Your application should handle error events sent by the Player.</span></span>

<span data-ttu-id="3489a-151">若要建立事件處理常式，請先開啟 Windows Media Player 控制項的屬性視窗。</span><span class="sxs-lookup"><span data-stu-id="3489a-151">To create an event handler, first open the Properties window for the Windows Media Player control.</span></span> <span data-ttu-id="3489a-152">在事件清單中，按兩下 [ **MediaError**]。</span><span class="sxs-lookup"><span data-stu-id="3489a-152">In the list of events, double-click **MediaError**.</span></span> <span data-ttu-id="3489a-153">隨即顯示下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="3489a-153">The following code is displayed:</span></span>


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



<span data-ttu-id="3489a-154">您可以在方法中插入下列程式碼，以提供最基本的錯誤處理功能。</span><span class="sxs-lookup"><span data-stu-id="3489a-154">The following code could be inserted in the method to provide minimal error-handling capability.</span></span> <span data-ttu-id="3489a-155">請注意，有關此錯誤的資訊可以從 **\_ WMPOCXEvents \_ MediaErrorEvent** 引數中取出。</span><span class="sxs-lookup"><span data-stu-id="3489a-155">Note that information about the error can be retrieved from the **\_WMPOCXEvents\_MediaErrorEvent** argument.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3489a-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="3489a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3489a-157">**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="3489a-157">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




