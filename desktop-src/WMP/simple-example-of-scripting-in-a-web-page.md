---
title: 在網頁中編寫腳本的簡單範例
description: 在網頁中編寫腳本的簡單範例
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player ActiveX 控制項、網頁
- Windows Media Player 的行動 ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- Windows Media Player ActiveX 控制項，腳本範例
- Windows Media Player Mobile ActiveX 控制項，腳本範例
- ActiveX 控制項，腳本範例
- 內嵌、網頁
- 網頁內嵌、腳本範例
- 網頁內嵌的腳本範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "106996359"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a><span data-ttu-id="642ba-119">在網頁中編寫腳本的簡單範例</span><span class="sxs-lookup"><span data-stu-id="642ba-119">Simple Example of Scripting in a Web Page</span></span>

<span data-ttu-id="642ba-120">您可以使用瀏覽器辨識的任何指令碼語言，輕鬆地將 Windows Media Player 控制項內嵌在 HTML 檔案中。</span><span class="sxs-lookup"><span data-stu-id="642ba-120">You can easily embed the Windows Media Player control in an HTML file using any scripting language your browser recognizes.</span></span> <span data-ttu-id="642ba-121">下列簡單的範例會使用 Microsoft JScript 來建立頁面，當您按一下按鈕時，就會播放該檔案，然後在您按一下另一個按鈕時停止播放該檔案。</span><span class="sxs-lookup"><span data-stu-id="642ba-121">The following simple example uses Microsoft JScript to create a page that will play a file when you click on a button, and stop playing the file when you click on another button.</span></span>

<span data-ttu-id="642ba-122">您可以使用下列四個步驟，將 Windows Media Player 的 ActiveX 控制項內嵌到網頁中：</span><span class="sxs-lookup"><span data-stu-id="642ba-122">You can embed the Windows Media Player ActiveX control in a webpage using the following four steps:</span></span>

1.  <span data-ttu-id="642ba-123">建立網頁。</span><span class="sxs-lookup"><span data-stu-id="642ba-123">Create the webpage.</span></span>
2.  <span data-ttu-id="642ba-124">加入物件標記。</span><span class="sxs-lookup"><span data-stu-id="642ba-124">Add the OBJECT tag.</span></span>
3.  <span data-ttu-id="642ba-125">新增使用者介面。</span><span class="sxs-lookup"><span data-stu-id="642ba-125">Add a user interface.</span></span> <span data-ttu-id="642ba-126">在此案例中，有兩個按鈕。</span><span class="sxs-lookup"><span data-stu-id="642ba-126">In this case, two buttons.</span></span>
4.  <span data-ttu-id="642ba-127">新增幾行程式碼，以便在使用者按一下您所建立的其中一個按鈕時回應。</span><span class="sxs-lookup"><span data-stu-id="642ba-127">Add a few lines of code to respond when the user clicks on one of the buttons you have created.</span></span>

## <a name="creating-the-web-page"></a><span data-ttu-id="642ba-128">建立網頁</span><span class="sxs-lookup"><span data-stu-id="642ba-128">Creating the Web Page</span></span>

<span data-ttu-id="642ba-129">第一個步驟是建立有效的 HTML 網頁。</span><span class="sxs-lookup"><span data-stu-id="642ba-129">The first step is to create a valid HTML webpage.</span></span> <span data-ttu-id="642ba-130">若要建立空白但有效的 HTML 網頁，至少需要下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="642ba-130">The following code is the minimum needed to create a blank but valid HTML page:</span></span>


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a><span data-ttu-id="642ba-131">加入物件標記</span><span class="sxs-lookup"><span data-stu-id="642ba-131">Adding the OBJECT Tag</span></span>

<span data-ttu-id="642ba-132">建立網頁之後，您需要新增物件標記。</span><span class="sxs-lookup"><span data-stu-id="642ba-132">Once you have created a webpage, you need to add an OBJECT tag.</span></span> <span data-ttu-id="642ba-133">這會識別瀏覽器的 ActiveX 控制項，並設定任何初始定義。</span><span class="sxs-lookup"><span data-stu-id="642ba-133">This identifies the ActiveX control to the browser and sets up any initial definitions.</span></span> <span data-ttu-id="642ba-134">您必須將物件標記放在程式碼主體中。</span><span class="sxs-lookup"><span data-stu-id="642ba-134">You must place the OBJECT tag in the BODY of the code.</span></span> <span data-ttu-id="642ba-135">如果您將它放在主體中，就會顯示 Windows Media Player 的預設使用者介面。</span><span class="sxs-lookup"><span data-stu-id="642ba-135">If you place it in the BODY, the default user interface of Windows Media Player will be visible.</span></span> <span data-ttu-id="642ba-136">如果您想要建立自己的使用者介面，請將 [高度] 和 [寬度] 屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="642ba-136">If you want to create your own user interface, set the height and width attributes to 0 (zero).</span></span> <span data-ttu-id="642ba-137">您也可以設定 *播放機*。當您想要隱藏控制項，但仍在頁面上保留空間時， **uiMode** 屬性為「隱藏」。</span><span class="sxs-lookup"><span data-stu-id="642ba-137">You can also set the *Player*.**uiMode** property to "invisible" when you want to hide the control, but still reserve space for it on the page.</span></span> <span data-ttu-id="642ba-138">當您提供自訂使用者介面時，建議使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="642ba-138">The following code is recommended when you provide a custom user interface:</span></span>


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



