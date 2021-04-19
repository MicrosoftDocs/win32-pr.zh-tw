---
title: 控制播放體驗
description: 控制播放體驗
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows Media 中繼檔播放清單，控制播放
- 播放清單，控制播放
- 中繼檔播放清單，控制播放
- Windows Media 中繼檔播放清單，播放問題
- 播放清單，播放問題
- 中繼檔播放清單，播放問題
- 控制播放
- Windows Media Player，控制播放
- Windows Media Player，播放問題
- HTMLView，播放問題
- HTMLView，控制播放
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106995553"
---
# <a name="controlling-the-playback-experience"></a><span data-ttu-id="d778f-114">控制播放體驗</span><span class="sxs-lookup"><span data-stu-id="d778f-114">Controlling the Playback Experience</span></span>

<span data-ttu-id="d778f-115">本節將討論使用 HTMLView 功能時可能遇到的一些播放問題。</span><span class="sxs-lookup"><span data-stu-id="d778f-115">This section discusses some of the playback issues you may encounter when using the HTMLView feature.</span></span>

## <a name="requiring-the-user-to-view-web-based-content"></a><span data-ttu-id="d778f-116">要求使用者查看 Web 內容</span><span class="sxs-lookup"><span data-stu-id="d778f-116">Requiring the user to view Web-based content</span></span>

<span data-ttu-id="d778f-117">您可能會想要讓使用者能夠在 HTMLView 的 Web 內容顯示時，享受您的數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="d778f-117">You may decide that you only want users to be able to enjoy your digital media content when the HTMLView Web-based content is also displayed.</span></span> <span data-ttu-id="d778f-118">如果使用者切換離開 **立即播放** 的功能，您可以在 HTMLView 網頁中包含腳本，以停止播放數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="d778f-118">You can include script code in your HTMLView webpage that stops playback of the digital media content if the user switches away from the **Now Playing** feature.</span></span> <span data-ttu-id="d778f-119">若要這樣做，您可以將 **unload** 事件的事件處理常式指定為 **BODY** 元素的一部分，如下列 HTML 程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="d778f-119">To do this, you can specify an event handler for the **unload** event as part of the **BODY** element, as the following HTML code demonstrates:</span></span>


```XML
<BODY onunload = "UnloadMe();">

```



<span data-ttu-id="d778f-120">然後，您可以在事件處理常式函式中包含腳本，以關閉播放程式中的檔案。</span><span class="sxs-lookup"><span data-stu-id="d778f-120">Then you can include script code in your event handler function to close the file in the Player.</span></span> <span data-ttu-id="d778f-121">下列範例程式碼會執行這項操作：</span><span class="sxs-lookup"><span data-stu-id="d778f-121">The following example code does this:</span></span>


```XML
function UnloadMe()
{
   Player.close();
}

```



<span data-ttu-id="d778f-122">當使用者按一下按鈕以開啟另一個 Windows Media Player 功能（例如媒體櫃）來切換離開時， **播放程式會** 關閉內嵌的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="d778f-122">When the user switches away from **Now Playing** by clicking a button to open another Windows Media Player feature, such as the library, the Player closes the embedded browser.</span></span> <span data-ttu-id="d778f-123">這會造成 **onunload** 事件發生，並在名為 **UnloadMe** 的函式中執行腳本。</span><span class="sxs-lookup"><span data-stu-id="d778f-123">This causes the **onunload** event to occur, running the script in the function named **UnloadMe**.</span></span> <span data-ttu-id="d778f-124">[Player. close](player-close.md)方法會停止播放和卸載目前的數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="d778f-124">The [Player.close](player-close.md) method stops playback and unloads the current digital media file.</span></span> <span data-ttu-id="d778f-125">若要再次查看內容，使用者必須重新開啟原始檔案。</span><span class="sxs-lookup"><span data-stu-id="d778f-125">To view the content again, the user must reopen the original .asx file.</span></span> <span data-ttu-id="d778f-126">當使用者離開 HTMLView 網頁時，這項技術也會停止播放。</span><span class="sxs-lookup"><span data-stu-id="d778f-126">This technique also stops playback when the user navigates away from the HTMLView webpage.</span></span> <span data-ttu-id="d778f-127">請注意，當使用者切換至面板模式時，這項技術無法防止使用者觀看數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="d778f-127">Note that this technique cannot prevent the user from viewing the digital media content when he or she switches to skin mode.</span></span>

