---
title: 將隱藏式輔助字幕新增至數位媒體
description: 將隱藏式輔助字幕新增至數位媒體
ms.assetid: 0fdd2cdc-32d4-4fda-9596-b050107abd5f
keywords:
- 'Windows Media Player，可同步的可存取媒體交換 (薩米文) '
- 'Windows Media Player 物件模型、已同步處理的可存取媒體交換 (薩米文) '
- '物件模型、同步的可存取媒體交換 (薩米) '
- 'Windows Media Player 行動裝置、已同步處理的可存取媒體交換 (薩米文) '
- 'Windows Media Player ActiveX 控制項、同步存取媒體交換 (薩米文) '
- 'Windows Media Player 的行動 ActiveX 控制項、已同步處理的可存取媒體交換 (薩米文) '
- 'ActiveX 控制項、同步的可存取媒體交換 (薩米) '
- 已同步處理的可存取媒體交換 (薩米) ，關於
- 薩米文 (同步處理的可存取媒體交換) ，關於
- Windows Media Player，新增隱藏式輔助字幕
- Windows Media Player 物件模型，加入隱藏式輔助字幕
- 物件模型，加入隱藏式輔助字幕
- Windows Media Player 行動裝置，新增隱藏式輔助字幕
- Windows Media Player ActiveX 控制項，加入隱藏式輔助字幕
- Windows Media Player 的行動 ActiveX 控制項，加入隱藏式輔助字幕
- ActiveX 控制項，加入隱藏式輔助字幕
- 已同步處理的可存取媒體交換 (薩米) ，新增隱藏式輔助字幕
- " (同步處理的可存取媒體交換) ，新增隱藏式輔助字幕"
- 新增隱藏式輔助字幕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc464fb879df1c7642cd0a04b319383654bae4aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021120"
---
# <a name="adding-closed-captions-to-digital-media"></a><span data-ttu-id="60d16-122">將隱藏式輔助字幕新增至數位媒體</span><span class="sxs-lookup"><span data-stu-id="60d16-122">Adding Closed Captions to Digital Media</span></span>

<span data-ttu-id="60d16-123">已同步處理的可存取媒體交換 (薩米) 是一種檔案格式，其設計目的是要以數位媒體內容提供同步處理的文字，例如字幕、字幕或音訊描述。</span><span class="sxs-lookup"><span data-stu-id="60d16-123">Synchronized Accessible Media Interchange (SAMI) is a file format designed to deliver synchronized text such as captions, subtitles, or audio descriptions with digital media content.</span></span> <span data-ttu-id="60d16-124">在使用 Windows Media Player 物件模型的網頁瀏覽器中整合，以薩米文提升存取範圍。</span><span class="sxs-lookup"><span data-stu-id="60d16-124">Integrated in a Web browser using the Windows Media Player object model, SAMI promotes accessibility.</span></span> <span data-ttu-id="60d16-125">藉由使用薩米文，您可以建立豐富的媒體內容，以達到更廣大、更多樣化的物件。</span><span class="sxs-lookup"><span data-stu-id="60d16-125">By using SAMI, you can create rich media content that reaches a larger, more diverse audience.</span></span>

<span data-ttu-id="60d16-126">除了標準字型，薩米文還可支援其他文字樣式，例如不同的色彩、大小或語言，以協助各種使用者。</span><span class="sxs-lookup"><span data-stu-id="60d16-126">In addition to standard fonts, SAMI can support other text styles, such as different colors, sizes, or languages to aid a variety of users.</span></span> <span data-ttu-id="60d16-127">薩米文對於視力較低的個人或聽力障礙的人特別有用。</span><span class="sxs-lookup"><span data-stu-id="60d16-127">SAMI can be particularly useful for individuals who have low vision or those who are deaf or hard-of-hearing.</span></span> <span data-ttu-id="60d16-128">薩米文的格式也可協助教育用途，例如教學學生的第二種語言。</span><span class="sxs-lookup"><span data-stu-id="60d16-128">The SAMI format can also assist in educational purposes, such as teaching students a second language.</span></span>

