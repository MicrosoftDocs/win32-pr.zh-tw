---
title: 確保 Windows Media Player 開啟 HTMLView 內容
description: 確保 Windows Media Player 開啟 HTMLView 內容
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Windows Media 中繼檔播放清單，Windows Media Player 開啟 HTMLView 內容
- 播放清單，Windows Media Player 開啟 HTMLView 內容
- 中繼檔播放清單，Windows Media Player 開啟 HTMLView 內容
- Windows Media 中繼檔播放清單，開啟 HTMLView 內容
- 播放清單，開啟 HTMLView 內容
- 中繼檔播放清單，開啟 HTMLView 內容
- 開啟 HTMLView 內容
- Windows Media Player，開啟 HTMLView 內容
- Windows Media Player，HTMLView 內容
- HTMLView，開啟內容
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673516"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a><span data-ttu-id="33ff8-113">確保 Windows Media Player 開啟 HTMLView 內容</span><span class="sxs-lookup"><span data-stu-id="33ff8-113">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>

<span data-ttu-id="33ff8-114">目前，Windows Media Player 9 系列和 Windows Media Player 10 是唯一支援 .asx 檔案中 *HTMLView* 參數的播放程式。</span><span class="sxs-lookup"><span data-stu-id="33ff8-114">Currently, Windows Media Player 9 Series and Windows Media Player 10 are the only players that support the *HTMLView* parameter in .asx files.</span></span> <span data-ttu-id="33ff8-115">這表示您應該採取步驟，以確保 HTMLView 內容會在這些版本的 Windows Media Player 中播放。</span><span class="sxs-lookup"><span data-stu-id="33ff8-115">This means you should take steps to ensure that your HTMLView content plays back in these versions of Windows Media Player.</span></span>

<span data-ttu-id="33ff8-116">您必須先判斷是否已在使用者的電腦上安裝 Windows Media Player 9 系列或 Windows Media Player 10。</span><span class="sxs-lookup"><span data-stu-id="33ff8-116">You must first determine whether Windows Media Player 9 Series or Windows Media Player 10 is installed on the user's computer.</span></span> <span data-ttu-id="33ff8-117">Windows Media Player SDK 包含完整的範例，示範如何在不同的網頁瀏覽器中偵測不同版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="33ff8-117">The Windows Media Player SDK includes a comprehensive sample that demonstrates how to detect different versions of Windows Media Player in different Web browsers.</span></span> <span data-ttu-id="33ff8-118">雖然偵測範例的完整分析已超出本節的範圍，但您可以採取一些基本步驟來判斷使用者電腦執行的 Windows Media Player 版本。</span><span class="sxs-lookup"><span data-stu-id="33ff8-118">Although a complete analysis of the detection sample is beyond the scope of this section, there are some basic steps you can take to determine which version of Windows Media Player the user's computer is running.</span></span>

<span data-ttu-id="33ff8-119">偵測 Windows Media Player 的最簡單方式，就是在網頁中內嵌 Player 控制項，以連結至您的 HTMLView 內容，然後檢查 *播放* 程式所抓取的值。**versionInfo** 屬性。</span><span class="sxs-lookup"><span data-stu-id="33ff8-119">In its simplest form, detecting Windows Media Player involves embedding the Player control in the webpage that links to your HTMLView content and then inspecting the value retrieved by the *Player*.**versionInfo** property.</span></span> <span data-ttu-id="33ff8-120">確認使用者已安裝 Windows Media Player 9 系列或 Windows Media Player 10 之後，您就可以使用 [openPlayer](player-openplayer.md) 方法來開啟全模式播放程式中的內容。</span><span class="sxs-lookup"><span data-stu-id="33ff8-120">Once you have verified that the user has Windows Media Player 9 Series or Windows Media Player 10 installed, you can use the [Player.openPlayer](player-openplayer.md) method to open the content in the full-mode Player.</span></span> <span data-ttu-id="33ff8-121">**OpenPlayer** 方法可確保您的內容一開始會顯示在全模式播放程式的「**立即播放**」功能中，而不是在面板、迷你播放程式模式下，或是另一個已註冊為 .asx 副檔名之檔案的預設程式，但不支援 HTMLView 的播放程式中顯示。</span><span class="sxs-lookup"><span data-stu-id="33ff8-121">The **openPlayer** method ensures that your content is initially displayed in the **Now Playing** feature of the full-mode Player, rather than in a skin, in mini Player mode, or in another player that has registered itself as the default program for files with an .asx file name extension, but doesn't support HTMLView.</span></span> <span data-ttu-id="33ff8-122">不過，在顯示內容之後，使用者可以完全掌控 Windows Media Player，這表示他或她可以選擇顯示 [ **立即播放**] 以外的功能、切換至 [面板] 模式，或甚至結束播放程式。</span><span class="sxs-lookup"><span data-stu-id="33ff8-122">Once the content is displayed, however, the user has complete control of Windows Media Player, meaning that he or she can choose to display a feature other than **Now Playing**, switch to skin mode, or even quit the Player.</span></span>

