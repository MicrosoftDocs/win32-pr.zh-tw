---
title: 範例無線電站播放清單
description: 範例無線電站播放清單
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows Media 中繼檔播放清單、播放清單範例
- 播放清單、播放清單範例
- 中繼檔播放清單，播放清單範例
- Windows Media 中繼檔播放清單，範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows Media 中繼檔播放清單、範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows Media 中繼檔播放清單，程式碼範例
- 播放清單，程式碼範例
- 中繼檔播放清單，程式碼範例
- Windows Media 中繼檔播放清單，無線電站播放清單範例
- 播放清單、無線電站播放清單範例
- 中繼檔播放清單，無線電站播放清單範例
- Windows Media Player，播放清單範例
- Windows Media Player，範例播放清單
- Windows Media Player，範例播放清單
- Windows Media Player，無線電站播放清單範例
- 播放清單範例
- 範例播放清單
- 範例播放清單
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372068"
---
# <a name="an-example-radio-station-playlist"></a><span data-ttu-id="58842-125">範例無線電站播放清單</span><span class="sxs-lookup"><span data-stu-id="58842-125">An Example Radio Station Playlist</span></span>

<span data-ttu-id="58842-126">下列範例程式碼說明如何建立播放清單來掃描三個岩石電臺電臺。</span><span class="sxs-lookup"><span data-stu-id="58842-126">The following example code illustrates how to create a playlist to scan three rock radio stations.</span></span> <span data-ttu-id="58842-127">虛構的公司艾德作品無線電品牌位於播放清單上，以及播放清單中所有個別的串流。</span><span class="sxs-lookup"><span data-stu-id="58842-127">The fictitious company Adventure Works Radio brand is on the playlist and on all of the individual streams within the playlist.</span></span> <span data-ttu-id="58842-128">當您撰寫程式碼時，請將所有 Url 和檔案名變更為可存取 Windows Media Player 的有效檔案名。</span><span class="sxs-lookup"><span data-stu-id="58842-128">When you write your code, change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="58842-129">每個工作站都會建立播放清單。</span><span class="sxs-lookup"><span data-stu-id="58842-129">A playlist is created for each of the stations.</span></span> <span data-ttu-id="58842-130">第四個播放清單會掃描前三個播放清單。</span><span class="sxs-lookup"><span data-stu-id="58842-130">A fourth playlist scans through the first three.</span></span> <span data-ttu-id="58842-131">系統會建立播放清單，以參考動態產生的廣告，並具有「艾德作品」無線電商標。</span><span class="sxs-lookup"><span data-stu-id="58842-131">The playlists are created to reference dynamically generated advertisements and have Adventure Works Radio branding.</span></span>

<span data-ttu-id="58842-132">其中一個代表電臺的播放清單可能如下所示。</span><span class="sxs-lookup"><span data-stu-id="58842-132">One of the playlists representing a radio station might look like this.</span></span>


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="58842-133">接著可以將播放清單視為個別播放清單的參考。</span><span class="sxs-lookup"><span data-stu-id="58842-133">The playlist can then be constructed of references to the individual playlists.</span></span>

<span data-ttu-id="58842-134">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="58842-134">Example Code</span></span>


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



<span data-ttu-id="58842-135">此範例會在每個所參考的三個電臺中，每一個都有30秒的時間來播放廣告。</span><span class="sxs-lookup"><span data-stu-id="58842-135">This example would play an ad followed by 30 seconds of each of the three stations referenced, one after the other.</span></span> <span data-ttu-id="58842-136">這個週期將會無限期重複，因為未定義 **重複** 專案的 **COUNT** 屬性。</span><span class="sxs-lookup"><span data-stu-id="58842-136">This cycle will repeat indefinitely because the **COUNT** attribute of the **REPEAT** element is not defined.</span></span>

-   <span data-ttu-id="58842-137">本文所述之公司、組織、產品、人物及事件均屬虛構，</span><span class="sxs-lookup"><span data-stu-id="58842-137">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="58842-138">並非影射任何真實的公司、組織、產品、人物或事件。</span><span class="sxs-lookup"><span data-stu-id="58842-138">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58842-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="58842-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58842-140">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="58842-140">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="58842-141">**範例播放清單**</span><span class="sxs-lookup"><span data-stu-id="58842-141">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="58842-142">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="58842-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="58842-143">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="58842-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="58842-144">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="58842-144">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




