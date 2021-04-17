---
title: 建立中繼檔播放清單
description: 建立中繼檔播放清單
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows Media 中繼檔播放清單，建立
- 播放清單，建立
- 中繼檔播放清單，建立
- 建立 Windows Media 中繼檔播放清單
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183857"
---
# <a name="creating-metafile-playlists"></a><span data-ttu-id="0d6fc-107">建立中繼檔播放清單</span><span class="sxs-lookup"><span data-stu-id="0d6fc-107">Creating Metafile Playlists</span></span>

<span data-ttu-id="0d6fc-108">您可以使用任何文字編輯器（例如 Microsoft 記事本）來建立播放清單。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-108">You can create a playlist using any text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="0d6fc-109">開啟您的文字編輯器。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-109">Open your text editor.</span></span> <span data-ttu-id="0d6fc-110">輸入您想要執行的腳本專案。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-110">Type the script entries you want to implement.</span></span> <span data-ttu-id="0d6fc-111">完成輸入記事本之後，請以適當的檔案名和副檔名儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-111">After you have finished typing into Notepad, save the file with an appropriate file name and file name extension.</span></span> <span data-ttu-id="0d6fc-112">如需擴充功能的詳細資訊，請參閱 [中繼檔延伸指導方針](metafile-extension-guidelines.md)。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-112">For more information about extensions, see [Metafile Extension Guidelines](metafile-extension-guidelines.md).</span></span> <span data-ttu-id="0d6fc-113">檔案名通常是 Windows Media 檔案或資料流程的名稱，後面接著地板蠟、. 300k.wvx 或 .asx 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-113">Typically the file name is the name of the Windows Media file or stream followed by an extension of .wax, .wvx, or .asx.</span></span> <span data-ttu-id="0d6fc-114">例如，如果您的媒體內容是副檔名為 .wma 的 Windows Media 音訊檔案，則在命名播放清單時，請使用地板蠟副檔名。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-114">For example, if your media content is a Windows Media audio file that has a .wma extension, use the .wax extension when naming the playlist.</span></span> <span data-ttu-id="0d6fc-115">播放清單不能包含文字處理器（例如 Microsoft Word）中的任何格式設定代碼。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-115">Playlists must not include any formatting codes from a word processor, such as Microsoft Word.</span></span> <span data-ttu-id="0d6fc-116">若要確定播放清單中未包含任何格式設定代碼，請將檔案儲存為純文字或 ASCII 檔。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-116">To be sure no formatting codes are included in the playlist, save the file as a plain text or ASCII file.</span></span>

> [!Note]  
> <span data-ttu-id="0d6fc-117">元素和屬性不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-117">Elements and attributes are not case sensitive.</span></span> <span data-ttu-id="0d6fc-118">播放清單中用來定義元素或屬性的文字可以是大寫或小寫，或是兩者的混合。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-118">The text used in the playlist to define an element or attribute can be either uppercase or lowercase, or a mixture of both.</span></span>

 

<span data-ttu-id="0d6fc-119">如果專案沒有任何子項目 (修改或包含在另一個專案) 中的專案，就可以在開頭標記的結尾處使用單一斜線字元 (/) ，而不是在 ' > ' 之前，用來取代結束記號。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-119">If an element does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag, just before the '>', in place of a closing tag.</span></span> <span data-ttu-id="0d6fc-120">專案的子項目必須出現在該元素的開頭和結束記號之間;否則這些專案不是該專案的子專案，而且會被忽略，或在播放清單的語法中造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-120">Child elements of an element must appear between the opening and closing tag for that element; otherwise they are not child elements for that element, and are ignored or cause an error in the syntax of the playlist.</span></span>