<span data-ttu-id="33ff8-123">下列程式碼範例會建立 Internet Explorer 的網頁。</span><span class="sxs-lookup"><span data-stu-id="33ff8-123">The following example code creates a webpage for Internet Explorer.</span></span> <span data-ttu-id="33ff8-124">此頁面會開啟 .asx 檔案，此檔案會指定在安裝 Windows Media Player 9 系列或更新版本時，在全模式播放程式中出現的 HTMLView 網頁。</span><span class="sxs-lookup"><span data-stu-id="33ff8-124">This page opens an .asx file, which specifies an HTMLView webpage that appears in the full-mode Player when Windows Media Player 9 Series or later is installed.</span></span>


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="33ff8-125">上述範例中的程式碼會內嵌 Windows Media Player 控制項，並將 **uiMode** 屬性設定為「隱藏」，而「播放程式高度」和「寬度」屬性則設定為零。</span><span class="sxs-lookup"><span data-stu-id="33ff8-125">The code in the preceding example embeds the Windows Media Player control with the **uiMode** property set to "invisible" and the Player height and width attributes set to zero.</span></span> <span data-ttu-id="33ff8-126">這是因為網頁不需要一開始就顯示播放程式控制項使用者介面，它只需要存取 Player 物件模型。</span><span class="sxs-lookup"><span data-stu-id="33ff8-126">This is because the webpage does not require the Player control user interface to be displayed initially—it only requires access to the Player object model.</span></span> <span data-ttu-id="33ff8-127">頁面也會顯示 [輸入] 按鈕，讓使用者播放 .asx 檔。</span><span class="sxs-lookup"><span data-stu-id="33ff8-127">The page also displays an input button that enables the user to play the .asx file.</span></span>

<span data-ttu-id="33ff8-128">當使用者按一下 [Play .ASX] 按鈕時，會執行 Microsoft JScript 函數 PlayASX。</span><span class="sxs-lookup"><span data-stu-id="33ff8-128">When the user clicks the Play ASX button, the Microsoft JScript function PlayASX runs.</span></span> <span data-ttu-id="33ff8-129">此函式會先取得 Player **versionInfo** 屬性的值，方法是使用 JScript **parseInt** 方法檢查所抓取字串的數值。</span><span class="sxs-lookup"><span data-stu-id="33ff8-129">This function first retrieves the value for the Player **versionInfo** property, using the JScript **parseInt** method to inspect the numerical value of the string retrieved.</span></span> <span data-ttu-id="33ff8-130">如果數值大於或等於 9 (表示使用者已) 安裝 Windows Media Player 9 系列，腳本會呼叫 **openPlayer** 方法，並傳遞包含 HTMLView 參數之 .asx 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="33ff8-130">If the numerical value is greater than or equal to 9 (meaning that the user has Windows Media Player 9 Series installed), the script code calls the **openPlayer** method, passing the URL of the .asx file that contains the HTMLView parameter.</span></span> <span data-ttu-id="33ff8-131">這個方法會使用 [完整] 模式中的 Windows Media Player 來開啟 .asx 檔案、在 .asx 播放清單中播放數位媒體內容，並在 [ **立即播放** ] 功能中顯示 HTMLView 的網頁內容。</span><span class="sxs-lookup"><span data-stu-id="33ff8-131">This method opens the .asx file using Windows Media Player in full mode, plays the digital media content in the .asx playlist, and displays the HTMLView Web-based content in the **Now Playing** feature.</span></span>

<span data-ttu-id="33ff8-132">如果版本字串的數值不大於或等於 9 (表示使用者未在其電腦上安裝 Windows Media Player 9 系列或更新版本) 。腳本程式碼會將 Player 控制項的 **uiMode** 變更為「完整」、設定控制項的新寬度和高度，然後藉由指定 **URL** 屬性的值，在內嵌的播放程式中開啟 .asx 檔。</span><span class="sxs-lookup"><span data-stu-id="33ff8-132">If the numerical value of the version string is not greater than or equal to 9 (meaning that the user does not have Windows Media Player 9 Series or later installed on his or her computer), the script code changes the **uiMode** of the Player control to "full", sets a new width and height for the control, and then opens the .asx file in the embedded Player by specifying a value for the **URL** property.</span></span> <span data-ttu-id="33ff8-133">發生這種情況時，會在網頁中播放數位媒體內容，但會忽略在 .asx 檔案中指定的任何 HTMLView 值。</span><span class="sxs-lookup"><span data-stu-id="33ff8-133">When this happens, the digital media content plays in the webpage, but any HTMLView values specified in the .asx file are ignored.</span></span>

<span data-ttu-id="33ff8-134">當使用者未安裝 Windows Media Player 9 系列或 Windows Media Player 10 時，如何播放內容的方式是由您自行決定。</span><span class="sxs-lookup"><span data-stu-id="33ff8-134">How content is played back when the user does not have Windows Media Player 9 Series or Windows Media Player 10 installed is up to you.</span></span> <span data-ttu-id="33ff8-135">上述範例顯示如何指定在網頁中播放內容，而不是在全模式播放程式中，忽略進程中的任何 HTMLView 內容。</span><span class="sxs-lookup"><span data-stu-id="33ff8-135">The preceding example shows how to specify that the content play in the webpage instead of the full-mode Player, ignoring any HTMLView content in the process.</span></span> <span data-ttu-id="33ff8-136">還有其他您可能會採用的方法。</span><span class="sxs-lookup"><span data-stu-id="33ff8-136">There are other approaches you might take.</span></span> <span data-ttu-id="33ff8-137">例如，您可以提示使用者安裝較新版本的 Windows Media Player，讓該版本的播放程式能夠播放數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="33ff8-137">For example, you could prompt the user to install a newer version of Windows Media Player, making that version of the Player a requirement for playing back your digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33ff8-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="33ff8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33ff8-139">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="33ff8-139">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="33ff8-140">**UiMode**</span><span class="sxs-lookup"><span data-stu-id="33ff8-140">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="33ff8-141">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="33ff8-141">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 