<span data-ttu-id="642ba-139">以下是必要的物件標記屬性：</span><span class="sxs-lookup"><span data-stu-id="642ba-139">The following OBJECT tag attributes are required:</span></span>

<span data-ttu-id="642ba-140">識別碼</span><span class="sxs-lookup"><span data-stu-id="642ba-140">ID</span></span>

<span data-ttu-id="642ba-141">程式碼的其他部分將用來識別和使用 ActiveX 控制項的名稱。</span><span class="sxs-lookup"><span data-stu-id="642ba-141">The name that will be used by other parts of the code to identify and use the ActiveX control.</span></span> <span data-ttu-id="642ba-142">您可以選擇任何想要的名稱，只要它是 HTML、HTML 延伸名或您所使用的指令碼語言尚未使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="642ba-142">You can choose any name you want, as long as it is a name that is not already used by HTML, HTML extensions, or the scripting language you are using.</span></span> <span data-ttu-id="642ba-143">在此範例中，會使用名稱 "Player"，但您也可以將它稱為 "MyPlayer" 或其他名稱。</span><span class="sxs-lookup"><span data-stu-id="642ba-143">In this example, the name "Player" is used, but you could also call it "MyPlayer" or something else.</span></span> <span data-ttu-id="642ba-144">只挑選該網頁的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="642ba-144">Just pick a name that is unique to that webpage.</span></span>

<span data-ttu-id="642ba-145">CLASSID</span><span class="sxs-lookup"><span data-stu-id="642ba-145">CLASSID</span></span>

<span data-ttu-id="642ba-146">非常大的十六進位數位，對控制項而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="642ba-146">A very large hexadecimal number that is unique to the control.</span></span> <span data-ttu-id="642ba-147">只有一個控制項具有此數目，而這是 Windows Media Player 的 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="642ba-147">Only one control has this number and it is the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="642ba-148">若要避免打字錯誤，您可以從檔中複製並貼上此編號。</span><span class="sxs-lookup"><span data-stu-id="642ba-148">To prevent typographical errors, you can copy and paste this number from the documentation.</span></span> <span data-ttu-id="642ba-149">7.0 版之前的 Windows Media Player 控制項版本具有不同的 CLASSID。</span><span class="sxs-lookup"><span data-stu-id="642ba-149">Versions of the Windows Media Player control prior to version 7.0 had a different CLASSID.</span></span>

## <a name="adding-a-user-interface"></a><span data-ttu-id="642ba-150">新增消費者介面</span><span class="sxs-lookup"><span data-stu-id="642ba-150">Adding a User Interface</span></span>

<span data-ttu-id="642ba-151">HTML 允許大量的使用者介面元素，讓使用者可以按一下、按下按鍵和其他使用者動作，與您的網頁互動。</span><span class="sxs-lookup"><span data-stu-id="642ba-151">HTML allows a vast wealth of user interface elements, allowing the user to interact with your webpage by clicking, pressing keys, and other user actions.</span></span> <span data-ttu-id="642ba-152">新增幾個輸入按鈕是提供快速使用者介面最簡單的方式。</span><span class="sxs-lookup"><span data-stu-id="642ba-152">Adding a few INPUT buttons is the easiest way to provide a quick user interface.</span></span> <span data-ttu-id="642ba-153">下列程式碼會建立可回應使用者的兩個按鈕。</span><span class="sxs-lookup"><span data-stu-id="642ba-153">The following code creates two buttons that can respond to the user.</span></span> <span data-ttu-id="642ba-154">按一下其中一個按鈕會啟動媒體資料流程播放，另一個按鈕則會將它停止：</span><span class="sxs-lookup"><span data-stu-id="642ba-154">Clicking one button starts the media stream playing and the other button stops it:</span></span>


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



<span data-ttu-id="642ba-155">按鈕的名稱是用來識別程式碼的按鈕;值是將會出現在按鈕上的標籤，而 OnClick 屬性會識別在按下按鈕時，會呼叫腳本程式碼的哪個部分。</span><span class="sxs-lookup"><span data-stu-id="642ba-155">The name of the button is used to identify the button to your code; the value is the label that will appear on the button, and the OnClick attribute identifies which part of your scripting code will be called when the button is clicked.</span></span>

