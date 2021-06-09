---
description: DirectShow 簡介
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: DirectShow 簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827222"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="4de50-103">DirectShow 簡介</span><span class="sxs-lookup"><span data-stu-id="4de50-103">Introduction to DirectShow</span></span>

<span data-ttu-id="4de50-104">Microsoft® DirectShow®是在 Microsoft Windows®平臺上串流處理媒體的架構。</span><span class="sxs-lookup"><span data-stu-id="4de50-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="4de50-105">DirectShow 為多媒體串流提供高品質的捕獲和播放功能。</span><span class="sxs-lookup"><span data-stu-id="4de50-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="4de50-106">它支援各種不同的格式，包括先進的系統格式 (ASF) 、運動圖片專家群組 (MPEG) 、Audio-Video 交錯 (AVI) 、MPEG 音訊第3層 (MP3) 和 WAV 音效檔。</span><span class="sxs-lookup"><span data-stu-id="4de50-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="4de50-107">它支援根據適用于 Windows 的 Windows Driver Model (WDM) 或影片，從數位和類比裝置進行捕捉。</span><span class="sxs-lookup"><span data-stu-id="4de50-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="4de50-108">它會自動偵測並使用影片和音訊加速硬體（如有提供），但也支援不含加速硬體的系統。</span><span class="sxs-lookup"><span data-stu-id="4de50-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="4de50-109">DirectShow 是以元件物件模型 (COM) 為基礎。</span><span class="sxs-lookup"><span data-stu-id="4de50-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="4de50-110">若要撰寫 DirectShow 應用程式或元件，您必須瞭解 COM 用戶端程式設計。</span><span class="sxs-lookup"><span data-stu-id="4de50-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="4de50-111">針對大部分的應用程式，您不需要執行自己的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="4de50-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="4de50-112">DirectShow 提供您所需的元件。</span><span class="sxs-lookup"><span data-stu-id="4de50-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="4de50-113">但是，如果您想要藉由撰寫自己的元件來擴充 DirectShow，則必須將它們實作為 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="4de50-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="4de50-114">DirectShow 是針對 c + + 所設計。</span><span class="sxs-lookup"><span data-stu-id="4de50-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="4de50-115">Microsoft 不提供適用于 DirectShow 的受控 API。</span><span class="sxs-lookup"><span data-stu-id="4de50-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="4de50-116">DirectShow 簡化了媒體播放、格式轉換和捕獲工作。</span><span class="sxs-lookup"><span data-stu-id="4de50-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="4de50-117">同時，針對需要自訂解決方案的應用程式，它會提供基礎資料流程控制架構的存取權。</span><span class="sxs-lookup"><span data-stu-id="4de50-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="4de50-118">您也可以建立自己的 DirectShow 元件，以支援新的格式或自訂效果。</span><span class="sxs-lookup"><span data-stu-id="4de50-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="4de50-119">您可以使用 DirectShow 撰寫之應用程式類型的範例包括檔案播放程式、電視和 DVD 播放機、影片編輯應用程式、檔案格式轉換器、音訊-影片捕獲應用程式、編碼器和解碼器、數位訊號處理器等等。</span><span class="sxs-lookup"><span data-stu-id="4de50-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="4de50-120">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="4de50-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="4de50-121">DirectShow 的新功能</span><span class="sxs-lookup"><span data-stu-id="4de50-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="4de50-122">DirectShow 中支援的格式</span><span class="sxs-lookup"><span data-stu-id="4de50-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="4de50-123">DirectShow 常見問題</span><span class="sxs-lookup"><span data-stu-id="4de50-123">DirectShow FAQ</span></span>](directshow-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="4de50-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="4de50-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4de50-125">快速入門</span><span class="sxs-lookup"><span data-stu-id="4de50-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="4de50-126">使用 DirectShow</span><span class="sxs-lookup"><span data-stu-id="4de50-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



