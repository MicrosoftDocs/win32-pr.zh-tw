---
description: VMR 的功能
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: VMR 的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973558"
---
# <a name="features-of-the-vmr"></a><span data-ttu-id="4429d-103">VMR 的功能</span><span class="sxs-lookup"><span data-stu-id="4429d-103">Features of the VMR</span></span>

<span data-ttu-id="4429d-104">影片混合轉譯器 7 (VMR-7) 支援下列新功能：</span><span class="sxs-lookup"><span data-stu-id="4429d-104">The Video Mixing Renderer 7 (VMR-7) supports the following new features:</span></span>

-   <span data-ttu-id="4429d-105">使用 Direct3D 硬體裝置的 Alpha 混合功能，來真正混合多個視頻串流。</span><span class="sxs-lookup"><span data-stu-id="4429d-105">Real mixing of multiple video streams, using the alpha-blending capabilities of Direct3D hardware devices.</span></span>
-   <span data-ttu-id="4429d-106">能夠插入您自己的複合元件，以在多個進入 VMR 的影片資料流程之間執行效果和轉換。</span><span class="sxs-lookup"><span data-stu-id="4429d-106">The ability to plug in your own compositing component to implement effects and transitions between multiple video streams entering the VMR.</span></span>
-   <span data-ttu-id="4429d-107">真正無視窗呈現。</span><span class="sxs-lookup"><span data-stu-id="4429d-107">True windowless rendering.</span></span> <span data-ttu-id="4429d-108">您不再需要讓影片播放視窗成為應用程式視窗的子系，以便包含影片播放。</span><span class="sxs-lookup"><span data-stu-id="4429d-108">It is no longer necessary to make the video playback window a child of the application's window in order to contain video playback.</span></span> <span data-ttu-id="4429d-109">VMR 的新無視窗轉譯模式，可讓應用程式輕鬆地在任何視窗內裝載影片播放，而不需要將視窗訊息轉寄到轉譯器特定的處理常式。</span><span class="sxs-lookup"><span data-stu-id="4429d-109">The VMR's new windowless rendering mode allows applications to easily host video playback within any window without having to forward window messages to the renderer for renderer-specific processing.</span></span>
-   <span data-ttu-id="4429d-110">新的 renderless 播放模式，在此模式中，應用程式可以提供自己的配置器元件，以便在螢幕上顯示已解碼的影片影像之前取得其存取權。</span><span class="sxs-lookup"><span data-stu-id="4429d-110">A new renderless playback mode where applications can supply their own allocator component to get access to the decoded video image prior to it being displayed on the screen.</span></span>
-   <span data-ttu-id="4429d-111">改進支援配備多個監視器的電腦。</span><span class="sxs-lookup"><span data-stu-id="4429d-111">Improved support for PCs equipped with multiple monitors.</span></span>
-   <span data-ttu-id="4429d-112">支援 Microsoft 的新 DirectX Video 加速架構。</span><span class="sxs-lookup"><span data-stu-id="4429d-112">Support for Microsoft's new DirectX Video Acceleration architecture.</span></span>
-   <span data-ttu-id="4429d-113">支援在多個 windows 上同時播放高品質的影片。</span><span class="sxs-lookup"><span data-stu-id="4429d-113">Support for high-quality video playback concurrently on multiple windows.</span></span>
-   <span data-ttu-id="4429d-114">支援 DirectDraw 獨佔模式</span><span class="sxs-lookup"><span data-stu-id="4429d-114">Support for DirectDraw Exclusive Mode</span></span>
-   <span data-ttu-id="4429d-115">100% 與現有應用程式的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="4429d-115">100% backward-compatibility with existing applications.</span></span>
-   <span data-ttu-id="4429d-116">支援框架逐步執行，以及可靠的方式來捕捉目前顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="4429d-116">Support for frame stepping and a reliable way to capture the current image being displayed.</span></span>
-   <span data-ttu-id="4429d-117">應用程式能輕鬆地將自己的靜態影像資料（例如頻道標誌或 UI 元件）與影片一起以無閃爍的方式)  (。</span><span class="sxs-lookup"><span data-stu-id="4429d-117">The ability for applications to easily alpha-blend their own static image data (such as channel logos or UI components) with the video in a smooth flicker-free way.</span></span>

<span data-ttu-id="4429d-118">VMR-9 支援以上所列的所有功能，以及：</span><span class="sxs-lookup"><span data-stu-id="4429d-118">The VMR-9 supports all the features listed above, plus:</span></span>

-   <span data-ttu-id="4429d-119">使用 Direct3D Api （例如圖元著色器）直接處理影片資料的能力。</span><span class="sxs-lookup"><span data-stu-id="4429d-119">The ability to process video data directly with Direct3D APIs such as pixel shaders.</span></span>
-   <span data-ttu-id="4429d-120">改進支援交錯式影片內容。</span><span class="sxs-lookup"><span data-stu-id="4429d-120">Improved support for interlaced video content.</span></span>
-   <span data-ttu-id="4429d-121">支援 DirectX 支援的任何平臺。</span><span class="sxs-lookup"><span data-stu-id="4429d-121">Support on any platform supported by DirectX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4429d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="4429d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4429d-123">關於影片混合轉譯</span><span class="sxs-lookup"><span data-stu-id="4429d-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