## <a name="adding-scripting-code"></a><span data-ttu-id="642ba-156">新增腳本程式碼</span><span class="sxs-lookup"><span data-stu-id="642ba-156">Adding Scripting Code</span></span>

<span data-ttu-id="642ba-157">腳本程式碼可將互動功能新增至您的網頁。</span><span class="sxs-lookup"><span data-stu-id="642ba-157">Scripting code adds interactivity to your page.</span></span> <span data-ttu-id="642ba-158">腳本程式碼可以回應事件、呼叫方法，以及變更執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="642ba-158">Scripting code can respond to events, call methods, and change run-time properties.</span></span> <span data-ttu-id="642ba-159">擴充的腳本會包含在腳本標記集內。</span><span class="sxs-lookup"><span data-stu-id="642ba-159">Extended scripts are enclosed in a SCRIPT tag set.</span></span> <span data-ttu-id="642ba-160">腳本標記會告知瀏覽器您的腳本處理常式代碼，並識別指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="642ba-160">The SCRIPT tag tells the browser where your scripting code is and identifies the scripting language.</span></span> <span data-ttu-id="642ba-161">如果您未識別語言，則預設語言會是 Microsoft JScript。</span><span class="sxs-lookup"><span data-stu-id="642ba-161">If you do not identify a language, the default language will be Microsoft JScript.</span></span>

<span data-ttu-id="642ba-162">將腳本放在 HTML 註解標記中是不錯的撰寫作法，因此不支援腳本的瀏覽器不會將您的程式碼轉譯為文字。</span><span class="sxs-lookup"><span data-stu-id="642ba-162">It is good authoring practice to enclose your script in HTML comment tags so browsers that do not support scripting do not render your code as text.</span></span> <span data-ttu-id="642ba-163">將腳本標記放在 HTML 檔案主體內的任何位置，然後將批註括住的程式碼內嵌在開頭和結尾腳本標記內。</span><span class="sxs-lookup"><span data-stu-id="642ba-163">Put the SCRIPT tag anywhere within the BODY of your HTML file and embed the comment-surrounded code within the opening and closing SCRIPT tags.</span></span>

<span data-ttu-id="642ba-164">下列 Microsoft JScript 程式碼範例會呼叫 Windows Media Player 控制項，並執行適當的動作來回應對應的按鈕點擊。</span><span class="sxs-lookup"><span data-stu-id="642ba-164">The following Microsoft JScript code example calls the Windows Media Player control and performs an appropriate action in response to the corresponding button click.</span></span>


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



<span data-ttu-id="642ba-165">當按一下標示為播放的按鈕時，會呼叫 StartMeUp 函式，並在按下 [停止] 按鈕時呼叫 ShutMeDown 函數。</span><span class="sxs-lookup"><span data-stu-id="642ba-165">The example function, StartMeUp, is called when the button marked Play is clicked, and the ShutMeDown function is called when the Stop button is clicked.</span></span>

<span data-ttu-id="642ba-166">StartMeUp 內的程式碼會使用 URL 屬性來定義媒體的路徑。</span><span class="sxs-lookup"><span data-stu-id="642ba-166">The code inside StartMeUp uses the URL property to define a path to the media.</span></span> <span data-ttu-id="642ba-167">媒體將立即開始播放。</span><span class="sxs-lookup"><span data-stu-id="642ba-167">The media will start playing immediately.</span></span>

<span data-ttu-id="642ba-168">ShutMeDown 程式碼會呼叫 **Controls** 物件的 **stop** 方法。</span><span class="sxs-lookup"><span data-stu-id="642ba-168">The ShutMeDown code calls the **stop** method of the **Controls** object.</span></span> <span data-ttu-id="642ba-169">請注意，**控制項** 物件是透過 **Player** 物件的 **controls** 屬性來呼叫，其 ID 值為 "player"。</span><span class="sxs-lookup"><span data-stu-id="642ba-169">Note that the **Controls** object is called through the **controls** property of the **Player** object, which has the ID value of "Player".</span></span>

<span data-ttu-id="642ba-170">下列程式碼顯示完整範例。</span><span class="sxs-lookup"><span data-stu-id="642ba-170">The following code shows a complete example.</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



<span data-ttu-id="642ba-171">請注意，您必須在 [URL] 屬性中提供有效的 URL 給有效的檔案名。</span><span class="sxs-lookup"><span data-stu-id="642ba-171">Note that you must provide a valid URL to a valid file name in the URL property.</span></span> <span data-ttu-id="642ba-172">在此情況下，假設檔案 laure 與 HTML 檔案位於相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="642ba-172">In this case the assumption is that the file laure.wma is in the same directory as the HTML file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="642ba-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="642ba-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="642ba-174">**在 Web 網頁中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="642ba-174">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




