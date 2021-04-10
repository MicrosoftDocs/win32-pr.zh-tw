---
title: 豐富的媒體串流
description: 豐富的媒體串流
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player，以網路為基礎的簡報
- Windows Media Player 物件模型，以網路為基礎的簡報
- 物件模型，以 Web 為基礎的簡報
- Windows Media Player 行動裝置、以網路為基礎的簡報
- Windows Media Player ActiveX 控制項，以 Web 為基礎的簡報
- Windows Media Player 的行動 ActiveX 控制項，以網路為基礎的簡報
- ActiveX 控制項，以網頁為基礎的簡報
- Windows Media Player，豐富的媒體串流
- Windows Media Player 物件模型，多媒體串流
- 物件模型，多媒體串流
- Windows Media Player Mobile、豐富的媒體串流
- Windows Media Player ActiveX 控制項，豐富的媒體串流
- Windows Media Player 的行動 ActiveX 控制項、豐富的媒體串流
- ActiveX 控制項，豐富的媒體串流
- 以網路為基礎的簡報，豐富的媒體串流
- 建立以網路為基礎的簡報、豐富的媒體串流
- 豐富的媒體串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674676"
---
# <a name="rich-media-streaming"></a><span data-ttu-id="86ec3-120">豐富的媒體串流</span><span class="sxs-lookup"><span data-stu-id="86ec3-120">Rich Media Streaming</span></span>

<span data-ttu-id="86ec3-121">複雜的網頁包含許多通常會分開傳輸的不同元件。</span><span class="sxs-lookup"><span data-stu-id="86ec3-121">Complex webpages contain many different components that are normally transferred separately.</span></span> <span data-ttu-id="86ec3-122">在慢速連線上，這類頁面會一次顯示一段時間，而且可能需要幾分鐘的時間才能完全顯示。</span><span class="sxs-lookup"><span data-stu-id="86ec3-122">On a slow connection, such pages display one piece at a time and may take several minutes to display completely.</span></span> <span data-ttu-id="86ec3-123">這可能會讓您無法有效地將網頁與數位媒體進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="86ec3-123">This may prevent you from effectively synchronizing webpages with your digital media.</span></span> <span data-ttu-id="86ec3-124">此問題的解決方式是豐富的媒體串流，這表示將您的網頁加入數位媒體串流，以與音訊或影片資料同時提供。</span><span class="sxs-lookup"><span data-stu-id="86ec3-124">The solution to this problem is rich media streaming, which means adding your webpages to your digital media stream so that they are delivered at the same time as the audio or video data.</span></span>

<span data-ttu-id="86ec3-125">豐富的媒體串流使用簡單的框架配置，其行為與一般的 URL 翻轉一樣。</span><span class="sxs-lookup"><span data-stu-id="86ec3-125">Rich media streaming uses a simple frameset layout and behaves exactly like normal URL flipping.</span></span> <span data-ttu-id="86ec3-126">如同在 URL 翻轉中，內嵌在數位媒體資料流程中的 URL 指令碼命令會用來顯示目標框架中的內容。</span><span class="sxs-lookup"><span data-stu-id="86ec3-126">Just as in URL flipping, URL script commands embedded in digital media streams are used to display the content in the target frame.</span></span> <span data-ttu-id="86ec3-127">但是，Windows Media Player 9 系列或更新版本會使用 URL 指令碼命令來存取 Internet Explorer 快取中的檔案，而不是指向 Web 上的頁面，而是在接收到資料流程處理的 HTML 內容時，會使用 URL 指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="86ec3-127">Instead of pointing to pages on the Web, however, the URL script commands are used by Windows Media Player 9 Series or later to access files in the Internet Explorer cache where the streamed HTML content is placed as it is received.</span></span> <span data-ttu-id="86ec3-128">如同一般的 URL 翻轉，您可以撰寫事件處理常式來回應這些 URL 指令碼命令，也可以讓 Windows Media Player 控制項自動處理所有內容。</span><span class="sxs-lookup"><span data-stu-id="86ec3-128">Just as with normal URL flipping, you can write event handlers that respond to these URL script commands, or you can let the Windows Media Player control handle everything automatically.</span></span>

> [!Note]  
> <span data-ttu-id="86ec3-129">透過豐富媒體串流傳遞的任何 HTML 內容都會在網際網路安全性區域中播放，並且受限於使用者的瀏覽器安全性設定。</span><span class="sxs-lookup"><span data-stu-id="86ec3-129">Any HTML content delivered through rich media streaming is played back in the Internet security zone, and is subject to the user's browser security settings.</span></span>

 

<span data-ttu-id="86ec3-130">如需有關建立豐富媒體簡報的詳細資訊，請參閱 Windows Media Format 9 系列或更新版本的 SDK 和 Windows Media 編碼器9系列 SDK。</span><span class="sxs-lookup"><span data-stu-id="86ec3-130">For more information on creating rich media presentations, see the Windows Media Format 9 Series or later SDK and the Windows Media Encoder 9 Series SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86ec3-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="86ec3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86ec3-132">**建立 Web-Based 簡報**</span><span class="sxs-lookup"><span data-stu-id="86ec3-132">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="86ec3-133">**使用腳本來控制 URL 翻轉**</span><span class="sxs-lookup"><span data-stu-id="86ec3-133">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




