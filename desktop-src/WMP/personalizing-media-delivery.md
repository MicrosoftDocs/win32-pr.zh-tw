---
title: 個人化媒體傳遞
description: 個人化媒體傳遞
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows Media 中繼檔播放清單，個人化媒體傳遞
- 播放清單、個人化媒體傳遞
- 中繼檔播放清單，個人化媒體傳遞
- Windows Media 中繼檔播放清單，媒體傳遞個人化
- 播放清單、媒體傳遞個人化
- 中繼檔播放清單，媒體傳遞個人化
- 媒體傳遞個人化
- 個人化媒體傳遞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183093"
---
# <a name="personalizing-media-delivery"></a><span data-ttu-id="f0afc-111">個人化媒體傳遞</span><span class="sxs-lookup"><span data-stu-id="f0afc-111">Personalizing Media Delivery</span></span>

<span data-ttu-id="f0afc-112">不同于將相同內容廣播給大量物件的單向通訊，Windows Media 技術可提供您使用人口統計來賦予廣播的工具。</span><span class="sxs-lookup"><span data-stu-id="f0afc-112">Unlike one-way communication that broadcasts identical content to a mass audience, Windows Media Technologies provides you with the tools to use demographics to individualize broadcasts.</span></span> <span data-ttu-id="f0afc-113">在網際網路上，大規模的雙向通訊可供使用。</span><span class="sxs-lookup"><span data-stu-id="f0afc-113">With the Internet, two-way communication on a large scale is readily available.</span></span> <span data-ttu-id="f0afc-114">這項動態的資訊交換可讓內容提供者知道其物件，並以自訂的簡報回應。</span><span class="sxs-lookup"><span data-stu-id="f0afc-114">This dynamic interchange of information enables content providers to know their audience and respond with customized presentations.</span></span>

<span data-ttu-id="f0afc-115">下列範例（使用虛構公司）說明如何將串流內容的傳遞傳遞給個人化。</span><span class="sxs-lookup"><span data-stu-id="f0afc-115">The following example, using a fictional company, illustrates how delivery of streaming content can be personalized.</span></span> <span data-ttu-id="f0afc-116">本文假設您已熟悉 Active Server Pages (ASP 或 .asp 檔案) 和定義變數。</span><span class="sxs-lookup"><span data-stu-id="f0afc-116">This discussion assumes that you are familiar with Active Server Pages (ASP, or .asp files) and defining variables.</span></span>

<span data-ttu-id="f0afc-117">新聞網路是虛構的廣播新聞群組織，已擴充其作業以包含網站。</span><span class="sxs-lookup"><span data-stu-id="f0afc-117">News Network is a fictional broadcast news organization that has expanded its operations to include a website.</span></span> <span data-ttu-id="f0afc-118">網站的主要功能是一個區段，使用者可以在其中建立自己的個人化 newscasts。</span><span class="sxs-lookup"><span data-stu-id="f0afc-118">The main feature of the site is a section where users can create their own personalized newscasts.</span></span> <span data-ttu-id="f0afc-119">使用者不會看到以大量物件為目標的傳統 newscast，而是會查看只包含個人興趣主題的完整新聞方案。</span><span class="sxs-lookup"><span data-stu-id="f0afc-119">Instead of viewing a traditional newscast that is aimed at a mass audience, a user views a complete news program that contains only topics of personal interest.</span></span> <span data-ttu-id="f0afc-120">下列順序說明一般使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="f0afc-120">The following sequence describes a typical user experience.</span></span>

1.  <span data-ttu-id="f0afc-121">新的使用者前往網站，然後按一下 [ **建立您的個人 Newscast**]。</span><span class="sxs-lookup"><span data-stu-id="f0afc-121">A new user goes to the site, and clicks **Create Your Personal Newscast**.</span></span>
2.  <span data-ttu-id="f0afc-122">喜好設定表單隨即開啟。</span><span class="sxs-lookup"><span data-stu-id="f0afc-122">A preference form opens.</span></span> <span data-ttu-id="f0afc-123">在此表單上，使用者會回答有關個人喜好的問題，例如我的最愛新聞故事、最愛的新聞報導、業餘新聞，以及日常接收日常新聞的方法。</span><span class="sxs-lookup"><span data-stu-id="f0afc-123">On this form, the user answers questions regarding personal preferences, such as favorite news stories, least favorite news stories, hobbies, and usual method of receiving daily news.</span></span>
3.  <span data-ttu-id="f0afc-124">使用者傳送此資訊，而幾秒鐘之後，就會查看完整、15分鐘的個人 newscast，內含程式內容、轉換和電視廣告。</span><span class="sxs-lookup"><span data-stu-id="f0afc-124">The user sends this information, and a few seconds later views a complete, 15-minute, personal newscast containing program content, transitions, and commercials.</span></span> <span data-ttu-id="f0afc-125">每個媒體元件的選取專案（包括電視廣告）是以使用者設定檔為基礎，而且是透過 Windows Media 技術元件和現成的網際網路工具自動完成。</span><span class="sxs-lookup"><span data-stu-id="f0afc-125">Selection of each media element, including commercials, is based on the user profile, and is accomplished automatically with Windows Media Technologies components and off-the-shelf Internet tools.</span></span>

