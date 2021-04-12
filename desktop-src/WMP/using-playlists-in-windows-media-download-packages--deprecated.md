---
title: '在 Windows Media 下載套件中使用播放清單 (已淘汰) '
description: '在 Windows Media 下載套件中使用播放清單 (已淘汰) '
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- 播放清單，Windows Media 下載套件
- 中繼檔播放清單，Windows Media 下載套件
- Windows Media 中繼檔播放清單，Windows Media 下載套件
- Windows Media 下載套件，播放清單
- Windows Media 下載套件，中繼檔播放清單
- Windows Media 下載套件，Windows Media 中繼檔播放清單
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372448"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="257e4-113">在 Windows Media 下載套件中使用播放清單 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="257e4-113">Using Playlists in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="257e4-114">本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="257e4-114">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="257e4-115">播放清單是具有 .asx 副檔名的 Windows Media 中繼檔，其提供的資訊會告訴 Windows Media Player 如何播放封裝的內容。</span><span class="sxs-lookup"><span data-stu-id="257e4-115">Playlists are Windows Media metafiles with an .asx file name extension that provide information that tells Windows Media Player how to play the packaged content.</span></span> <span data-ttu-id="257e4-116">藉由將多個內容檔案結合成單一 Windows Media 下載套件，您可以使用播放清單來控制和自訂 Windows Media 下載套件。</span><span class="sxs-lookup"><span data-stu-id="257e4-116">By combining multiple content files into a single Windows Media Download package, you can control and customize your Windows Media Download package by using the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="257e4-117">一般情況下，Windows Media 下載套件會使用中繼檔播放清單來參考封裝中的多媒體內容，而不是從內部網路或網際網路上的伺服器來參考資料流。</span><span class="sxs-lookup"><span data-stu-id="257e4-117">In general, metafile playlists are used by Windows Media Download packages to reference the multimedia content in the package rather than a stream from a server on an intranet or the Internet.</span></span> <span data-ttu-id="257e4-118">不過，支援該 .asx 檔案內的 URL 參考。</span><span class="sxs-lookup"><span data-stu-id="257e4-118">However, URL references within the .asx file are supported.</span></span>

 

<span data-ttu-id="257e4-119">使用 XML 時，中繼檔會提供 Windows Media Player 用來播放和顯示內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="257e4-119">Using XML, the metafile provides the information Windows Media Player uses to play and display content.</span></span> <span data-ttu-id="257e4-120">播放清單是由各種 XML 程式碼元素及其相關聯的標記和屬性所組成。</span><span class="sxs-lookup"><span data-stu-id="257e4-120">Playlists are made up of various XML code elements with their associated tags and attributes.</span></span> <span data-ttu-id="257e4-121">Windows Media 中繼檔播放清單中的每個元素都會定義 Windows Media Player 中的特定設定或動作。</span><span class="sxs-lookup"><span data-stu-id="257e4-121">Each element in a Windows Media metafile playlist defines a particular setting or action in Windows Media Player.</span></span>

<span data-ttu-id="257e4-122">使用者的電腦會將副檔名為 .asx 的 Windows Media 中繼檔與 Windows Media Player 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="257e4-122">The user's computer associates a Windows Media metafile that has an .asx file name extension with Windows Media Player.</span></span> <span data-ttu-id="257e4-123">Windows Media Player 會開啟並剖析中繼檔中的 XML 程式碼，其中包含尋找已封裝音訊或影片檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="257e4-123">Windows Media Player opens and parses the XML code in the metafile, which contains the path for locating the packaged audio or video files.</span></span> <span data-ttu-id="257e4-124">然後，中繼檔腳本會控制音訊、影片和圖形化體驗。</span><span class="sxs-lookup"><span data-stu-id="257e4-124">The metafile script then controls the audio, video, and graphical experience.</span></span> <span data-ttu-id="257e4-125">中繼檔也包含 Windows Media Player 處理，並顯示在 [播放清單] 下拉式清單方塊中的資訊。</span><span class="sxs-lookup"><span data-stu-id="257e4-125">The metafile also contains information that Windows Media Player processes and displays in the playlist drop-down box.</span></span> <span data-ttu-id="257e4-126">在清單顯示之後，會立即播放清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="257e4-126">Immediately after the list is displayed, the first item in the list is played.</span></span>

<span data-ttu-id="257e4-127">中繼檔播放清單是包含已封裝內容之檔案的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="257e4-127">A metafile playlist is a shortcut to the files that contain your packaged content.</span></span> <span data-ttu-id="257e4-128">下列程式碼是中繼檔的範例，其中指定要使用 **面板元素顯示** 的框線、要播放的兩個歌曲，以及每一首歌曲的播放清單資訊。</span><span class="sxs-lookup"><span data-stu-id="257e4-128">The following code is an example of a metafile that specifies the border to display by using the **SKIN** element, two songs to be played, and the playlist information for each song.</span></span>


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="257e4-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="257e4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="257e4-130">**Windows Media Player (已淘汰) 的框線**</span><span class="sxs-lookup"><span data-stu-id="257e4-130">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="257e4-131">**(淘汰的 Windows Media 下載套件)**</span><span class="sxs-lookup"><span data-stu-id="257e4-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="257e4-132">**Windows Media 中繼檔**</span><span class="sxs-lookup"><span data-stu-id="257e4-132">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




