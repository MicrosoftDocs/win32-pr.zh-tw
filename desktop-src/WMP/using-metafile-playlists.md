---
title: 使用中繼檔播放清單
description: 使用中繼檔播放清單
ms.assetid: f5711a7f-7674-4b92-8262-cee8bac4aa77
keywords:
- Windows Media 中繼檔播放清單，關於
- 播放清單，關於
- 中繼檔播放清單，關於
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71f245d1fc1610174f842347a15dfcfaa13286e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839559"
---
# <a name="using-metafile-playlists"></a><span data-ttu-id="f7fd8-106">使用中繼檔播放清單</span><span class="sxs-lookup"><span data-stu-id="f7fd8-106">Using Metafile Playlists</span></span>

<span data-ttu-id="f7fd8-107">播放清單會指定播放串流媒體或媒體檔案的方式，以及 Windows Media Player 將顯示哪些中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-107">Playlists specify how the streaming media or media files will be played and what metadata Windows Media Player will display.</span></span>

<span data-ttu-id="f7fd8-108">本節說明您可以使用播放清單的幾種方式。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-108">This section explains several ways you can use playlists.</span></span> <span data-ttu-id="f7fd8-109">區段分為下列主題。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-109">The section is divided into the following topics.</span></span>



| <span data-ttu-id="f7fd8-110">主題</span><span class="sxs-lookup"><span data-stu-id="f7fd8-110">Topic</span></span>                                                                                              | <span data-ttu-id="f7fd8-111">描述</span><span class="sxs-lookup"><span data-stu-id="f7fd8-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7fd8-112">修改顯示</span><span class="sxs-lookup"><span data-stu-id="f7fd8-112">Modifying the Display</span></span>](modifying-the-display.md)                                                 | <span data-ttu-id="f7fd8-113">加入文字、連結和影像。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-113">Adding text, links, and images.</span></span>                                                                                                                                |
| [<span data-ttu-id="f7fd8-114">重新導向</span><span class="sxs-lookup"><span data-stu-id="f7fd8-114">Redirection</span></span>](redirection.md)                                                                     | <span data-ttu-id="f7fd8-115">使用播放清單將瀏覽器重新導向至 Windows Media Player，並指定要播放之資料流程或媒體檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-115">Using playlists to redirect the browser to Windows Media Player and specifying the URL of a stream or media file to play.</span></span>                                      |
| [<span data-ttu-id="f7fd8-116">存取媒體</span><span class="sxs-lookup"><span data-stu-id="f7fd8-116">Accessing Media</span></span>](accessing-media.md)                                                             | <span data-ttu-id="f7fd8-117">使用中繼檔專案及其子項目來指定要存取的內容，以及其播放的順序和持續時間。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-117">Using metafile elements and their child elements to specify the content to access, and the order and duration of their playback.</span></span>                               |
| [<span data-ttu-id="f7fd8-118">使用即時事件串流切換</span><span class="sxs-lookup"><span data-stu-id="f7fd8-118">Using Live Event Stream Switching</span></span>](using-live-event-stream-switching.md)                         | <span data-ttu-id="f7fd8-119">使用 **EVENT** 元素來指定要存取的媒體資料流程，然後繼續播放原始資料流程。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-119">Using the **EVENT** element to specify a media stream to access and then resume playing the original stream.</span></span> <span data-ttu-id="f7fd8-120">用於廣告插入。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-120">Used for ad insertion.</span></span>                            |
| [<span data-ttu-id="f7fd8-121">使用中繼檔進行順暢的串流切換</span><span class="sxs-lookup"><span data-stu-id="f7fd8-121">Using Metafiles for Seamless Stream Switching</span></span>](using-metafiles-for-seamless-stream-switching.md) | <span data-ttu-id="f7fd8-122">使用 **事件** 專案預先載入下一個媒體資料流程以進行存取，以避免呈現中出現間距。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-122">Using the **EVENT** element to preload the next media stream to access to avoid gaps in the presentation.</span></span>                                                      |
| [<span data-ttu-id="f7fd8-123">使用公告</span><span class="sxs-lookup"><span data-stu-id="f7fd8-123">Using Announcements</span></span>](using-announcements.md)                                                     | <span data-ttu-id="f7fd8-124">使用中繼檔來提供媒體資料流程 URL 的相關資訊，包括多播 IP 位址、埠、串流格式，以及其他工作站設定。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-124">Using a metafile to provide information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> |
| [<span data-ttu-id="f7fd8-125">使用 URL 和伺服器變換</span><span class="sxs-lookup"><span data-stu-id="f7fd8-125">Using URL and Server Rollover</span></span>](using-url-and-server-rollover.md)                                 | <span data-ttu-id="f7fd8-126">使用中繼檔播放清單，可在無法存取或播放資料流程時，提供自動滾動至替代內容來源的方法。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-126">Using metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span>             |
| [<span data-ttu-id="f7fd8-127">使用自訂參數和命令</span><span class="sxs-lookup"><span data-stu-id="f7fd8-127">Using Custom Parameters and Commands</span></span>](using-custom-parameters-and-commands.md)                   | <span data-ttu-id="f7fd8-128">使用 **PARAM** 元素來定義自訂元素，以提供其他中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-128">Using the **PARAM** element to define custom elements to provide additional metadata.</span></span>                                                                          |
| [<span data-ttu-id="f7fd8-129">個人化媒體傳遞</span><span class="sxs-lookup"><span data-stu-id="f7fd8-129">Personalizing Media Delivery</span></span>](personalizing-media-delivery.md)                                   | <span data-ttu-id="f7fd8-130">使用使用者喜好設定來決定廣播內容。</span><span class="sxs-lookup"><span data-stu-id="f7fd8-130">Using user preferences to determine broadcast content.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="f7fd8-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7fd8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7fd8-132">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="f7fd8-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f7fd8-133">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="f7fd8-133">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f7fd8-134">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="f7fd8-134">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




