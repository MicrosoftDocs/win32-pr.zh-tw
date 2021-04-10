---
title: Advanced 播放清單
description: Advanced 播放清單
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
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
- Windows Media 中繼檔播放清單，advanced 播放清單範例
- 播放清單、advanced 播放清單範例
- 中繼檔播放清單，advanced 播放清單範例
- Windows Media Player，播放清單範例
- Windows Media Player，範例播放清單
- Windows Media Player，範例播放清單
- Windows Media Player，advanced 播放清單範例
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021238"
---
# <a name="an-advanced-playlist"></a><span data-ttu-id="6b708-125">Advanced 播放清單</span><span class="sxs-lookup"><span data-stu-id="6b708-125">An Advanced Playlist</span></span>

<span data-ttu-id="6b708-126">下列播放清單範例顯示如何使用一組更完整的播放清單元素。</span><span class="sxs-lookup"><span data-stu-id="6b708-126">The following playlist example shows how to use a more complete set of playlist elements.</span></span> <span data-ttu-id="6b708-127">撰寫您自己的程式碼時，您必須將所有 Url 和檔案名變更為有效的檔案名，而您的 Windows Media Player 可以存取這些名稱。</span><span class="sxs-lookup"><span data-stu-id="6b708-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="6b708-128">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="6b708-128">Example Code</span></span>


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="6b708-129">下表描述上述的 advanced 播放清單。</span><span class="sxs-lookup"><span data-stu-id="6b708-129">The following table describes the preceding advanced playlist.</span></span>



