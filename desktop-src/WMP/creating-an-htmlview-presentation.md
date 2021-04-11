---
title: 建立 HTMLView 簡報
description: 建立 HTMLView 簡報
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Windows Media 中繼檔播放清單，HTMLView 簡報
- 播放清單、HTMLView 簡報
- 中繼檔播放清單，HTMLView 簡報
- Windows Media 中繼檔播放清單，建立 HTMLView 簡報
- 播放清單，建立 HTMLView 簡報
- 中繼檔播放清單，建立 HTMLView 簡報
- 建立 HTMLView 簡報
- Windows Media Player，建立 HTMLView 簡報
- Windows Media Player，HTMLView 簡報
- HTMLView，建立簡報
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372345"
---
# <a name="creating-an-htmlview-presentation"></a><span data-ttu-id="83468-113">建立 HTMLView 簡報</span><span class="sxs-lookup"><span data-stu-id="83468-113">Creating an HTMLView Presentation</span></span>

<span data-ttu-id="83468-114">若要建立基本的 HTMLView 簡報，您需要至少三個元素：</span><span class="sxs-lookup"><span data-stu-id="83468-114">To create a basic HTMLView presentation, you need at least three elements:</span></span>

-   <span data-ttu-id="83468-115">**數位媒體內容。**</span><span class="sxs-lookup"><span data-stu-id="83468-115">**Digital media content.**</span></span> <span data-ttu-id="83468-116">這是一或多個 Windows Media Player 播放的音訊或影片檔案。</span><span class="sxs-lookup"><span data-stu-id="83468-116">This is one or more audio or video files that Windows Media Player plays.</span></span>
-   <span data-ttu-id="83468-117">**網頁。**</span><span class="sxs-lookup"><span data-stu-id="83468-117">**A webpage.**</span></span> <span data-ttu-id="83468-118">這是以網路為基礎的內容，會顯示在播放程式 UI 的「 **立即播放** 」功能中。</span><span class="sxs-lookup"><span data-stu-id="83468-118">This is the Web-based content that displays in the **Now Playing** feature of the Player UI.</span></span>
-   <span data-ttu-id="83468-119">**Windows Media 中繼檔。**</span><span class="sxs-lookup"><span data-stu-id="83468-119">**A Windows Media metafile.**</span></span> <span data-ttu-id="83468-120">這是用來指示 Windows Media Player 將數位媒體內容與網頁結合的中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="83468-120">This is the metafile playlist that directs Windows Media Player to combine the digital media content with the webpage.</span></span>

<span data-ttu-id="83468-121">.Asx 檔案是一種文字檔，可提供檔案資料流程及其簡報的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83468-121">An .asx file is a text file that provides information about a file stream and its presentation.</span></span> <span data-ttu-id="83468-122">根據可延伸標記語言 (XML)  (XML) 語法，.asx 檔案可以包含各種不同的元素，而每個專案都是由具有相關聯屬性的標記所識別。</span><span class="sxs-lookup"><span data-stu-id="83468-122">Based on Extensible Markup Language (XML) syntax, .asx files can contain a variety of elements, each identified by a tag with associated attributes.</span></span> <span data-ttu-id="83468-123">**PARAM** 元素提供一種方式，可讓自訂參數與中繼檔播放清單中的特定專案或整個中繼檔產生關聯。</span><span class="sxs-lookup"><span data-stu-id="83468-123">The **PARAM** element provides a way to associate a custom parameter with either a particular entry in a metafile playlist or the entire metafile.</span></span> <span data-ttu-id="83468-124">其中一個可供您使用的預先定義參數名稱為 "HTMLView"。</span><span class="sxs-lookup"><span data-stu-id="83468-124">One of the predefined parameter names available for your use is "HTMLView".</span></span> <span data-ttu-id="83468-125">這是讓 URL 值指定的網頁顯示在 Windows Media Player 中的參數。</span><span class="sxs-lookup"><span data-stu-id="83468-125">This is the parameter that causes the webpage specified by the URL value to be displayed in Windows Media Player.</span></span>

<span data-ttu-id="83468-126">下列範例程式碼顯示將單一數位媒體檔案與單一網頁結合的 .asx 檔案：</span><span class="sxs-lookup"><span data-stu-id="83468-126">The following example code shows an .asx file that combines a single digital media file with a single webpage:</span></span>


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="83468-127">當 Windows Media Player 在上述範例中開啟 .asx 檔案時，它會從名為 content1 的檔案播放音訊，並在全模式播放程式的「 **立即播放** 」功能中開啟名為 htmlview.htm 的網頁。</span><span class="sxs-lookup"><span data-stu-id="83468-127">When Windows Media Player opens the .asx file in the preceding example, it plays the audio from the file named content1.wma and opens the webpage named htmlview.htm in the **Now Playing** feature of the full-mode Player.</span></span> <span data-ttu-id="83468-128">使用者可以使用 Windows Media Player 控制項來暫停、搜尋及停止音訊內容。</span><span class="sxs-lookup"><span data-stu-id="83468-128">The user can pause, seek, and stop the audio content using the Windows Media Player controls.</span></span>

<span data-ttu-id="83468-129">您可以藉由將 **PARAM** 元素與每個專案產生關聯，輕鬆地變更每個內容所顯示的網頁，如下列程式碼範例所示：</span><span class="sxs-lookup"><span data-stu-id="83468-129">You can easily change the webpage that is displayed for each piece of content by associating a **PARAM** element with each entry, as the following code example shows:</span></span>


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="83468-130">在上述範例中，Windows Media Player 先顯示在播放數位音訊檔案 content1 時的網頁 htmlview1.htm。</span><span class="sxs-lookup"><span data-stu-id="83468-130">In the preceding example, Windows Media Player first displays the webpage htmlview1.htm while playing the digital audio file content1.wma.</span></span> <span data-ttu-id="83468-131">當播放清單開啟播放清單（content2）中的下一個專案時，顯示在中的網頁 **現在現正播放** htmlview2.htm 的變更。</span><span class="sxs-lookup"><span data-stu-id="83468-131">When the Player opens the next entry in the playlist, content2.wma, the webpage displayed in **Now Playing** changes to htmlview2.htm.</span></span> <span data-ttu-id="83468-132">如此一來，您就可以指定使用者針對每個數位媒體內容所看到的網頁。</span><span class="sxs-lookup"><span data-stu-id="83468-132">In this way, you can specify which webpage the user sees for each piece of digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83468-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="83468-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83468-134">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="83468-134">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="83468-135">**PARAM 元素**</span><span class="sxs-lookup"><span data-stu-id="83468-135">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




