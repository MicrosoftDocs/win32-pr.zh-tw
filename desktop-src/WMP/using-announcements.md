---
title: 使用公告
description: 使用公告
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Windows Media 中繼檔播放清單，公告
- 播放清單、公告
- 中繼檔播放清單，公告
- Windows Media Player，公告
- 宣告
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968837"
---
# <a name="using-announcements"></a><span data-ttu-id="4f485-108">使用公告</span><span class="sxs-lookup"><span data-stu-id="4f485-108">Using Announcements</span></span>

<span data-ttu-id="4f485-109">公告是一個檔案，其中包含媒體串流 URL 的相關資訊，包括多播 IP 位址、埠、串流格式，以及其他工作站設定。</span><span class="sxs-lookup"><span data-stu-id="4f485-109">An announcement is a file that contains information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> <span data-ttu-id="4f485-110">建立單播或多播發布串流時，Windows Media 系統管理員會建立宣告。</span><span class="sxs-lookup"><span data-stu-id="4f485-110">Announcements are created by Windows Media Administrator when a unicast or multicast publishing stream is created.</span></span> <span data-ttu-id="4f485-111">用戶端可以快速載入公告檔案，然後繼續存取串流處理媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="4f485-111">The client can quickly load the announcement file, then proceed to access the streaming media file.</span></span>

<span data-ttu-id="4f485-112">若為單播發行端點，則會開啟發行端點媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="4f485-112">For a unicast publishing point, the publishing point media stream is opened.</span></span> <span data-ttu-id="4f485-113">若是多播發行端點，則會從 .nsc 副檔名的廣播站檔案解壓縮 URL，並存取串流媒體。</span><span class="sxs-lookup"><span data-stu-id="4f485-113">For a multicast publishing point, the URL is extracted from a broadcast station file with an .nsc extension, and the streaming media is accessed.</span></span> <span data-ttu-id="4f485-114">不同于單播串流，多播資料流程中不包含任何標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="4f485-114">Unlike a unicast stream, no header information is contained in a multicast stream.</span></span> <span data-ttu-id="4f485-115">這是來自廣播站檔案，副檔名為 .nsc 的資訊。</span><span class="sxs-lookup"><span data-stu-id="4f485-115">That information comes from the broadcast station file with an .nsc extension.</span></span> <span data-ttu-id="4f485-116">Windows Media Player 通常會先開啟公告檔案，這是一個用於中繼檔播放清單，指向廣播站檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="4f485-116">Windows Media Player usually first opens an announcement file, which is one use for metafile playlists, that points to the location of the broadcast station file.</span></span>

<span data-ttu-id="4f485-117">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="4f485-117">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="4f485-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f485-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f485-119">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="4f485-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4f485-120">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="4f485-120">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