<span data-ttu-id="0d6fc-121">播放清單的前四個字元必須是 " &lt; ASX"。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-121">The first four characters of a playlist must be "&lt;ASX".</span></span> <span data-ttu-id="0d6fc-122">當所有播放清單中的地板蠟、. 300k.wvx 或 .asx 時，都使用了 **ASX** 元素。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-122">The **ASX** element is used in all playlists whether their extension is .wax, .wvx, or .asx.</span></span> <span data-ttu-id="0d6fc-123">每個播放清單必須只有一個 **ASX** 元素。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-123">There must be only one **ASX** element per playlist.</span></span> <span data-ttu-id="0d6fc-124">這個元素會將檔案識別為 Windows Media 中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-124">This element identifies the file as a Windows Media metafile playlist.</span></span> <span data-ttu-id="0d6fc-125">它不會指定播放清單的類型。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-125">It does not specify the type of playlist.</span></span>

<span data-ttu-id="0d6fc-126">**ASX** 元素有三個可能的屬性：</span><span class="sxs-lookup"><span data-stu-id="0d6fc-126">The **ASX** element has three possible attributes:</span></span>

<span data-ttu-id="0d6fc-127">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="0d6fc-127">**VERSION**</span></span>

<span data-ttu-id="0d6fc-128">**VERSION** 屬性是必要的，而且必須緊接在 **ASX** 元素之後，例如 "<asx VERSION =" 3.0 " &gt; "。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-128">The **VERSION** attribute is required and must follow immediately after the **ASX** element, for example "<ASX version = "3.0"&gt;".</span></span> <span data-ttu-id="0d6fc-129">目前的版本號碼為3.0。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-129">The current version number is 3.0.</span></span> <span data-ttu-id="0d6fc-130">Windows Media Player 支援所有先前的版本。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-130">Windows Media Player supports all previous versions.</span></span> <span data-ttu-id="0d6fc-131">**VERSION** 屬性可接受的值包括3.0 和 3 (，但) 不含小數點。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-131">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="0d6fc-132">**PREVIEWMODE**</span><span class="sxs-lookup"><span data-stu-id="0d6fc-132">**PREVIEWMODE**</span></span>

<span data-ttu-id="0d6fc-133">**PREVIEWMODE** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-133">The **PREVIEWMODE** attribute is optional.</span></span> <span data-ttu-id="0d6fc-134">它提供另一種機制來指定呈現剪輯的時間長度。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-134">It provides another mechanism for specifying how long to render a clip.</span></span> <span data-ttu-id="0d6fc-135">如果 [ **PREVIEWMODE** ] 屬性的值為 [是]，Windows Media Player 將會針對元素 **PREVIEWDURATION** 所指定的持續時間轉譯每個剪輯。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-135">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player will render each clip for the duration specified by the element **PREVIEWDURATION**.</span></span> <span data-ttu-id="0d6fc-136">每個剪輯都可以指定 **PREVIEWDURATION** 。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-136">Each clip can have a **PREVIEWDURATION** specified.</span></span>

<span data-ttu-id="0d6fc-137">**BANNERBAR**</span><span class="sxs-lookup"><span data-stu-id="0d6fc-137">**BANNERBAR**</span></span>

