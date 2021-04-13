---
title: 建立 Web-Based 簡報
description: 建立 Web-Based 簡報
ms.assetid: 60d8be10-ebed-4a4f-b17f-700475b51b34
keywords:
- Windows Media Player，以網路為基礎的簡報
- Windows Media Player 物件模型，以網路為基礎的簡報
- 物件模型，以 Web 為基礎的簡報
- Windows Media Player 行動裝置、以網路為基礎的簡報
- Windows Media Player ActiveX 控制項，以 Web 為基礎的簡報
- Windows Media Player 的行動 ActiveX 控制項，以網路為基礎的簡報
- ActiveX 控制項，以網頁為基礎的簡報
- 以網路為基礎的簡報，建立
- 建立以網路為基礎的簡報，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 117ee00164b50d319699f6e1d1806c4d8bf374af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311414"
---
# <a name="creating-web-based-presentations"></a><span data-ttu-id="1d0d4-112">建立 Web-Based 簡報</span><span class="sxs-lookup"><span data-stu-id="1d0d4-112">Creating Web-Based Presentations</span></span>

<span data-ttu-id="1d0d4-113">Windows Media Player 控制項可讓您輕鬆地建立以網路為基礎的投影片放映簡報，將音訊和影片與 HTML 結合在一起。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-113">The Windows Media Player control lets you easily create Web-based slide-show presentations that combine audio and video with HTML.</span></span> <span data-ttu-id="1d0d4-114">藉由將 URL 類型的指令碼命令新增至您的媒體檔案，您就可以在數位媒體播放期間的特定時間，讓指定的網頁顯示在指定的網頁瀏覽器框架中。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-114">By adding URL-type script commands to your media files, you can cause specified webpages to display in a specified Web browser frame at specific times during digital media playback.</span></span>

<span data-ttu-id="1d0d4-115">Windows Media Player 也提供豐富的媒體串流處理功能，可讓您有效率地透過單一 Windows Media 資料流程或檔案內的網路傳遞 HTML 資料。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-115">Windows Media Player also features rich media streaming to enable efficient delivery of HTML data over a network inside a single Windows Media stream or file.</span></span> <span data-ttu-id="1d0d4-116">播放程式和伺服器會處理流暢、及時的音訊、影片和 HTML 傳遞到瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-116">The Player and server handle the smooth, timely delivery of audio, video, and HTML to the browser.</span></span> <span data-ttu-id="1d0d4-117">就像是不使用豐富媒體串流處理的 Web 簡報一樣，內嵌指令碼命令會在指定的時間內，于指定的瀏覽器框架中轉譯展示。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-117">Just as in Web presentations that do not use rich media streaming, embedded script commands render the presentation in a specified browser frame at specified times.</span></span>

<span data-ttu-id="1d0d4-118">以 Web 為基礎的簡報一般配置會使用兩個畫面格。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-118">A typical layout for Web-based presentations uses two frames.</span></span> <span data-ttu-id="1d0d4-119">其中一個畫面格包含內嵌 Windows Media Player 控制項的網頁，並顯示簡報的影片部分。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-119">One frame contains a webpage that embeds the Windows Media Player control and displays the video part of a presentation.</span></span> <span data-ttu-id="1d0d4-120">另一個框架會顯示當影片播放時，在不同時間變更的網頁。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-120">The other frame displays webpages that change at various times as the video plays.</span></span>

<span data-ttu-id="1d0d4-121">如果您的網頁隨附的數位媒體僅包含音訊，您可以藉由將其寬度設定為零，隱藏包含 Windows Media Player 控制項的畫面格。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-121">If the digital media accompanying your webpages contains audio only, you can hide the frame that contains the Windows Media Player control by setting its width to zero.</span></span> <span data-ttu-id="1d0d4-122">如此一來，當您的網頁在完整瀏覽器視窗中顯示時，音訊就可以在背景中不中斷的播放。</span><span class="sxs-lookup"><span data-stu-id="1d0d4-122">This way, the audio can play uninterrupted in the background while your webpages display in the full browser window.</span></span>

<span data-ttu-id="1d0d4-123">下列各節說明啟用網頁型簡報的常見技術：</span><span class="sxs-lookup"><span data-stu-id="1d0d4-123">The following sections describe common techniques for enabling Web-based presentations:</span></span>

-   [<span data-ttu-id="1d0d4-124">URL 翻轉</span><span class="sxs-lookup"><span data-stu-id="1d0d4-124">URL Flipping</span></span>](url-flipping.md)
-   [<span data-ttu-id="1d0d4-125">豐富的媒體串流</span><span class="sxs-lookup"><span data-stu-id="1d0d4-125">Rich Media Streaming</span></span>](rich-media-streaming.md)

## <a name="related-topics"></a><span data-ttu-id="1d0d4-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d0d4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d0d4-127">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="1d0d4-127">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




