---
title: 重新導向
description: 重新導向
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Media 中繼檔播放清單，重新導向
- 播放清單，重新導向
- 中繼檔播放清單，重新導向
- Windows Media Player，重新導向
- 重新導向
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300164"
---
# <a name="redirection"></a><span data-ttu-id="7b710-108">重新導向</span><span class="sxs-lookup"><span data-stu-id="7b710-108">Redirection</span></span>

<span data-ttu-id="7b710-109">播放清單會將瀏覽器重新導向至 Windows Media Player，以播放指定的媒體串流或媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="7b710-109">The playlist will redirect the browser to Windows Media Player to play the designated media stream or media file.</span></span> <span data-ttu-id="7b710-110">最基本的中繼檔播放清單只包含媒體檔案 (URL) 的統一資源定位器。</span><span class="sxs-lookup"><span data-stu-id="7b710-110">The most basic metafile playlist contains only the Uniform Resource Locator (URL) of a media file.</span></span>

<span data-ttu-id="7b710-111">若要建立基本的中繼檔播放清單，請開啟您慣用的文字編輯器（例如 Microsoft 記事本），然後輸入下列範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="7b710-111">To create a basic metafile playlist, open your favorite text editor, such as Microsoft Notepad, and type the following example code.</span></span>


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



<span data-ttu-id="7b710-112">使用下表中的語法取代 Windows Media 檔案的有效路徑。</span><span class="sxs-lookup"><span data-stu-id="7b710-112">Substitute a valid path to your Windows Media file using the syntax in the following table.</span></span>



| <span data-ttu-id="7b710-113">內容來源</span><span class="sxs-lookup"><span data-stu-id="7b710-113">Source of content</span></span>                                                                                 | <span data-ttu-id="7b710-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b710-114">Syntax</span></span>                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="7b710-115">內容是 Windows Media 伺服器上的檔案</span><span class="sxs-lookup"><span data-stu-id="7b710-115">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="7b710-116">mms://ServerName/Path/FileName.wma</span><span class="sxs-lookup"><span data-stu-id="7b710-116">mms://ServerName/Path/FileName.wma</span></span>        |
| <span data-ttu-id="7b710-117">內容是從 Windows Media 站存取的廣播多播</span><span class="sxs-lookup"><span data-stu-id="7b710-117">Content is a broadcast multicast that is accessed from a Windows Media station</span></span>                    | https://WebServerName/Stations/kxyz.nsc    |
| <span data-ttu-id="7b710-118">內容是從 Windows Media 伺服器上的發行端點存取的廣播單播</span><span class="sxs-lookup"><span data-stu-id="7b710-118">Content is a broadcast unicast that is accessed from a publishing point on a Windows Media server</span></span> | <span data-ttu-id="7b710-119">mms://ServerName/PublishingPointAlias</span><span class="sxs-lookup"><span data-stu-id="7b710-119">mms://ServerName/PublishingPointAlias</span></span>     |
| <span data-ttu-id="7b710-120">內容是 web 伺服器上的檔案</span><span class="sxs-lookup"><span data-stu-id="7b710-120">Content is a file on a web server</span></span>                                                                 | https://WebServerName/Path/Filename.wma    |
| <span data-ttu-id="7b710-121">內容是本機硬碟上的檔案</span><span class="sxs-lookup"><span data-stu-id="7b710-121">Content is a file on a local hard disk</span></span>                                                            | <span data-ttu-id="7b710-122">file://c： \\ 路徑 \\ 檔案名 .wma</span><span class="sxs-lookup"><span data-stu-id="7b710-122">file://c:\\Path\\Filename.wma</span></span>             |
| <span data-ttu-id="7b710-123">內容是網路共用上的檔案</span><span class="sxs-lookup"><span data-stu-id="7b710-123">Content is a file on a network share</span></span>                                                              | <span data-ttu-id="7b710-124">file:// \\ \\ ServerName \\ 路徑 \\ 檔案名 .wma</span><span class="sxs-lookup"><span data-stu-id="7b710-124">file://\\\\ServerName\\Path\\Filename.wma</span></span> |
| <span data-ttu-id="7b710-125">內容是 Windows Media 伺服器上的檔案</span><span class="sxs-lookup"><span data-stu-id="7b710-125">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="7b710-126">mms://ServerName/Path/FileName.wmv</span><span class="sxs-lookup"><span data-stu-id="7b710-126">mms://ServerName/Path/FileName.wmv</span></span>        |



 

<span data-ttu-id="7b710-127">使用 [[副檔名] 中所](file-name-extensions.md)述的檔案名和副檔名來儲存您所建立的檔案。</span><span class="sxs-lookup"><span data-stu-id="7b710-127">Save the file you have created with a file name and extension as described in [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="7b710-128">在 Windows 檔案總管中按兩下它。</span><span class="sxs-lookup"><span data-stu-id="7b710-128">Double-click it in Windows Explorer.</span></span> <span data-ttu-id="7b710-129">Windows Media Player 應開啟並開始串流處理內容。</span><span class="sxs-lookup"><span data-stu-id="7b710-129">Windows Media Player should open and start streaming the content.</span></span> <span data-ttu-id="7b710-130">您可以將檔案連同網頁一起儲存至 web 伺服器，並使用 **HREF** 元素連結到該檔案，或使用 Windows Media Player **物件** 標記將它內嵌在網頁中。</span><span class="sxs-lookup"><span data-stu-id="7b710-130">You can save the file to your web server, along with your webpages, and link to it with an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** tag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b710-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b710-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b710-132">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="7b710-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="7b710-133">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="7b710-133">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="7b710-134">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="7b710-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7b710-135">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="7b710-135">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




