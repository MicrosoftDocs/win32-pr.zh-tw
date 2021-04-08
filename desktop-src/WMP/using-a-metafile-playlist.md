---
title: 使用中繼檔播放清單
description: 使用中繼檔播放清單
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Windows Media 中繼檔播放清單，使用
- 中繼檔播放清單，使用
- 播放清單，使用
- Windows Media 中繼檔播放清單，關於
- 中繼檔播放清單，關於
- 播放清單，關於
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672767"
---
# <a name="using-a-metafile-playlist"></a><span data-ttu-id="3624b-109">使用中繼檔播放清單</span><span class="sxs-lookup"><span data-stu-id="3624b-109">Using a Metafile Playlist</span></span>

<span data-ttu-id="3624b-110">由於您無法直接從網頁連結到串流媒體伺服器，因此您可以使用中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="3624b-110">Because you cannot link directly from a webpage to a streaming media server, you use metafile playlists.</span></span> <span data-ttu-id="3624b-111">中繼檔播放清單包含 Windows Media Player 所需的資訊，而且會儲存在 web 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="3624b-111">The metafile playlists contain the information needed by Windows Media Player and are stored on a web server.</span></span> <span data-ttu-id="3624b-112">然後，您可以從 Web 檔連結到中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="3624b-112">You can then link from the Web document to a metafile playlist.</span></span> <span data-ttu-id="3624b-113">開啟中繼檔播放清單時，會將控制項傳輸至 Windows Media Player，以處理檔案、連線至串流處理媒體伺服器，並播放指定的內容。</span><span class="sxs-lookup"><span data-stu-id="3624b-113">When a metafile playlist is opened, control transfers to Windows Media Player, which processes the file, connects to the streaming media server, and plays the specified content.</span></span>

<span data-ttu-id="3624b-114">瀏覽器會先將中繼檔播放清單下載到使用者的快取目錄。</span><span class="sxs-lookup"><span data-stu-id="3624b-114">The browser first downloads the metafile playlist to the user's cache directory.</span></span> <span data-ttu-id="3624b-115">因為中繼檔播放清單很小，所以這是非常快速的步驟。</span><span class="sxs-lookup"><span data-stu-id="3624b-115">Because the metafile playlist is small, this is a very quick step.</span></span> <span data-ttu-id="3624b-116">使用者的電腦接著會在其 [檔案關聯] 資料表中找到與 Windows Media Player 的中繼檔播放清單關聯。</span><span class="sxs-lookup"><span data-stu-id="3624b-116">The user's computer then finds in its file associations table the association of the metafile playlist with Windows Media Player.</span></span> <span data-ttu-id="3624b-117">Windows Media Player 會開啟並解釋中繼檔播放清單中的腳本，其中包含串流內容的 URL，還有其他專案。</span><span class="sxs-lookup"><span data-stu-id="3624b-117">Windows Media Player opens and interprets the scripting in the metafile playlist, which contains, among other things, the URL of the streaming content.</span></span> <span data-ttu-id="3624b-118">Windows Media Player 會使用 URL 來找出內容並起始資料流程。</span><span class="sxs-lookup"><span data-stu-id="3624b-118">Windows Media Player uses the URL to locate the content and initiate the stream.</span></span> <span data-ttu-id="3624b-119">中繼檔播放清單腳本接著會控制串流體驗。</span><span class="sxs-lookup"><span data-stu-id="3624b-119">The metafile playlist scripting then controls the streaming experience.</span></span>

<span data-ttu-id="3624b-120">因為中繼檔播放清單會透過與 ASXMIME 類型相關聯的協助程式應用程式運作， (application/mplayer2 或 video/x--------) --------</span><span class="sxs-lookup"><span data-stu-id="3624b-120">Because metafile playlists work through a helper application associated with the ASXMIME type (application/mplayer2 or video/x-ms-asf), they are compatible with any browser that supports helper applications.</span></span> <span data-ttu-id="3624b-121">本檔中顯示的範例適用于 Microsoft Internet Explorer 4.0 和更新版本，以及 Microsoft Win32®和 Apple Macintosh 平臺上的 Netscape Navigator 4.0 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="3624b-121">The examples shown in this document will work with Microsoft Internet Explorer 4.0 and later, and with Netscape Navigator 4.0 and later on Microsoft Win32® and Apple Macintosh platforms.</span></span> <span data-ttu-id="3624b-122">在所有範例中，您都必須確定參考的任何數位媒體檔案都具有有效的環境路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="3624b-122">In all examples, you will have to be sure that any digital media files referenced have valid paths and file names for your environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3624b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="3624b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3624b-124">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="3624b-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="3624b-125">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="3624b-125">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="3624b-126">**Windows Media 中繼檔總覽**</span><span class="sxs-lookup"><span data-stu-id="3624b-126">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




