---
description: DirectShow 編輯服務簡介
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: DirectShow 編輯服務簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467665"
---
# <a name="introduction-to-directshow-editing-services"></a><span data-ttu-id="3e408-103">DirectShow 編輯服務簡介</span><span class="sxs-lookup"><span data-stu-id="3e408-103">Introduction to DirectShow Editing Services</span></span>

<span data-ttu-id="3e408-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3e408-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3e408-105">DirectShow 的核心是處理串流媒體的強大架構。</span><span class="sxs-lookup"><span data-stu-id="3e408-105">The core of DirectShow is a powerful architecture for handling streaming media.</span></span> <span data-ttu-id="3e408-106">應用程式可以使用它來播放以各式各樣格式撰寫的多媒體內容，而開發人員不需要擔心檔案壓縮和其他繁瑣的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3e408-106">An application can use it to play multimedia content authored in a wide variety of formats, without the developer needing to worry about file compression and other tedious details.</span></span> <span data-ttu-id="3e408-107">不過，在 [Directshow 編輯服務](directshow-editing-services.md) (DES) 之前，directshow 缺乏非線性編輯所需的彈性。</span><span class="sxs-lookup"><span data-stu-id="3e408-107">Prior to [DirectShow Editing Services](directshow-editing-services.md) (DES), however, DirectShow lacked the flexibility needed for nonlinear editing.</span></span>

<span data-ttu-id="3e408-108">例如，假設您想要建立由來源 A 4 秒組成的影片序列，後面接著來源 B 的10秒，並以來源 C 的5秒結尾。您可以很輕鬆地使用核心的 DirectShow API 來完成。</span><span class="sxs-lookup"><span data-stu-id="3e408-108">For example, suppose you wanted to create a video sequence consisting of 4 seconds from source A, followed by 10 seconds from source B, and ending with 5 seconds from source C. You could accomplish that much fairly easily using only the core DirectShow API.</span></span>

<span data-ttu-id="3e408-109">但是，如果您決定來源 C 應該在來源 B 之前，不是在之後，順序應該使用來自來源 A 的8秒，而不是4。而整個生產需要在背景中播放個別的音訊播放軌嗎？</span><span class="sxs-lookup"><span data-stu-id="3e408-109">But what if you decided that source C should come before source B, not after; that the sequence should use 8 seconds from source A, not 4; and that the entire production needed a separate audio track playing in the background?</span></span> <span data-ttu-id="3e408-110">即使是微小的變更（例如這些變更）也很難實行。</span><span class="sxs-lookup"><span data-stu-id="3e408-110">Even minor changes such as these could be difficult to implement.</span></span> <span data-ttu-id="3e408-111">但是剛剛所述的案例是 DES 的簡單編輯專案—您可以使用少數的方法呼叫來進行。</span><span class="sxs-lookup"><span data-stu-id="3e408-111">But the scenario just described is a trivial editing project in DES—you can do it with a handful of method calls.</span></span>

<span data-ttu-id="3e408-112">以下是一些 DES 為 DirectShow 帶來的功能：</span><span class="sxs-lookup"><span data-stu-id="3e408-112">Here are some of the features that DES brings to DirectShow:</span></span>

-   <span data-ttu-id="3e408-113">將影片和音訊曲目組織成嵌套圖層的時間軸模型，可讓您輕鬆地操作最終生產環境</span><span class="sxs-lookup"><span data-stu-id="3e408-113">A timeline model that organizes video and audio tracks into nested layers, making it easy to manipulate the final production</span></span>
-   <span data-ttu-id="3e408-114">即時預覽影片專案的能力</span><span class="sxs-lookup"><span data-stu-id="3e408-114">The ability to preview a video project on the fly</span></span>
-   <span data-ttu-id="3e408-115">透過以 XML 為基礎的格式的專案持續性</span><span class="sxs-lookup"><span data-stu-id="3e408-115">Project persistence through an XML-based format</span></span>
-   <span data-ttu-id="3e408-116">支援影片和音訊效果，以及影片曲目之間的轉換 (例如淡化和抹除) </span><span class="sxs-lookup"><span data-stu-id="3e408-116">Support for video and audio effects, as well as transitions between video tracks (such as fades and wipes)</span></span>
-   <span data-ttu-id="3e408-117">超過100標準抹除，如運動圖片和電視工程師的社會所定義 (SMPTE) </span><span class="sxs-lookup"><span data-stu-id="3e408-117">Over 100 standard wipes, as defined by the Society of Motion Picture and Television Engineers (SMPTE)</span></span>
-   <span data-ttu-id="3e408-118">以色調、亮度、RGB 值或 Alpha 值為基礎的金鑰</span><span class="sxs-lookup"><span data-stu-id="3e408-118">Keying based on hue, luminance, RGB value, or alpha value</span></span>
-   <span data-ttu-id="3e408-119">自動轉換畫面播放速率和音訊取樣率，讓生產環境使用異類來源</span><span class="sxs-lookup"><span data-stu-id="3e408-119">Automatic conversion of frame rates and audio sampling rates, enabling a production to use heterogeneous sources</span></span>
-   <span data-ttu-id="3e408-120">調整大小或裁剪影片</span><span class="sxs-lookup"><span data-stu-id="3e408-120">Resizing or cropping of video</span></span>

<span data-ttu-id="3e408-121">限制：</span><span class="sxs-lookup"><span data-stu-id="3e408-121">Limitations:</span></span>

-   <span data-ttu-id="3e408-122">DES 不支援 MPEG-2 或 h.264 影片來源。</span><span class="sxs-lookup"><span data-stu-id="3e408-122">DES does not support MPEG-2 or H.264 video sources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e408-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e408-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e408-124">DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="3e408-124">DirectShow Editing Services</span></span>](directshow-editing-services.md)
</dt> </dl>

 

 



