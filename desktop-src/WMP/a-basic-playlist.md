---
title: 基本播放清單
description: 基本播放清單
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Windows Media 中繼檔播放清單，基本播放清單範例
- 播放清單、基本播放清單範例
- 中繼檔播放清單，基本播放清單範例
- Windows Media Player，播放清單範例
- Windows Media Player，範例播放清單
- Windows Media Player，範例播放清單
- Windows Media Player，基本播放清單範例
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314781"
---
# <a name="a-basic-playlist"></a><span data-ttu-id="59414-125">基本播放清單</span><span class="sxs-lookup"><span data-stu-id="59414-125">A Basic Playlist</span></span>

<span data-ttu-id="59414-126">下列播放清單範例顯示一組基本的播放清單元素。</span><span class="sxs-lookup"><span data-stu-id="59414-126">The following playlist example shows a basic set of playlist elements.</span></span> <span data-ttu-id="59414-127">撰寫您自己的程式碼時，您必須將所有 Url 和檔案名變更為有效的檔案名，而您的 Windows Media Player 可以存取這些名稱。</span><span class="sxs-lookup"><span data-stu-id="59414-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="59414-128">**程式碼範例**</span><span class="sxs-lookup"><span data-stu-id="59414-128">**Code Example**</span></span>


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="59414-129">下表提供在範例程式碼中使用每個元素的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="59414-129">The following table provides details on the use of each element in the example code.</span></span>



| <span data-ttu-id="59414-130">線條</span><span class="sxs-lookup"><span data-stu-id="59414-130">Line</span></span>                                                                                            | <span data-ttu-id="59414-131">描述</span><span class="sxs-lookup"><span data-stu-id="59414-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | <span data-ttu-id="59414-132">[ASX](asx-element.md)元素會識別用戶端 (Windows Media Player) 這是 Windows Media 中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="59414-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="59414-133">**Version** 屬性會指定中繼檔元素的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="59414-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="59414-134">\<TITLE>基本播放清單示範\</TITLE></span><span class="sxs-lookup"><span data-stu-id="59414-134">\<TITLE>Basic Playlist Demo\</TITLE></span></span>                                                  | <span data-ttu-id="59414-135">[Title](title-element--metafile.md)元素會識別播放清單的整體標題。</span><span class="sxs-lookup"><span data-stu-id="59414-135">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="59414-136">Windows Media Player 會將此中繼資料顯示為 [顯示標題]。</span><span class="sxs-lookup"><span data-stu-id="59414-136">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | <span data-ttu-id="59414-137">開始 [輸入](entry-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="59414-137">Begins the [ENTRY](entry-element.md) element.</span></span> <span data-ttu-id="59414-138">**ENTRY** 元素是在播放清單中定義特定剪輯的方式</span><span class="sxs-lookup"><span data-stu-id="59414-138">An **ENTRY** element is a way to define a particular clip in a playlist</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="59414-139">\<TITLE>基本播放清單中的專案\</TITLE></span><span class="sxs-lookup"><span data-stu-id="59414-139">\<TITLE>An Entry in a basic playlist\</TITLE></span></span>                                         | <span data-ttu-id="59414-140">識別播放清單剪輯的標題。</span><span class="sxs-lookup"><span data-stu-id="59414-140">Identifies the title of the playlist clip .</span></span> <span data-ttu-id="59414-141">它與先前的 **TITLE** 元素不同，因為這個專案是在 **專案專案** 內進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="59414-141">It is different than the previous **TITLE** element because this one is nested within an **ENTRY** element.</span></span> <span data-ttu-id="59414-142">Windows Media Player 會將此中繼資料顯示為剪輯標題。</span><span class="sxs-lookup"><span data-stu-id="59414-142">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="59414-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span><span class="sxs-lookup"><span data-stu-id="59414-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span></span>                                              | <span data-ttu-id="59414-144">[Author](author-element.md)元素會識別 media 剪輯的作者。</span><span class="sxs-lookup"><span data-stu-id="59414-144">The [AUTHOR](author-element.md) element identifies the author of the media clip .</span></span> <span data-ttu-id="59414-145">Windows Media Player 會將此中繼資料顯示為剪輯 **作者**。</span><span class="sxs-lookup"><span data-stu-id="59414-145">Windows Media Player displays this metadata as the clip **AUTHOR**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | <span data-ttu-id="59414-146">註解。</span><span class="sxs-lookup"><span data-stu-id="59414-146">A comment.</span></span> <span data-ttu-id="59414-147">只有在程式碼被查看，而且格式與 **XML** 批註相同時，才會顯示 [批註](comments.md)。</span><span class="sxs-lookup"><span data-stu-id="59414-147">[Comments](comments.md) are visible only when the code is viewed, and are in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | <span data-ttu-id="59414-148">媒體檔案的實際指標。</span><span class="sxs-lookup"><span data-stu-id="59414-148">Actual pointer to the media file.</span></span> <span data-ttu-id="59414-149">[REF](ref-element.md)元素會將該行識別為媒體內容的指標，而 **HREF** 屬性則是媒體檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="59414-149">The [REF](ref-element.md) element identifies the line as a pointer to media content, while the **HREF** attribute is the URL to the media file.</span></span> <span data-ttu-id="59414-150">在此情況下，URL 會使用 MMS 通訊協定，因此它會指向 Windows Media 伺服器。媒體伺服器上的媒體檔案通常不會與您的 HTML 檔案保存在相同的位置。</span><span class="sxs-lookup"><span data-stu-id="59414-150">In this case, the URL uses the MMS protocol, so it points to a Windows Media server.Media files on your media server are not usually kept in the same location as your HTML documents.</span></span><br/> <span data-ttu-id="59414-151">請注意，使用類似 XML 的元素 "/>"，而不是 " &lt; /REF &gt; "。</span><span class="sxs-lookup"><span data-stu-id="59414-151">Note the use of the XML-like closing of the element , "/>", instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="59414-152">因為這個元素沒有子專案，所以它會自行關閉。</span><span class="sxs-lookup"><span data-stu-id="59414-152">Because this element does not have child elements, it closes itself.</span></span><br/> |
| \</ENTRY>                                                                                  | <span data-ttu-id="59414-153">指定 **ENTRY** 元素的結尾。</span><span class="sxs-lookup"><span data-stu-id="59414-153">Specifies the end of the **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | <span data-ttu-id="59414-154">指定播放清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="59414-154">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="59414-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="59414-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59414-156">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="59414-156">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="59414-157">**範例播放清單**</span><span class="sxs-lookup"><span data-stu-id="59414-157">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="59414-158">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="59414-158">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="59414-159">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="59414-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="59414-160">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="59414-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





