---
description: 音訊捕獲
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: 音訊捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317783"
---
# <a name="audio-capture"></a><span data-ttu-id="f68ac-103">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="f68ac-103">Audio Capture</span></span>

<span data-ttu-id="f68ac-104">應用程式可以透過音效卡上的輸入，使用 DirectShow 從麥克風、磁帶播放機和其他裝置捕獲音訊資料。</span><span class="sxs-lookup"><span data-stu-id="f68ac-104">An application can use DirectShow to capture audio data from microphones, tape players, and other devices, through the inputs on the sound card.</span></span> <span data-ttu-id="f68ac-105">一般案例包括：</span><span class="sxs-lookup"><span data-stu-id="f68ac-105">Typical scenarios include:</span></span>

-   <span data-ttu-id="f68ac-106">錄製 voiceover 旁白，以稍後透過影片串流進行配音。</span><span class="sxs-lookup"><span data-stu-id="f68ac-106">Recording a voiceover narration for later dubbing over a video stream.</span></span>
-   <span data-ttu-id="f68ac-107">將舊版類比音訊內容轉換為數字格式。</span><span class="sxs-lookup"><span data-stu-id="f68ac-107">Converting legacy analog audio content to digital format.</span></span>
-   <span data-ttu-id="f68ac-108">透過網路捕捉語音或音樂以進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="f68ac-108">Capturing voice or music for transmission over a network.</span></span>

<span data-ttu-id="f68ac-109">終端使用者有數個選項可從音效卡將音訊捕獲到硬碟。</span><span class="sxs-lookup"><span data-stu-id="f68ac-109">End users have several options for capturing audio from the sound card to the hard disk.</span></span> <span data-ttu-id="f68ac-110">大部分的卡片都提供應用程式從其音訊輸入混合及錄製。</span><span class="sxs-lookup"><span data-stu-id="f68ac-110">Most cards provide applications for mixing and recording from their audio inputs.</span></span> <span data-ttu-id="f68ac-111">Windows 提供了答錄機，這是一個簡單的公用程式，可從麥克風錄製。</span><span class="sxs-lookup"><span data-stu-id="f68ac-111">Windows provides Sound Recorder, a simple utility application for recording from a microphone.</span></span> <span data-ttu-id="f68ac-112">Windows Media 編碼器可以納入至 DirectShow 應用程式中，做為 [DirectX 媒體物件](directx-media-objects.md) (的) 。</span><span class="sxs-lookup"><span data-stu-id="f68ac-112">The Windows Media Encoder can be incorporated into a DirectShow application as a [DirectX Media Object](directx-media-objects.md) (DMO).</span></span> <span data-ttu-id="f68ac-113">本節說明如何使用 DirectShow 將音訊捕獲功能整合到您自己的應用程式中。</span><span class="sxs-lookup"><span data-stu-id="f68ac-113">This section describes how to integrate audio capture functionality within your own application using DirectShow.</span></span>

<span data-ttu-id="f68ac-114">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="f68ac-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="f68ac-115">關於音訊捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="f68ac-115">About the Audio Capture Filter</span></span>](about-the-audio-capture-filter.md)
-   [<span data-ttu-id="f68ac-116">選取捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="f68ac-116">Selecting a Capture Device</span></span>](selecting-a-capture-device.md)
-   [<span data-ttu-id="f68ac-117">建立音訊捕獲圖形</span><span class="sxs-lookup"><span data-stu-id="f68ac-117">Creating an Audio Capture Graph</span></span>](creating-an-audio-capture-graph.md)
-   [<span data-ttu-id="f68ac-118">使用預覽建立音訊捕獲圖形</span><span class="sxs-lookup"><span data-stu-id="f68ac-118">Creating an Audio Capture Graph with Preview</span></span>](creating-an-audio-capture-graph-with-preview.md)
-   [<span data-ttu-id="f68ac-119">設定音訊捕獲屬性</span><span class="sxs-lookup"><span data-stu-id="f68ac-119">Setting Audio Capture Properties</span></span>](setting-audio-capture-properties.md)

## <a name="related-topics"></a><span data-ttu-id="f68ac-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="f68ac-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f68ac-121">使用 DirectShow</span><span class="sxs-lookup"><span data-stu-id="f68ac-121">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