<span data-ttu-id="60d16-129">本主題著重于將薩米和 Windows Media Player 的 ActiveX 控制項物件模型合併。</span><span class="sxs-lookup"><span data-stu-id="60d16-129">This topic focuses on the incorporation of SAMI with the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="60d16-130">薩米文檔案與數位媒體檔案分開存在，而且不依賴特定的影片或音訊格式來運作。</span><span class="sxs-lookup"><span data-stu-id="60d16-130">SAMI files exist independently from digital media files and do not rely on a specific video or audio format to function.</span></span> <span data-ttu-id="60d16-131">由於檔案是分開的，因此 Windows Media Player 控制項將會在用戶端電腦上尋找、剖析、同步處理和轉譯每個檔案。</span><span class="sxs-lookup"><span data-stu-id="60d16-131">Since the files are separate, the Windows Media Player control will locate, parse, synchronize, and render each file on the client's computer.</span></span> <span data-ttu-id="60d16-132">這可提供額外的彈性和功能，因為它可讓您編輯個別的薩米文檔案、使用不同的數位媒體格式來合併薩米文檔案，以及將薩米的檔案儲存在不同的伺服器位置。</span><span class="sxs-lookup"><span data-stu-id="60d16-132">This provides for added flexibility and functionality because it allows for the editing of individual SAMI files, the incorporation of the SAMI file with different digital media formats, and the storage of SAMI files on different server locations.</span></span>

<span data-ttu-id="60d16-133">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="60d16-133">This topic contains the following sections.</span></span>



| <span data-ttu-id="60d16-134">區段</span><span class="sxs-lookup"><span data-stu-id="60d16-134">Section</span></span>                                                                                                                            | <span data-ttu-id="60d16-135">描述</span><span class="sxs-lookup"><span data-stu-id="60d16-135">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60d16-136">關於薩米文的檔案</span><span class="sxs-lookup"><span data-stu-id="60d16-136">About SAMI Files</span></span>](about-sami-files.md)                                                                                           | <span data-ttu-id="60d16-137">描述薩米文檔案的基本結構。</span><span class="sxs-lookup"><span data-stu-id="60d16-137">Describes the basic structure of SAMI files.</span></span>                                               |
| [<span data-ttu-id="60d16-138">薩米文檔案範例</span><span class="sxs-lookup"><span data-stu-id="60d16-138">SAMI File Example</span></span>](sami-file-example.md)                                                                                         | <span data-ttu-id="60d16-139">描述範例薩米文檔案的結構。</span><span class="sxs-lookup"><span data-stu-id="60d16-139">Describes the structure of an example SAMI file.</span></span>                                           |
| [<span data-ttu-id="60d16-140">在瀏覽器中搭配 Windows Media Player 控制項使用薩米文</span><span class="sxs-lookup"><span data-stu-id="60d16-140">Using SAMI with the Windows Media Player Control in a Browser</span></span>](using-sami-with-the-windows-media-player-control-in-a-browser.md) | <span data-ttu-id="60d16-141">說明如何在網頁中使用帶 Windows Media Player 控制項的薩米文。</span><span class="sxs-lookup"><span data-stu-id="60d16-141">Describes how to use SAMI in a webpage with the Windows Media Player control.</span></span>              |
| [<span data-ttu-id="60d16-142">關於薩米文的 Url</span><span class="sxs-lookup"><span data-stu-id="60d16-142">About SAMI URLs</span></span>](about-sami-urls.md)                                                                                             | <span data-ttu-id="60d16-143">說明如何使用單一 URL，將數位媒體檔案與薩米文檔案相關聯。</span><span class="sxs-lookup"><span data-stu-id="60d16-143">Describes how digital media files can be associated with SAMI files by using a single URL.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="60d16-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="60d16-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60d16-145">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="60d16-145">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