<span data-ttu-id="f0afc-126">下列清單說明各種工具如何互動以建立個人化 newscast。</span><span class="sxs-lookup"><span data-stu-id="f0afc-126">The following list describes how the various tools interact to create a personalized newscast.</span></span>

1.  <span data-ttu-id="f0afc-127">使用者填寫的喜好設定表單是使用中的伺服器頁 (ASP)  (選項。 asp) 。</span><span class="sxs-lookup"><span data-stu-id="f0afc-127">The preference form that the user fills out is an Active Server Page (ASP) (Choices.asp).</span></span> <span data-ttu-id="f0afc-128">從喜好設定形式取得的資料會由兩個伺服器元件進行分析。</span><span class="sxs-lookup"><span data-stu-id="f0afc-128">Data obtained from the preference form is analyzed by two server components.</span></span> <span data-ttu-id="f0afc-129">其中一個元件會使用此資訊來查詢 Microsoft SQL Server 的新聞故事資料庫。</span><span class="sxs-lookup"><span data-stu-id="f0afc-129">One component uses the information to query a Microsoft SQL Server database of news stories.</span></span> <span data-ttu-id="f0afc-130">另一個元件是一種 ad 伺服器，會根據合約需求和人口統計來使用一組複雜的規則，以便在該時間排程適合使用者的廣告。</span><span class="sxs-lookup"><span data-stu-id="f0afc-130">The other component is an ad server that uses a complex set of rules based on contractual requirements and demographics to schedule ads appropriate to the user at that time.</span></span>
2.  <span data-ttu-id="f0afc-131">這兩個資料庫會傳回不同的播放清單部分。</span><span class="sxs-lookup"><span data-stu-id="f0afc-131">The two databases return different portions of a playlist.</span></span> <span data-ttu-id="f0afc-132">新聞故事資料庫會傳回一組適當的故事專案，而且 ad 伺服器會傳回一組適當的商業專案。</span><span class="sxs-lookup"><span data-stu-id="f0afc-132">The news story database returns a set of appropriate story Entries, and the ad server returns a set of appropriate commercial Entries.</span></span>
3.  <span data-ttu-id="f0afc-133">第二個 ASP 網頁 (PlayShow asp) 從新聞故事資料庫和 ad 伺服器接收專案，並將這些專案與標準顯示開啟、關閉和轉換專案結合。</span><span class="sxs-lookup"><span data-stu-id="f0afc-133">A second ASP page (PlayShow.asp) receives the Entries from the news story database and ad server, and combines those with standard show open, close, and transition Entries.</span></span> <span data-ttu-id="f0afc-134">然後，所有專案都會根據 PlayShow 所提供的範本來配置，而 ASP 頁面會將播放清單傳回給使用者。</span><span class="sxs-lookup"><span data-stu-id="f0afc-134">All Entries are then laid out according to the template provided by PlayShow.asp, and the ASP page returns a playlist to the user.</span></span>
4.  <span data-ttu-id="f0afc-135">使用者電腦上的內嵌 Windows Media Player 控制項播放播放清單的播放清單，而使用者則會查看個人化 newscast。</span><span class="sxs-lookup"><span data-stu-id="f0afc-135">The embedded Windows Media Player control on the user's computer plays the playlist from beginning to end, and the user views a personalized newscast.</span></span>

<span data-ttu-id="f0afc-136">下列範例是使用者可能會收到的播放清單檔案部分。</span><span class="sxs-lookup"><span data-stu-id="f0afc-136">The following example is a portion of a playlist file that a user might receive.</span></span> <span data-ttu-id="f0afc-137">Ad 橫幅、MOREINFO 連結和摘要已新增至其中。</span><span class="sxs-lookup"><span data-stu-id="f0afc-137">Ad banners, MOREINFO links, and ABSTRACTS have been added to it.</span></span>


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   <span data-ttu-id="f0afc-138">本文所述之公司、組織、產品、人物及事件均屬虛構，</span><span class="sxs-lookup"><span data-stu-id="f0afc-138">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="f0afc-139">並非影射任何真實的公司、組織、產品、人物或事件。</span><span class="sxs-lookup"><span data-stu-id="f0afc-139">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0afc-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0afc-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0afc-141">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="f0afc-141">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f0afc-142">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="f0afc-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f0afc-143">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="f0afc-143">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f0afc-144">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="f0afc-144">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f0afc-145">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="f0afc-145">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




