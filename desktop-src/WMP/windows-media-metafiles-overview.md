---
title: Windows Media 中繼檔總覽
description: Windows Media 中繼檔總覽
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Windows Media 中繼檔，關於
- Windows Media Player，中繼檔
- Windows Media Player，Windows Media 中繼檔
- 中繼檔，關於
- Windows Media，中繼檔
- Windows Media 中繼檔播放清單，關於
- 播放清單，關於
- Windows Media 中繼檔，語法
- 中繼檔，語法
- 中繼檔播放清單，關於
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969854"
---
# <a name="windows-media-metafiles-overview"></a><span data-ttu-id="5abe8-113">Windows Media 中繼檔總覽</span><span class="sxs-lookup"><span data-stu-id="5abe8-113">Windows Media Metafiles Overview</span></span>

<span data-ttu-id="5abe8-114">成功使用 Windows Media 中繼檔的最重要部分是使用中繼檔元素的正確語法。</span><span class="sxs-lookup"><span data-stu-id="5abe8-114">The most important part of successfully using Windows Media metafiles is using the correct syntax for the metafile elements.</span></span> <span data-ttu-id="5abe8-115">Windows Media 中繼檔中的語法錯誤可能會導致任何來自被忽略之單一屬性的任何事物，而不會將中繼檔辨識為有效且無法運作。</span><span class="sxs-lookup"><span data-stu-id="5abe8-115">Syntax errors in a Windows Media metafile can cause anything from a single attribute being overlooked, to the metafile not being recognized as valid and failing to work.</span></span>

<span data-ttu-id="5abe8-116">最重要的是元素出現在 Windows Media 中繼檔中的順序。</span><span class="sxs-lookup"><span data-stu-id="5abe8-116">Almost as important is the order in which the elements appear in a Windows Media metafile.</span></span> <span data-ttu-id="5abe8-117">某些專案的屬性會暫時覆寫中繼檔不同區段中類似專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="5abe8-117">The attributes of some elements temporarily override the attributes of similar elements in different sections of the metafile.</span></span> <span data-ttu-id="5abe8-118">有一個已定義 [的優先順序](order-of-precedence.md)。</span><span class="sxs-lookup"><span data-stu-id="5abe8-118">There is a defined [Order of Precedence](order-of-precedence.md).</span></span>

<span data-ttu-id="5abe8-119">Windows Media 中繼檔播放清單是 Windows Media 中繼檔，可提供 Windows Media Player 用來接收單點傳送串流、多播串流以及其他內部網路或網際網路支援之媒體的資訊。</span><span class="sxs-lookup"><span data-stu-id="5abe8-119">Windows Media metafile playlists are Windows Media metafiles that provide information that Windows Media Player uses to receive unicast streams, multicast streams, and other supported media from an intranet or the Internet.</span></span> <span data-ttu-id="5abe8-120">中繼檔播放清單基本上是媒體內容的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="5abe8-120">A metafile playlist is basically a shortcut to media content.</span></span> <span data-ttu-id="5abe8-121">中繼檔播放清單可以當做電子郵件傳送，作為網頁上的連結參考、使用 Active Server Pages (ASP) 動態建立，或以獨立檔案的形式存在於本機磁片磁碟機上。</span><span class="sxs-lookup"><span data-stu-id="5abe8-121">A metafile playlist can be sent as email, used as a link reference on a webpage, created dynamically using Active Server Pages (ASP), or exist as a stand-alone file on a local disk drive.</span></span> <span data-ttu-id="5abe8-122">中繼檔播放清單可以參考另一個中繼檔播放清單、ASP 頁面或 (副檔名為 .nsc 的 Windows Media 站檔案) 。</span><span class="sxs-lookup"><span data-stu-id="5abe8-122">A metafile playlist can reference another metafile playlist, an ASP page, or a Windows Media station file (with an .nsc file name extension).</span></span> <span data-ttu-id="5abe8-123">.Nsc 檔案是用來定義要 Windows Media Player 的 Windows Media 站。</span><span class="sxs-lookup"><span data-stu-id="5abe8-123">An .nsc file is used to define a Windows Media station to Windows Media Player.</span></span> <span data-ttu-id="5abe8-124">每個案例的基本處理常式都相同。</span><span class="sxs-lookup"><span data-stu-id="5abe8-124">The basic handling process is the same for each case.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5abe8-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="5abe8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5abe8-126">**關於 Windows Media 中繼檔**</span><span class="sxs-lookup"><span data-stu-id="5abe8-126">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> </dl>

 

 




