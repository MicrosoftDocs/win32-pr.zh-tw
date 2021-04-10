---
title: Windows Media 中繼檔指南
description: Windows Media 中繼檔指南
ms.assetid: d2360a63-f073-44b0-8637-1f22b577f51a
keywords:
- Windows Media 中繼檔，關於
- Windows Media Player，中繼檔
- Windows Media Player，Windows Media 中繼檔
- 中繼檔，關於
- Windows Media，中繼檔
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
ms.openlocfilehash: fcf0a4c98ae49d1cdf3b7e36e8a278f184cd4632
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932524"
---
# <a name="windows-media-metafile-guide"></a><span data-ttu-id="f4604-111">Windows Media 中繼檔指南</span><span class="sxs-lookup"><span data-stu-id="f4604-111">Windows Media Metafile Guide</span></span>

<span data-ttu-id="f4604-112">Windows Media 中繼檔可以像您需要的一樣簡單或複雜。</span><span class="sxs-lookup"><span data-stu-id="f4604-112">A Windows Media metafile can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="f4604-113">最基本的 Windows Media 中繼檔只包含伺服器上某些多媒體內容 (URL) 的統一資源定位器。</span><span class="sxs-lookup"><span data-stu-id="f4604-113">The most basic Windows Media metafile contains only the Uniform Resource Locator (URL) of some multimedia content on a server.</span></span> <span data-ttu-id="f4604-114">用戶端 Windows Media Player 會剖析此資訊，然後開啟 Windows Media 中繼檔中定義的媒體檔案或資料流程。</span><span class="sxs-lookup"><span data-stu-id="f4604-114">The client, Windows Media Player, parses this information and then opens the media file or stream defined in the Windows Media metafile.</span></span> <span data-ttu-id="f4604-115">複雜的中繼檔可以包含播放清單中排列的多個檔案或資料流程、如何播放檔案或資料流程的指示、文字和圖形元素，例如標題、作者和著作權文字、個人化廣告插入至即時資料流、與 Windows Media Player 介面上的專案相關聯的超連結等等。</span><span class="sxs-lookup"><span data-stu-id="f4604-115">A complex metafile can contain multiple files or streams arranged in a playlist, instructions on how to play the files or streams, text and graphic elements such as title, author, and copyright text, personalized ad insertion into a live stream, hyperlinks associated with elements on the Windows Media Player interface, and more.</span></span>

<span data-ttu-id="f4604-116">下列各節提供有關如何建立及使用 Windows Media 中繼檔播放清單的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f4604-116">The following sections provide detailed information on how to create and use Windows Media metafile playlists.</span></span>



| <span data-ttu-id="f4604-117">區段</span><span class="sxs-lookup"><span data-stu-id="f4604-117">Section</span></span>                                                            | <span data-ttu-id="f4604-118">描述</span><span class="sxs-lookup"><span data-stu-id="f4604-118">Description</span></span>                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4604-119">播放清單的類型</span><span class="sxs-lookup"><span data-stu-id="f4604-119">Types of Playlists</span></span>](types-of-playlists.md)                       | <span data-ttu-id="f4604-120">列出可用的副檔名。</span><span class="sxs-lookup"><span data-stu-id="f4604-120">Lists available file name extensions.</span></span>                                               |
| [<span data-ttu-id="f4604-121">建立中繼檔播放清單</span><span class="sxs-lookup"><span data-stu-id="f4604-121">Creating Metafile Playlists</span></span>](creating-metafile-playlists.md)     | <span data-ttu-id="f4604-122">說明如何建立 Windows Media 中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="f4604-122">Describes how to create Windows Media metafile playlists.</span></span>                           |
| [<span data-ttu-id="f4604-123">中繼檔播放清單</span><span class="sxs-lookup"><span data-stu-id="f4604-123">Metafile Playlists</span></span>](metafile-playlists.md)                       | <span data-ttu-id="f4604-124">描述中繼檔播放清單使用方式、腳本、中繼資料和處理。</span><span class="sxs-lookup"><span data-stu-id="f4604-124">Describes metafile playlist usage, scripting, metadata, and processing.</span></span>             |
| [<span data-ttu-id="f4604-125">中繼檔延伸指導方針</span><span class="sxs-lookup"><span data-stu-id="f4604-125">Metafile Extension Guidelines</span></span>](metafile-extension-guidelines.md) | <span data-ttu-id="f4604-126">描述針對串流處理媒體檔案的副檔名慣用用法。</span><span class="sxs-lookup"><span data-stu-id="f4604-126">Describes the preferred use of file name extensions for streaming media files.</span></span>      |
| [<span data-ttu-id="f4604-127">優先順序</span><span class="sxs-lookup"><span data-stu-id="f4604-127">Order of Precedence</span></span>](order-of-precedence.md)                     | <span data-ttu-id="f4604-128">描述中繼檔播放清單元素如何覆寫其他中繼檔播放清單元素。</span><span class="sxs-lookup"><span data-stu-id="f4604-128">Describes how metafile playlist elements override other metafile playlist elements.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f4604-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="f4604-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4604-130">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="f4604-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f4604-131">**Windows Media 中繼檔**</span><span class="sxs-lookup"><span data-stu-id="f4604-131">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




