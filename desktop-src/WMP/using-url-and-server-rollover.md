---
title: 使用 URL 和伺服器變換
description: 使用 URL 和伺服器變換
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows Media 中繼檔播放清單，URL 變換
- 播放清單，URL 變換
- 中繼檔播放清單，URL 變換
- Windows Media 中繼檔播放清單，伺服器變換
- 播放清單，伺服器變換
- 中繼檔播放清單，伺服器變換
- Windows Media 中繼檔播放清單，通訊協定變換
- 播放清單，通訊協定變換
- 中繼檔播放清單，通訊協定變換
- Windows Media Player，URL 變換
- Windows Media Player，伺服器變換
- Windows Media Player，通訊協定變換
- URL 變換
- 伺服器變換
- 通訊協定變換
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301007"
---
# <a name="using-url-and-server-rollover"></a><span data-ttu-id="aa669-118">使用 URL 和伺服器變換</span><span class="sxs-lookup"><span data-stu-id="aa669-118">Using URL and Server Rollover</span></span>

<span data-ttu-id="aa669-119">您可以使用中繼檔播放清單，在無法存取或播放資料流程時，提供自動變換替代內容來源的方法。</span><span class="sxs-lookup"><span data-stu-id="aa669-119">You can use metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span> <span data-ttu-id="aa669-120">您可以使用這個變換方法，在不同的伺服器或不同類型的伺服器上指定相同內容的來源。</span><span class="sxs-lookup"><span data-stu-id="aa669-120">You can use this rollover method to specify sources of the same content on different servers or different types of servers.</span></span> <span data-ttu-id="aa669-121">例如，您可以在不同的 Windows Media 伺服器上指定第一個替代。</span><span class="sxs-lookup"><span data-stu-id="aa669-121">You can, for example, specify a first alternate on a different Windows Media server.</span></span> <span data-ttu-id="aa669-122">如果該內容無法播放，用戶端可以變換為 web 伺服器上的第二個替代。</span><span class="sxs-lookup"><span data-stu-id="aa669-122">If that content fails to play, the client can roll over to a second alternate on a web server.</span></span> <span data-ttu-id="aa669-123">Windows Media Player 會在嘗試播放清單中的換用 Url 之前，根據其 Windows Media 內容設定，自動嘗試變換至不同的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="aa669-123">Windows Media Player automatically tries to roll over to different protocols according to its Windows Media property settings before trying the rollover URLs in the playlist.</span></span>

<span data-ttu-id="aa669-124">藉由在一個 **專案專案** 中連續放置多個 **REF** 元素，來設定伺服器和通訊協定變換。</span><span class="sxs-lookup"><span data-stu-id="aa669-124">Set server and protocol rollover by placing multiple **REF** elements in succession within one **ENTRY** element.</span></span> <span data-ttu-id="aa669-125">每個 **REF** 元素都會指定媒體檔案或資料流程的替代位置或通訊協定。</span><span class="sxs-lookup"><span data-stu-id="aa669-125">Each **REF** element specifies an alternate location or protocol for a media file or stream.</span></span>

<span data-ttu-id="aa669-126">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="aa669-126">Example Code</span></span>


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="aa669-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa669-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa669-128">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="aa669-128">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="aa669-129">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="aa669-129">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




