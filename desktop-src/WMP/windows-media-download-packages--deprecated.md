---
title: " (淘汰的 Windows Media 下載套件) "
description: " (淘汰的 Windows Media 下載套件) "
ms.assetid: e2d55253-574e-4b18-8b69-2c7e2f6ef9c4
keywords:
- Windows Media 中繼檔，Windows Media 下載套件
- Windows Media Player，Windows Media 下載套件
- 中繼檔，Windows Media 下載套件
- Windows Media、Windows Media 下載套件
- Windows Media 下載套件，關於
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 746330f16b883c337c87f055770477ba1ecf5621
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021471"
---
# <a name="windows-media-download-packages-deprecated"></a><span data-ttu-id="61424-108"> (淘汰的 Windows Media 下載套件) </span><span class="sxs-lookup"><span data-stu-id="61424-108">Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="61424-109">本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="61424-109">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="61424-110">Windows Media 下載套件將 Windows Media Player 框線、播放清單資訊和多媒體內容，結合 wmd 副檔名的單一可下載檔案中。</span><span class="sxs-lookup"><span data-stu-id="61424-110">Windows Media Download packages combine Windows Media Player borders, playlist information, and multimedia content in a single downloadable file with a .wmd file name extension.</span></span> <span data-ttu-id="61424-111">Windows Media 下載套件可能包含整個專輯的音樂影片，這些影片也會以圖形商標的形式顯示廣告，並連結至線上音樂零售商網站。</span><span class="sxs-lookup"><span data-stu-id="61424-111">A Windows Media Download package could include an entire album of music videos that also displays advertising in the form of graphical branding and links to an online music retailer website.</span></span>

<span data-ttu-id="61424-112">使用者只要按一下連結，就可以從網站下載 Windows Media 下載套件。</span><span class="sxs-lookup"><span data-stu-id="61424-112">Users can download a Windows Media Download package from a website simply by clicking a link.</span></span> <span data-ttu-id="61424-113">將套件下載到使用者的電腦之後，Windows Media Player 會自動解壓縮套件內的檔案，然後將封裝的播放清單新增至 [播放清單] 下拉式方塊、將內容新增至文件庫、在 [完整模式] Windows Media Player 的 [ **立即播放** ] 窗格中顯示框線外觀，然後播放播放清單中的初始專案。</span><span class="sxs-lookup"><span data-stu-id="61424-113">Once the package is downloaded to the user's computer, Windows Media Player extracts the files inside the package automatically, then adds the packaged playlist to the playlists drop-down box, adds the content to the library, displays the border skin in the **Now Playing** pane of the full mode Windows Media Player, and then plays the initial item in the playlist.</span></span>

<span data-ttu-id="61424-114">Windows Media 下載套件提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="61424-114">Windows Media Download packages provide the following benefits:</span></span>

-   <span data-ttu-id="61424-115">單鍵下載、解壓縮及目錄配合多個檔案到使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="61424-115">A single-click downloads, extracts, and catalogues multiple files to the user's computer.</span></span>
-   <span data-ttu-id="61424-116">內容會在下載後立即播放。</span><span class="sxs-lookup"><span data-stu-id="61424-116">Content plays immediately after being downloaded.</span></span>
-   <span data-ttu-id="61424-117">自訂框線可以顯示廣告和商標資訊。</span><span class="sxs-lookup"><span data-stu-id="61424-117">Customized borders can display advertising and branding information.</span></span>
-   <span data-ttu-id="61424-118">封裝的播放清單會在媒體櫃中進行編目。</span><span class="sxs-lookup"><span data-stu-id="61424-118">Packaged playlists are cataloged in the library.</span></span>
-   <span data-ttu-id="61424-119">網站重新導向可能會從 Windows Media Player 內的相關網站進行。</span><span class="sxs-lookup"><span data-stu-id="61424-119">Web site redirection can occur from within Windows Media Player to a related site.</span></span>
-   <span data-ttu-id="61424-120">有各種互動式框線控制項可供使用。</span><span class="sxs-lookup"><span data-stu-id="61424-120">A variety of interactive border controls are available.</span></span>
-   <span data-ttu-id="61424-121">有多個音訊和影片檔案類型支援封裝。</span><span class="sxs-lookup"><span data-stu-id="61424-121">Multiple audio and video file types are supported for packaging.</span></span>

