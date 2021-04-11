---
title: Web 串流
description: Web 串流
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media Format SDK，Web 資料流程
- Advanced Systems Format (ASF) 、Web 串流
- ASF (Advanced Systems Format) ，Web 串流
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- Web 串流，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021377"
---
# <a name="web-streams"></a><span data-ttu-id="45207-110">Web 串流</span><span class="sxs-lookup"><span data-stu-id="45207-110">Web Streams</span></span>

<span data-ttu-id="45207-111">Web 資料流程就像是檔案資料流程，它包含資料檔案。</span><span class="sxs-lookup"><span data-stu-id="45207-111">A Web stream is like a file stream in that it contains data files.</span></span> <span data-ttu-id="45207-112">在 Web 資料流程中，這些檔案通常是 HTML 網頁以及 GIF 或 JPEG 格式的相關圖形。</span><span class="sxs-lookup"><span data-stu-id="45207-112">In a Web stream, these files are typically HTML pages and associated graphics in GIF or JPEG format.</span></span>

<span data-ttu-id="45207-113">Web 串流特別適用于以簡報形式使用的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="45207-113">Web streams can be particularly useful for ASF files that are used as presentations.</span></span> <span data-ttu-id="45207-114">在支援 Web 串流之前，簡報在檔案內的腳本資料流程中會有 Url，讓網頁可以在預定的時間載入。</span><span class="sxs-lookup"><span data-stu-id="45207-114">Prior to the support of Web streams, presentations would have URLs in script streams within a file so that a Web page would load at a predetermined time.</span></span> <span data-ttu-id="45207-115">困難之處在于網路擁塞可能會造成延遲，並建立不佳的觀賞體驗。</span><span class="sxs-lookup"><span data-stu-id="45207-115">The difficulty was that network congestion could cause delays and create a poor viewing experience.</span></span>

<span data-ttu-id="45207-116">使用 Web 串流時，Web pages 的組成部分可以包含在 ASF 檔案中作為串流。</span><span class="sxs-lookup"><span data-stu-id="45207-116">With Web streams, the constituent parts of Web pages can be included in the ASF file as a stream.</span></span> <span data-ttu-id="45207-117">當收到檔案時，可以快取這些檔案，如此一來，當命令顯示 (或轉譯) URL 時，瀏覽器就可以立即存取這些檔案。</span><span class="sxs-lookup"><span data-stu-id="45207-117">As the files are received, they can be cached so that, when the command to display (or render) a URL is delivered, they can be instantly accessed by a browser.</span></span> <span data-ttu-id="45207-118">這可讓您順暢且一致地播放。</span><span class="sxs-lookup"><span data-stu-id="45207-118">This enables smooth, consistent playback.</span></span> <span data-ttu-id="45207-119">轉譯命令會在 Web 資料流程本身中傳遞，而不是在個別資料流程中以指令碼命令的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="45207-119">The render command is delivered in the Web stream itself, not as a script command in a separate stream.</span></span>

<span data-ttu-id="45207-120">建議使用 Windows Media Format 9 系列 SDK 建立的 Web 串流，或稍後為版本號碼1提供。</span><span class="sxs-lookup"><span data-stu-id="45207-120">It is recommended that Web streams created by using the Windows Media Format 9 Series SDK, or later be given the version number 1.</span></span> <span data-ttu-id="45207-121">這個值是在 **wVersion** 成員的 [**WMT \_ WEBSTREAM \_ 格式**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)結構中指定的。</span><span class="sxs-lookup"><span data-stu-id="45207-121">This value is specified in the [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure in the **wVersion** member.</span></span> <span data-ttu-id="45207-122">SDK 本身不會執行任何動作來強制執行此版本。</span><span class="sxs-lookup"><span data-stu-id="45207-122">The SDK itself does nothing to enforce this version.</span></span>

> [!Note]  
> <span data-ttu-id="45207-123">連接到具有 Web 串流的即時廣播串流時，使用者可能會在指定的檔案實際位於本機快取之前，收到轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="45207-123">When connecting to live broadcast streams that have Web streams, it is possible that the user may receive a render command before the specified file is actually in the local cache.</span></span> <span data-ttu-id="45207-124">除非您的應用程式會處理這種狀況，否則瀏覽器會顯示「找不到頁面」錯誤。</span><span class="sxs-lookup"><span data-stu-id="45207-124">Unless your application handles this condition, the browser will display a "Page not found" error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="45207-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="45207-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45207-126">**任意資料流程**</span><span class="sxs-lookup"><span data-stu-id="45207-126">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="45207-127">**設定 Web 資料流程**</span><span class="sxs-lookup"><span data-stu-id="45207-127">**Configuring Web Streams**</span></span>](configuring-web-streams.md)
</dt> </dl>

 

 




