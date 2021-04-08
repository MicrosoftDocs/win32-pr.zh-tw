---
title: 使用中繼檔中的相對連結
description: 使用中繼檔中的相對連結
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Windows Media 中繼檔播放清單，相對連結
- 播放清單、相對連結
- 中繼檔播放清單、相對連結
- 中繼檔、相對連結
- Windows Media 中繼檔，相對連結
- relative links (相對連結)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839727"
---
# <a name="using-relative-links-in-metafiles"></a><span data-ttu-id="b9687-109">使用中繼檔中的相對連結</span><span class="sxs-lookup"><span data-stu-id="b9687-109">Using Relative Links in Metafiles</span></span>

<span data-ttu-id="b9687-110">相對連結是 Windows Media 中繼檔的完整支援功能。</span><span class="sxs-lookup"><span data-stu-id="b9687-110">Relative links are a fully supported feature of Windows Media metafiles.</span></span> <span data-ttu-id="b9687-111">您可以使用中繼檔中的相對連結，就像在 HTML 檔案中使用一樣。</span><span class="sxs-lookup"><span data-stu-id="b9687-111">You can use relative links in metafiles much like you use them in HTML documents.</span></span> <span data-ttu-id="b9687-112">使用相對連結可讓您建立可移植的中繼檔，也就是說，您可以將整個目錄結構複製或移動到另一部伺服器，而不需要更新用來作為橫幅的圖形檔案路徑或 **MOREINFO** 專案的 **HREF** 屬性 (如果它們參考與儲存的中繼檔) 相同的 web 伺服器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="b9687-112">The use of relative links enables you to create metafiles that are portable, meaning you can copy or move an entire directory structure to another server without updating the paths to graphic files used as banners or the **HREF** attributes of **MOREINFO** elements (if they reference files on the same web server as the stored metafile).</span></span> <span data-ttu-id="b9687-113">相對連結可在任何支援它們的應用程式中運作，因為未包含在專案之 **HREF** 屬性中的 url 部分，會包含在要求該 url 的應用程式傳送至伺服器的 url 中。</span><span class="sxs-lookup"><span data-stu-id="b9687-113">Relative links work, in any application that supports them, because the parts of the URL not included in the **HREF** attribute of an element are included in the URL sent by the application to the server when that URL is requested.</span></span> <span data-ttu-id="b9687-114">這表示通訊協定 (例如 HTTPs://) 、伺服器名稱，以及包含相對連結的檔案所在的虛擬目錄，全都包含在傳送至伺服器的 URL 中。</span><span class="sxs-lookup"><span data-stu-id="b9687-114">This means that the protocol (such as https://), the server name, and the virtual directory in which the file containing the relative link is located are all included in the URL that is sent to the server.</span></span> <span data-ttu-id="b9687-115">如果您使用相對連結連結到的媒體檔案或 URL 與中繼檔不位於相同的伺服器上，相對連結就會無效。</span><span class="sxs-lookup"><span data-stu-id="b9687-115">If the media file, or URL you link to using a relative link does not reside on the same server as the metafile, the relative link is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="b9687-116">只有在使用獨立 Windows Media Player 中開啟之中繼檔的連結時，相關連結上的這項資訊才是正確的。</span><span class="sxs-lookup"><span data-stu-id="b9687-116">This information on relative links is correct only when using a link to metafiles that are opened in the stand-alone Windows Media Player.</span></span> <span data-ttu-id="b9687-117">當您使用內嵌的 Windows Media Player 控制項時，所有連結都會相對於裝載控制項的頁面，除非使用 **ASX** 元素的 **基底** 子項目來重新導向相對路徑。</span><span class="sxs-lookup"><span data-stu-id="b9687-117">When you use the embedded Windows Media Player control, all links are relative to the page on which the control is hosted, unless the **BASE** child element of the **ASX** element is used to redirect the relative path.</span></span>

 

<span data-ttu-id="b9687-118">中繼檔中的所有相對連結都必須是串流媒體的完全相對，而不是相對於磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b9687-118">All relative links in the metafile must be fully relative, not drive-relative, for streaming media.</span></span> <span data-ttu-id="b9687-119">當 URL 的開頭為 " \\ " 字元時，連結會相對於磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b9687-119">When a URL begins with a "\\" character, the link is drive-relative.</span></span> <span data-ttu-id="b9687-120">Windows Media Player 嘗試在開啟中繼檔的磁片磁碟機上開啟連結的檔案，通常是 web 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b9687-120">Windows Media Player attempts to open the file linked to on the drive where the metafile was opened from, usually a web server.</span></span> <span data-ttu-id="b9687-121">由於 web 伺服器使用虛擬目錄，Windows Media Player 嘗試在開啟中繼檔的 web 伺服器上，于虛擬目錄的子目錄中尋找指定的資料流程或媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="b9687-121">Because web servers use virtual directories, Windows Media Player tries to find the specified stream or media file in a subdirectory of a virtual directory on the web server where the metafile was opened from.</span></span> <span data-ttu-id="b9687-122">使用者無法存取伺服器目錄。</span><span class="sxs-lookup"><span data-stu-id="b9687-122">A user would not have access to a server directory.</span></span> <span data-ttu-id="b9687-123">本章節中的範例說明如何使用完整的相對連結。</span><span class="sxs-lookup"><span data-stu-id="b9687-123">The example in this section illustrates the use of a fully relative link.</span></span>

<span data-ttu-id="b9687-124">當您在單一電腦上使用中繼檔時，可以使用磁片磁碟機相對連結，而中繼檔播放清單中連結的所有媒體檔案都存在於該電腦的儲存裝置上。</span><span class="sxs-lookup"><span data-stu-id="b9687-124">You can use drive-relative links when using metafiles on a single computer where all media files linked to in the metafile playlist exist on a storage device in that computer.</span></span> <span data-ttu-id="b9687-125">不過，您無法以這種方式串流媒體。</span><span class="sxs-lookup"><span data-stu-id="b9687-125">However, you cannot stream media in this manner.</span></span>

<span data-ttu-id="b9687-126">當您使用另一個中繼檔的連結來允許相對連結時，依 Windows Media Player 顯示的名稱會是原始中繼檔中的標題。</span><span class="sxs-lookup"><span data-stu-id="b9687-126">When you use a link to another metafile to allow for relative links, the name displayed as the Title by Windows Media Player is the Title in the original metafile.</span></span>

<span data-ttu-id="b9687-127">相對連結無法用於串流處理媒體伺服器的 Url，因為使用不同的通訊協定來存取串流媒體內容。</span><span class="sxs-lookup"><span data-stu-id="b9687-127">Relative links cannot be used for URLs to a streaming media server because different protocols are used for accessing streaming media content.</span></span>

<span data-ttu-id="b9687-128">在下列範例播放清單中，第一個 **ENTRYREF** 包含另一個播放清單的 URL，相對. 地板蠟。</span><span class="sxs-lookup"><span data-stu-id="b9687-128">In the following example playlist, the first **ENTRYREF** contains a URL for another playlist, relative.wax.</span></span>


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



<span data-ttu-id="b9687-129">下列範例是地板蠟檔案，其中包含相對連結。</span><span class="sxs-lookup"><span data-stu-id="b9687-129">The following example is the file relative.wax, which contains relative links.</span></span>


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="b9687-130">包含播放清單地板蠟參考的 URL 可以存在於使用者可存取的中繼檔播放清單中。</span><span class="sxs-lookup"><span data-stu-id="b9687-130">The URL containing the reference to the playlist, relative.wax, can exist in a metafile playlist anywhere that is accessible to the user.</span></span> <span data-ttu-id="b9687-131">若要成功處理 URL，必須有一個名為 "example.microsoft.com" 的 web 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b9687-131">For the URL to be processed successfully, there must be a web server named "example.microsoft.com".</span></span> <span data-ttu-id="b9687-132">該網頁伺服器必須有定義為「中繼檔」的虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="b9687-132">That web server must have a virtual directory defined as "metafiles".</span></span> <span data-ttu-id="b9687-133">參照的播放清單地板蠟必須存在於虛擬目錄 "中繼檔" 中名為 "example.microsoft.com" 的 web 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b9687-133">The referenced playlist, relative.wax, must exist on the web server named "example.microsoft.com" in the virtual directory "metafiles".</span></span>

<span data-ttu-id="b9687-134">如果要成功存取和播放播放清單中的參考媒體檔案，必須有一個名為 "Graphics" 的目錄，這是伺服器的虛擬目錄 "中繼檔" 的子目錄。</span><span class="sxs-lookup"><span data-stu-id="b9687-134">For the referenced media files in the playlist relative.wax to be successfully accessed and played, there must be a directory named "Graphics" which is a subdirectory of the server's virtual directory "metafiles".</span></span> <span data-ttu-id="b9687-135">**橫幅** 元素中所參考的圖形檔案 Logo1.jpg 必須是名為 graphics 的子目錄。</span><span class="sxs-lookup"><span data-stu-id="b9687-135">The graphics file Logo1.jpg, referenced in the **BANNER** element, must be the subdirectory named Graphics.</span></span>

<span data-ttu-id="b9687-136">同樣地，名為 Category1.htm 的檔必須位於名為 Category1 的子目錄中。</span><span class="sxs-lookup"><span data-stu-id="b9687-136">Similarly a document named Category1.htm must reside in a subdirectory named Category1.</span></span> <span data-ttu-id="b9687-137">名為 Category1 的目錄必須以子目錄形式存在於 web 伺服器 example.microsoft.com 上的虛擬目錄「中繼檔」。</span><span class="sxs-lookup"><span data-stu-id="b9687-137">The directory named Category1 must exist as a subdirectory of the virtual directory "metafiles" on the web server example.microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9687-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9687-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9687-139">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="b9687-139">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="b9687-140">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="b9687-140">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="b9687-141">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="b9687-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b9687-142">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="b9687-142">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