<span data-ttu-id="61424-122">所有這些優點都可以一起使用。</span><span class="sxs-lookup"><span data-stu-id="61424-122">All of these benefits can be used together.</span></span> <span data-ttu-id="61424-123">例如，單一 Windows Media 下載套件可讓使用者有機會在播放歌曲時看到歌詞、顯示歌曲隨附的影片、觀看有關記錄散發者的廣告資訊、觀看專輯封面、造訪風扇網站，以及在文件庫中將內容編目。</span><span class="sxs-lookup"><span data-stu-id="61424-123">For example, a single Windows Media Download package could give users the opportunity to view the lyrics to songs as they play, display a video that accompanies the songs, view advertising information about the record distributor, view album cover art, visit a fan website, and catalog the content in the library.</span></span>

<span data-ttu-id="61424-124">下列各節提供的概念可協助您瞭解及建立 Windows Media 下載套件。</span><span class="sxs-lookup"><span data-stu-id="61424-124">The following sections provide concepts to help you understand and create Windows Media Download packages.</span></span>



| <span data-ttu-id="61424-125">區段</span><span class="sxs-lookup"><span data-stu-id="61424-125">Section</span></span>                                                                                                                               | <span data-ttu-id="61424-126">描述</span><span class="sxs-lookup"><span data-stu-id="61424-126">Description</span></span>                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61424-127">Windows Media 下載套件的運作方式 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="61424-127">How Windows Media Download Packages Work (deprecated)</span></span>](how-windows-media-download-packages-work--deprecated.md)                     | <span data-ttu-id="61424-128">概要說明如何將 Windows Media 下載檔案封裝、張貼至網站、下載及播放 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="61424-128">Provides an overview of how a Windows Media Download file is packaged, posted to a website, downloaded, and played by Windows Media Player.</span></span> |
| [<span data-ttu-id="61424-129">在 Windows Media 下載套件中使用框線 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="61424-129">Using Borders in Windows Media Download Packages (deprecated)</span></span>](using-borders-in-windows-media-download-packages--deprecated.md)     | <span data-ttu-id="61424-130">介紹框線，並說明如何建立框線。</span><span class="sxs-lookup"><span data-stu-id="61424-130">Introduces borders and explains how a border is created.</span></span>                                                                                    |
| [<span data-ttu-id="61424-131">在 Windows Media 下載套件中使用播放清單 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="61424-131">Using Playlists in Windows Media Download Packages (deprecated)</span></span>](using-playlists-in-windows-media-download-packages--deprecated.md) | <span data-ttu-id="61424-132">描述如何在 Windows Media 下載套件中使用中繼檔播放清單檔案，並提供範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="61424-132">Describes how a metafile playlist file is used in a Windows Media Download package, and provides sample code.</span></span>                               |
| [<span data-ttu-id="61424-133"> (已淘汰) 建立 Windows Media 下載套件 </span><span class="sxs-lookup"><span data-stu-id="61424-133">Creating a Windows Media Download Package (deprecated)</span></span>](creating-a-windows-media-download-package--deprecated.md)                   | <span data-ttu-id="61424-134">描述將封裝放在一起以進行散發的程式。</span><span class="sxs-lookup"><span data-stu-id="61424-134">Describes the process of putting a package together for distribution.</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="61424-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="61424-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61424-136">**關於 Windows Media 中繼檔**</span><span class="sxs-lookup"><span data-stu-id="61424-136">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="61424-137">**Windows Media Player (已淘汰) 的框線**</span><span class="sxs-lookup"><span data-stu-id="61424-137">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> </dl>

 

 