<span data-ttu-id="0d6fc-138">選擇性的 **BANNERBAR** 屬性會定義 Windows Media Player 控制項是否保留橫幅圖形的空間。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-138">The optional **BANNERBAR** attribute defines whether the Windows Media Player control reserves space for a banner graphic.</span></span> <span data-ttu-id="0d6fc-139"> (使用 **橫幅** 元素來指定要顯示的圖形。 ) 如果 **BANNERBAR** 的值是固定的，Windows Media Player 會保留顯示和每個剪輯的橫幅空間，無論中繼檔播放清單是否指定顯示或剪輯的橫幅。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-139">(Use the **BANNER** element to specify the graphic to display.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for the show and for every clip, whether the metafile playlist specifies a banner for the show or clip.</span></span> <span data-ttu-id="0d6fc-140">這會將 Windows Media Player 視窗的大小保持不變，但不論是在影片大小變更) ，不論是否有橫幅圖形都不存在也 (一樣。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-140">This will keep the size of the Windows Media Player window the same (except when the video size changes) regardless of the absence or presence of a banner graphic.</span></span> <span data-ttu-id="0d6fc-141">如果顯示或剪輯沒有相關聯的橫幅，保留給一個的空間會是黑色。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-141">If the show or clip does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="0d6fc-142">如果 [ **BANNERBAR** ] 屬性的值為 [自動]，Windows Media Player 只有在顯示或剪輯包含時，才會保留橫幅的空間。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-142">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the show or clip includes one.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



<span data-ttu-id="0d6fc-143">如需有關 **asx** 元素之三個屬性的詳細資訊，請參閱 [asx 元素](asx-element.md)的參考專案。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-143">For more information about the three attributes of the **ASX** element, see the reference entry for the [ASX Element](asx-element.md).</span></span>

<span data-ttu-id="0d6fc-144">**ASX** 元素包含 **專案** 子項目，可定義要存取之媒體檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-144">An **ASX** element contains **ENTRY** child elements that define information about the media files to be accessed.</span></span> <span data-ttu-id="0d6fc-145">每個 **ENTRY 專案** 都必須包含 **REF** 元素，以指定要進行資料流程處理之媒體檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-145">Each **ENTRY** element must contain a **REF** element that specifies the path to the media file to be streamed.</span></span> <span data-ttu-id="0d6fc-146">**ASX** 元素中必須至少有一個 **專案** 或 **ENTRYREF** 元素。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-146">There must be at least one **ENTRY** or **ENTRYREF** element within an **ASX** element.</span></span>

<span data-ttu-id="0d6fc-147">在 **ASX** 元素範圍內定義的其他元素（例如 **標題** 和 **作者**）會與 Windows Media Player 所顯示的中繼資料相關聯。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-147">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the metadata displayed by Windows Media Player.</span></span>

<span data-ttu-id="0d6fc-148">最簡單的播放清單是藉由將具有單一 **REF** 專案的多個 **專案專案** 新增至中繼檔來建立。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-148">The simplest playlists are created by adding multiple **ENTRY** elements with a single **REF** element to a metafile.</span></span> <span data-ttu-id="0d6fc-149">中繼檔播放清單中的每個 **ENTRY 專案** 都會依照其出現的順序轉譯，如同使用者手動開啟每個剪輯一樣。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-149">Each **ENTRY** element in a metafile playlist is rendered in the order it appears in the file as though the user had manually opened each clip.</span></span>

<span data-ttu-id="0d6fc-150">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="0d6fc-150">Example Code</span></span>


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



<span data-ttu-id="0d6fc-151">在 Windows 檔案總管中按兩下播放清單來確定播放清單是否正常運作。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-151">Be sure that the playlist is working by double-clicking it in Windows Explorer.</span></span> <span data-ttu-id="0d6fc-152">Windows Media Player 應開啟並開始串流處理媒體內容。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-152">Windows Media Player should open and start streaming the media content.</span></span> <span data-ttu-id="0d6fc-153">確認播放清單正常運作之後，請將它連同網頁一起儲存到您的 web 伺服器，並透過 **HREF** 元素連結，或使用 Windows Media Player **物件** 專案將它內嵌在網頁中。</span><span class="sxs-lookup"><span data-stu-id="0d6fc-153">After you have confirmed that the playlist works, save it to your web server along with your webpages, and link to it by means of an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** element.</span></span>

<span data-ttu-id="0d6fc-154">下列各節包含詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="0d6fc-154">The following sections contain more information:</span></span>

-   [<span data-ttu-id="0d6fc-155">嵌套中繼檔</span><span class="sxs-lookup"><span data-stu-id="0d6fc-155">Nesting Metafiles</span></span>](nesting-metafiles.md)
-   [<span data-ttu-id="0d6fc-156">使用 ASP 頁面動態建立 Windows Media 中繼檔播放清單</span><span class="sxs-lookup"><span data-stu-id="0d6fc-156">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="0d6fc-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d6fc-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d6fc-158">**橫幅元素**</span><span class="sxs-lookup"><span data-stu-id="0d6fc-158">**BANNER Element**</span></span>](banner-element.md)
</dt> <dt>

[<span data-ttu-id="0d6fc-159">**範例播放清單**</span><span class="sxs-lookup"><span data-stu-id="0d6fc-159">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="0d6fc-160">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="0d6fc-160">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0d6fc-161">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="0d6fc-161">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