| <span data-ttu-id="6b708-130">線條</span><span class="sxs-lookup"><span data-stu-id="6b708-130">Line</span></span>                                                                                            | <span data-ttu-id="6b708-131">Description</span><span class="sxs-lookup"><span data-stu-id="6b708-131">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | <span data-ttu-id="6b708-132">[ASX](asx-element.md)元素會識別用戶端 (Windows Media Player) 這是 Windows Media 中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="6b708-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="6b708-133">**Version** 屬性會指定中繼檔元素的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6b708-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | <span data-ttu-id="6b708-134">[Title](title-element--metafile.md)元素會識別播放清單的整體標題。</span><span class="sxs-lookup"><span data-stu-id="6b708-134">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="6b708-135">Windows Media Player 會將此中繼資料顯示為 [顯示標題]。</span><span class="sxs-lookup"><span data-stu-id="6b708-135">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | <span data-ttu-id="6b708-136">[ABSTRACT](abstract-element.md)元素提供顯示標題的工具提示。</span><span class="sxs-lookup"><span data-stu-id="6b708-136">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the show title.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | <span data-ttu-id="6b708-137">[MOREINFO](moreinfo-element.md)元素會將顯示標題連結到 URL。</span><span class="sxs-lookup"><span data-stu-id="6b708-137">The [MOREINFO](moreinfo-element.md) element links the show title to an URL.</span></span> <span data-ttu-id="6b708-138">如果已定義工具提示，則將滑鼠指標暫停在顯示標題上方即可存取工具提示。</span><span class="sxs-lookup"><span data-stu-id="6b708-138">Pausing the mouse pointer over the show title accesses the ToolTip, if defined.</span></span> <span data-ttu-id="6b708-139">選取 [顯示標題] 之後，就會開啟指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b708-139">Selecting the show title will then open the designated URL.</span></span>                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | <span data-ttu-id="6b708-140">[橫幅](banner-element.md)元素會在 Windows Media Player 中建立廣告橫幅。</span><span class="sxs-lookup"><span data-stu-id="6b708-140">The [BANNER](banner-element.md) element creates an advertising banner in Windows Media Player.</span></span> <span data-ttu-id="6b708-141">**HREF** 屬性指定橫幅圖形 (必須是194圖元寬、32圖元高) 。</span><span class="sxs-lookup"><span data-stu-id="6b708-141">The **HREF** attribute specifies the banner graphic (which must be 194 pixels wide by 32 pixels tall).</span></span>                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | <span data-ttu-id="6b708-142">[ABSTRACT](abstract-element.md)元素提供 **橫幅** 的工具提示。</span><span class="sxs-lookup"><span data-stu-id="6b708-142">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the **BANNER**.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | <span data-ttu-id="6b708-143">[MOREINFO](moreinfo-element.md)元素會將 **橫幅** 圖形連結到 URL。</span><span class="sxs-lookup"><span data-stu-id="6b708-143">The [MOREINFO](moreinfo-element.md) element links the **BANNER** graphic to a URL.</span></span> <span data-ttu-id="6b708-144">如果有定義工具提示，請將滑鼠指標放在 **橫幅** 上來存取工具提示。</span><span class="sxs-lookup"><span data-stu-id="6b708-144">Holding the mouse pointer over the **BANNER** accesses a ToolTip, if defined.</span></span> <span data-ttu-id="6b708-145">選取 **橫幅** 會開啟指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b708-145">Selecting the **BANNER** will open the designated URL.</span></span>                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | <span data-ttu-id="6b708-146">[PARAM](param-element.md)元素定義自訂參數。</span><span class="sxs-lookup"><span data-stu-id="6b708-146">The [PARAM](param-element.md) element defines a custom parameter.</span></span> <span data-ttu-id="6b708-147">**Name** 屬性會將自訂參數的名稱定義為「track」。</span><span class="sxs-lookup"><span data-stu-id="6b708-147">The **name** attribute defines the name of the custom parameter as "track".</span></span> <span data-ttu-id="6b708-148">**Value** 屬性會將 "track" 的值定義為 "1"。</span><span class="sxs-lookup"><span data-stu-id="6b708-148">The **value** attribute defines the value of "track" to be "1".</span></span>                                                                                                                          |
| `</BANNER>`                                                                                 | <span data-ttu-id="6b708-149">關閉 **橫幅** 元素</span><span class="sxs-lookup"><span data-stu-id="6b708-149">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | <span data-ttu-id="6b708-150">開始 [輸入](entry-element.md) 元素區塊。</span><span class="sxs-lookup"><span data-stu-id="6b708-150">Begins the [ENTRY](entry-element.md) element block.</span></span> <span data-ttu-id="6b708-151">這個元素會藉由指定 **REF** 元素中的連結，來定義播放清單中的剪輯。</span><span class="sxs-lookup"><span data-stu-id="6b708-151">This element defines a clip in a playlist by specifying a link in the **REF** element.</span></span> <span data-ttu-id="6b708-152">將 **ClientSkip** 設定為 [否] 表示使用者無法向前快轉或跳到下一個剪輯</span><span class="sxs-lookup"><span data-stu-id="6b708-152">Setting **ClientSkip** to "no" means that the user cannot fast forward or jump to the next clip</span></span>                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | <span data-ttu-id="6b708-153">建立廣告橫幅。</span><span class="sxs-lookup"><span data-stu-id="6b708-153">Creates an advertising banner.</span></span> <span data-ttu-id="6b708-154">**HREF** 是橫幅圖形 (194x32 圖元) 。</span><span class="sxs-lookup"><span data-stu-id="6b708-154">The **HREF** is the banner graphic (194x32 pixels).</span></span>                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | <span data-ttu-id="6b708-155">提供橫幅的工具提示。</span><span class="sxs-lookup"><span data-stu-id="6b708-155">Provides the ToolTip for the banner.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="6b708-156">提供橫幅 URL 的連結。</span><span class="sxs-lookup"><span data-stu-id="6b708-156">Provides a link to the URL for the banner.</span></span> <span data-ttu-id="6b708-157">選取橫幅會連接到 URL。</span><span class="sxs-lookup"><span data-stu-id="6b708-157">Selecting the banner connects to the URL.</span></span>                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | <span data-ttu-id="6b708-158">關閉 **橫幅** 元素</span><span class="sxs-lookup"><span data-stu-id="6b708-158">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="6b708-159">提供剪輯 **標題** 文字 URL 的連結。</span><span class="sxs-lookup"><span data-stu-id="6b708-159">Provides a link to the URL for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | <span data-ttu-id="6b708-160">註解。</span><span class="sxs-lookup"><span data-stu-id="6b708-160">A comment.</span></span> <span data-ttu-id="6b708-161">只有在程式碼被查看時，才會顯示[批註](comments.md)。</span><span class="sxs-lookup"><span data-stu-id="6b708-161">[Comments](comments.md) are only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | <span data-ttu-id="6b708-162">提供剪輯 **標題** 文字的工具提示。</span><span class="sxs-lookup"><span data-stu-id="6b708-162">Provides the ToolTip for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | <span data-ttu-id="6b708-163">識別剪輯的標題。</span><span class="sxs-lookup"><span data-stu-id="6b708-163">Identifies the title of the clip.</span></span> <span data-ttu-id="6b708-164">這是剪輯 **標題** ，因為它是在 **專案專案** 內進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="6b708-164">It is the clip **TITLE** because it is nested within an **ENTRY** element.</span></span> <span data-ttu-id="6b708-165">Windows Media Player 會將此中繼資料顯示為剪輯標題。</span><span class="sxs-lookup"><span data-stu-id="6b708-165">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | <span data-ttu-id="6b708-166">識別媒體剪輯的作者。</span><span class="sxs-lookup"><span data-stu-id="6b708-166">Identifies the author of the media clip.</span></span> <span data-ttu-id="6b708-167">Windows Media Player，此中繼資料會顯示為剪輯 **作者** 。</span><span class="sxs-lookup"><span data-stu-id="6b708-167">This metadata is displayed as the clip **AUTHOR** by Windows Media Player.</span></span>                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | <span data-ttu-id="6b708-168">[著作權](copyright-element.md)元素會指定與媒體剪輯相關聯的著作權。</span><span class="sxs-lookup"><span data-stu-id="6b708-168">The [COPYRIGHT](copyright-element.md) element specifies the copyrights associated with the media clip.</span></span> <span data-ttu-id="6b708-169">Windows Media Player 會將此中繼資料顯示為剪輯著作權。</span><span class="sxs-lookup"><span data-stu-id="6b708-169">Windows Media Player displays this metadata as the clip COPYRIGHT.</span></span>                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="6b708-170">與 **XML** 批註相同格式的批註。</span><span class="sxs-lookup"><span data-stu-id="6b708-170">A comment, in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | <span data-ttu-id="6b708-171">媒體內容的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b708-171">URL for the media content.</span></span> <span data-ttu-id="6b708-172">[REF](ref-element.md)元素會將該行識別為媒體內容的指標。</span><span class="sxs-lookup"><span data-stu-id="6b708-172">The [REF](ref-element.md) element identifies the line as a pointer to media content.</span></span> <span data-ttu-id="6b708-173">**HREF** 屬性是檔案的 URL。請注意，使用類似 XML 的元素 "/>" 而非 " &lt; /REF &gt; "。</span><span class="sxs-lookup"><span data-stu-id="6b708-173">The **HREF** attribute is the URL to the file.Note the use of the XML-like closing of the element , "/>" instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="6b708-174">因為這個元素沒有子專案，所以它會自行關閉。</span><span class="sxs-lookup"><span data-stu-id="6b708-174">Because this element does not have child elements, it closes itself.</span></span><br/> |
| `</ENTRY>`                                                                                  | <span data-ttu-id="6b708-175">指定第一個 **專案** 元素的結尾。</span><span class="sxs-lookup"><span data-stu-id="6b708-175">Specifies the end of the of the first **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | <span data-ttu-id="6b708-176">開始第二個 **ENTRY** 元素。</span><span class="sxs-lookup"><span data-stu-id="6b708-176">Begins the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | <span data-ttu-id="6b708-177">識別第二個剪輯的標題。</span><span class="sxs-lookup"><span data-stu-id="6b708-177">Identifies the title of the second clip.</span></span>                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | <span data-ttu-id="6b708-178">識別第二個媒體剪輯的作者。</span><span class="sxs-lookup"><span data-stu-id="6b708-178">Identifies the author of the second media clip.</span></span>                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | <span data-ttu-id="6b708-179">註解。</span><span class="sxs-lookup"><span data-stu-id="6b708-179">A comment.</span></span> <span data-ttu-id="6b708-180">只有在程式碼被查看時，才會顯示。</span><span class="sxs-lookup"><span data-stu-id="6b708-180">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | <span data-ttu-id="6b708-181">這是剪輯 **標題** 文字的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="6b708-181">This is the ToolTip text for the **TITLE** text of the clip.</span></span>                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="6b708-182">註解。</span><span class="sxs-lookup"><span data-stu-id="6b708-182">A comment.</span></span> <span data-ttu-id="6b708-183">只有在程式碼被查看時，才會顯示。</span><span class="sxs-lookup"><span data-stu-id="6b708-183">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | <span data-ttu-id="6b708-184">將該行識別為媒體內容的指標。</span><span class="sxs-lookup"><span data-stu-id="6b708-184">Identifies the line as a pointer to media content.</span></span> <span data-ttu-id="6b708-185">**HREF** 屬性是檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b708-185">The **HREF** attribute is the URL to the file.</span></span>                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | <span data-ttu-id="6b708-186">指定第二個 **ENTRY** 元素的結尾。</span><span class="sxs-lookup"><span data-stu-id="6b708-186">Specifies the end of the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | <span data-ttu-id="6b708-187">指定播放清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="6b708-187">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6b708-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b708-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b708-189">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="6b708-189">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6b708-190">**範例播放清單**</span><span class="sxs-lookup"><span data-stu-id="6b708-190">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="6b708-191">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="6b708-191">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6b708-192">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="6b708-192">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6b708-193">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="6b708-193">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