<span data-ttu-id="d778f-128">您會記得 HTMLView 參數可以套用至 .asx 檔案中的每個 **ENTRY 專案** 。</span><span class="sxs-lookup"><span data-stu-id="d778f-128">You will recall that the HTMLView parameter can be applied to each **ENTRY** element in an .asx file.</span></span> <span data-ttu-id="d778f-129">您可以利用這項功能，確保每次新的數位媒體檔案啟動時，就會顯示您的 HTMLView 內容。</span><span class="sxs-lookup"><span data-stu-id="d778f-129">You can take advantage of this feature to ensure that your HTMLView content is displayed each time a new digital media file starts.</span></span> <span data-ttu-id="d778f-130">若要這樣做，請將 HTMLView 的 **PARAM** 元素與您 .asx 播放清單中的每個專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d778f-130">To do this, associate a **PARAM** element for HTMLView with each entry in your .asx playlist.</span></span> <span data-ttu-id="d778f-131">當每個專案播放時，播放清單都會回到全模式，並顯示您在播放清單中指定的 HTMLView 內容。</span><span class="sxs-lookup"><span data-stu-id="d778f-131">When each entry plays, the Player returns to full mode and displays the HTMLView content you specified in the playlist.</span></span>

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a><span data-ttu-id="d778f-132">預設會停用 URL 和檔案指令碼命令類型</span><span class="sxs-lookup"><span data-stu-id="d778f-132">URL and FILE script command types are disabled by default</span></span>

<span data-ttu-id="d778f-133">Windows Media Player 9 系列或更新版本提供的設定，可讓使用者指定 URL 和檔案類型的指令碼命令是否能夠執行。</span><span class="sxs-lookup"><span data-stu-id="d778f-133">Windows Media Player 9 Series or later provides settings that enable the user to specify whether URL and FILE type script commands are able to run.</span></span> <span data-ttu-id="d778f-134">根據預設，這兩個指令碼命令類型都不會執行。</span><span class="sxs-lookup"><span data-stu-id="d778f-134">By default, both of these script command types do not run.</span></span> <span data-ttu-id="d778f-135">如果您使用自訂指令碼命令類型，不論使用者的設定為何，它們都會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="d778f-135">If you use custom script command types, they will continue to run, regardless of the user setting.</span></span> <span data-ttu-id="d778f-136">如果您必須使用 URL 和檔案類型的指令碼命令，則必須提示使用者變更設定。</span><span class="sxs-lookup"><span data-stu-id="d778f-136">If you must use URL and FILE type script commands, you must prompt the user to change the settings.</span></span> <span data-ttu-id="d778f-137">若要變更設定，請依序按一下 [ **工具**]、[ **選項**] 和 [ **安全性**]。</span><span class="sxs-lookup"><span data-stu-id="d778f-137">To change the settings, click **Tools**, then **Options**, and then **Security**.</span></span>

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a><span data-ttu-id="d778f-138">重新開啟 HTMLView 並不會重載網頁</span><span class="sxs-lookup"><span data-stu-id="d778f-138">Reopening an HTMLView does not reload the webpage</span></span>

<span data-ttu-id="d778f-139">當使用者開啟包含 HTMLView 參數的 .asx 檔案，並接著重新開啟相同的檔案時，Windows Media Player 不會重新整理 HTMLView 網頁。</span><span class="sxs-lookup"><span data-stu-id="d778f-139">When the user opens an .asx file that includes an HTMLView parameter and subsequently reopens the same file, Windows Media Player does not refresh the HTMLView webpage.</span></span> <span data-ttu-id="d778f-140">這也表示，如果您允許使用者離開您的 HTMLView 網頁，播放程式就不會將內嵌瀏覽器傳回初始的 HTMLView 網頁。</span><span class="sxs-lookup"><span data-stu-id="d778f-140">This also means that if you have allowed users to navigate away from your HTMLView webpage, the Player does not return the embedded browser to the initial HTMLView webpage.</span></span>

## <a name="hiding-the-content-location"></a><span data-ttu-id="d778f-141">隱藏內容位置</span><span class="sxs-lookup"><span data-stu-id="d778f-141">Hiding the content location</span></span>

<span data-ttu-id="d778f-142">您可能會決定不希望 Windows Media Player 在播放 .asx 檔案時顯示數位媒體內容的位置。</span><span class="sxs-lookup"><span data-stu-id="d778f-142">You might decide that you don't want Windows Media Player to display the location of your digital media content while it is playing an .asx file.</span></span> <span data-ttu-id="d778f-143">通常，Windows Media Player 只會在從網際網路串流內容時顯示播放清單本身的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d778f-143">Usually, Windows Media Player only shows information about the playlist itself when streaming content from the Internet.</span></span> <span data-ttu-id="d778f-144">不過，您可以採取進一步的步驟，以防止使用者判斷內容的位置。</span><span class="sxs-lookup"><span data-stu-id="d778f-144">However, there are further steps you can take to prevent users from determining the location of your content.</span></span> <span data-ttu-id="d778f-145">例如，您可以使用 Windows Media Services 伺服器端播放清單，來確保播放程式不會顯示您內容的路徑。</span><span class="sxs-lookup"><span data-stu-id="d778f-145">For example, one way to ensure that the Player does not display the path to your content is to stream your content using Windows Media Services server-side playlists.</span></span> <span data-ttu-id="d778f-146">如此一來，當使用者流覽內容的內容時，就會看到伺服器的 URL，而不是您的內容 URL。</span><span class="sxs-lookup"><span data-stu-id="d778f-146">That way, when the user views the properties for the content, he or she sees the URL of the server and not the URL of your content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d778f-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="d778f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d778f-148">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="d778f-148">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="d778f-149">**PARAM 元素**</span><span class="sxs-lookup"><span data-stu-id="d778f-149">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




