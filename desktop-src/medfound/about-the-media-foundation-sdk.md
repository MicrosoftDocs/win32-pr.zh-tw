---
description: Microsoft 媒體基礎是 Windows 的新一代多媒體平臺，可讓開發人員、取用者及內容提供者利用增強的強大功能、無與倫比的品質，以及無縫的互通性，來採用新的新 wave 內容 wave。
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: 關於媒體基礎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986008"
---
# <a name="about-media-foundation"></a><span data-ttu-id="7189a-103">關於媒體基礎</span><span class="sxs-lookup"><span data-stu-id="7189a-103">About Media Foundation</span></span>

<span data-ttu-id="7189a-104">Microsoft 媒體基礎是 Windows 的新一代多媒體平臺，可讓開發人員、取用者及內容提供者利用增強的強大功能、無與倫比的品質，以及無縫的互通性，來採用新的新 wave 內容 wave。</span><span class="sxs-lookup"><span data-stu-id="7189a-104">Microsoft Media Foundation is the next generation multimedia platform for Windows that enables developers, consumers, and content providers to embrace the new wave of premium content with enhanced robustness, unparalleled quality, and seamless interoperability.</span></span>

<span data-ttu-id="7189a-105">媒體基礎需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7189a-105">Media Foundation requires Windows Vista or later.</span></span> <span data-ttu-id="7189a-106">它使用元件物件模型 (COM) ，而且需要 C/c + +。</span><span class="sxs-lookup"><span data-stu-id="7189a-106">It uses the component object model (COM) and requires C/C++.</span></span> <span data-ttu-id="7189a-107">Microsoft 不會提供媒體基礎的受控 API。</span><span class="sxs-lookup"><span data-stu-id="7189a-107">Microsoft does not provide a managed API for Media Foundation.</span></span>

<span data-ttu-id="7189a-108">媒體基礎 Api 是 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)的一部分。</span><span class="sxs-lookup"><span data-stu-id="7189a-108">The Media Foundation APIs are part of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7189a-109">若要開發媒體基礎的應用程式，請安裝最新版本的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="7189a-109">To develop a Media Foundation application, install the latest version of the Windows SDK.</span></span>

## <a name="audio-and-video-quality"></a><span data-ttu-id="7189a-110">音訊和影片品質</span><span class="sxs-lookup"><span data-stu-id="7189a-110">Audio and Video Quality</span></span>

<span data-ttu-id="7189a-111">媒體基礎的設計目的是要滿足高定義內容所造成的挑戰。</span><span class="sxs-lookup"><span data-stu-id="7189a-111">Media Foundation has been designed to meet the challenges posed by high-definition content.</span></span> <span data-ttu-id="7189a-112">整個平臺中的音訊和影片品質增強功能現在可讓您為下一代的高定義內容提供絕佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="7189a-112">Audio and video quality enhancements made throughout the platform now make it possible to deliver a great experience for next generation high-definition content.</span></span>

-   <span data-ttu-id="7189a-113">DirectX Video 加速 (DXVA) 2.0 提供更有效率的影片加速，相較于 DXVA 1.0，其具有更強大且更有效率的影片解碼，並可在影片處理中擴充硬體的使用。</span><span class="sxs-lookup"><span data-stu-id="7189a-113">DirectX Video Acceleration (DXVA) 2.0 offers more efficient video acceleration, compared with DXVA 1.0, with more robust and streamlined video decoding and extended use of hardware in video processing.</span></span> <span data-ttu-id="7189a-114">使用 DXVA 2.0，Windows 可以處理一些需求最高的高定義內容，而且具有高品質且改良的故障恢復功能。</span><span class="sxs-lookup"><span data-stu-id="7189a-114">With DXVA 2.0, Windows can handle some of the most demanding high-definition content with high quality and improved glitch-resilience.</span></span>

-   <span data-ttu-id="7189a-115">整個影片管線都會保留色彩空間資訊。</span><span class="sxs-lookup"><span data-stu-id="7189a-115">Color-space information is preserved throughout the video pipeline.</span></span> <span data-ttu-id="7189a-116">使用者可以完整的精確度享受影片內容。</span><span class="sxs-lookup"><span data-stu-id="7189a-116">Users can enjoy video content with full fidelity.</span></span> <span data-ttu-id="7189a-117">色彩資訊和交錯影像現在會傳遞給單一傳遞組合的硬體。</span><span class="sxs-lookup"><span data-stu-id="7189a-117">Color information and interlaced images are now passed to hardware for single-pass compositions.</span></span> <span data-ttu-id="7189a-118">保留色彩空間資訊也可減少不必要的色彩空間轉換，以釋出更多的週期來處理要求的 HD 內容。</span><span class="sxs-lookup"><span data-stu-id="7189a-118">Preserving color-space information also reduces unnecessary color space conversions, which frees more cycles to process demanding HD content.</span></span>
-   <span data-ttu-id="7189a-119">增強的影片轉譯器 (EVR) 提供更佳的時間支援、增強的影片處理，以及改善的故障恢復功能。</span><span class="sxs-lookup"><span data-stu-id="7189a-119">The enhanced video renderer (EVR) offers better timing support, enhanced video processing, and improved glitch-resilience.</span></span> <span data-ttu-id="7189a-120">全螢幕播放支援已增強，而視窗模式中的影片撕裂已降至最低。</span><span class="sxs-lookup"><span data-stu-id="7189a-120">Full-screen playback support has been enhanced, and video tearing in windowed mode has been minimized.</span></span>
-   <span data-ttu-id="7189a-121">媒體基礎使用多媒體類別排程器服務 (MMCSS) 是 Windows Vista 中的新系統服務。</span><span class="sxs-lookup"><span data-stu-id="7189a-121">Media Foundation uses the Multimedia Class Scheduler Service (MMCSS), a new system service in Windows Vista.</span></span> <span data-ttu-id="7189a-122">MMCSS 可讓多媒體應用程式確保其時間緊迫的處理會獲得 CPU 資源的優先存取權。</span><span class="sxs-lookup"><span data-stu-id="7189a-122">MMCSS enables multimedia applications to ensure that their time-sensitive processing receives prioritized access to CPU resources.</span></span>

## <a name="content-access"></a><span data-ttu-id="7189a-123">內容存取</span><span class="sxs-lookup"><span data-stu-id="7189a-123">Content Access</span></span>

<span data-ttu-id="7189a-124">當數位娛樂移入高定義時代，而內容變得更容易攜帶和普及時，內容保護將成為數位媒體產品不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="7189a-124">As digital entertainment moves into the high-definition era and content becomes more portable and ubiquitous, content protection will become an integral part of digital media products.</span></span> <span data-ttu-id="7189a-125">媒體基礎的擴充性可確保它可以支援這些趨勢。</span><span class="sxs-lookup"><span data-stu-id="7189a-125">The extensibility of Media Foundation ensures that it can support these trends.</span></span>

<span data-ttu-id="7189a-126">此外，媒體基礎擴充性可讓不同的內容保護系統一起運作。</span><span class="sxs-lookup"><span data-stu-id="7189a-126">In addition, Media Foundation extensibility enables different content protection systems to operate together.</span></span>

## <a name="about-media-foundation"></a><span data-ttu-id="7189a-127">關於媒體基礎</span><span class="sxs-lookup"><span data-stu-id="7189a-127">About Media Foundation</span></span>

<span data-ttu-id="7189a-128">本章節包含媒體基礎 Api 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="7189a-128">This section contains general information about the Media Foundation APIs.</span></span> <span data-ttu-id="7189a-129">您可以在 [媒體基礎程式設計指南](media-foundation-programming-guide.md)中找到詳細的程式設計資訊。</span><span class="sxs-lookup"><span data-stu-id="7189a-129">Detailed programming information can be found in the [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>



| <span data-ttu-id="7189a-130">區段</span><span class="sxs-lookup"><span data-stu-id="7189a-130">Section</span></span>                                                                              | <span data-ttu-id="7189a-131">描述</span><span class="sxs-lookup"><span data-stu-id="7189a-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="7189a-132">媒體基礎的新功能</span><span class="sxs-lookup"><span data-stu-id="7189a-132">What's New for Media Foundation</span></span>](whats-new-for-media-foundation.md)                | <span data-ttu-id="7189a-133">描述媒體基礎中的新功能。</span><span class="sxs-lookup"><span data-stu-id="7189a-133">Describes new features in Media Foundation.</span></span>                               |
| [<span data-ttu-id="7189a-134">媒體基礎的標頭和程式庫</span><span class="sxs-lookup"><span data-stu-id="7189a-134">Media Foundation Headers and Libraries</span></span>](media-foundation-headers-and-libraries.md) | <span data-ttu-id="7189a-135">列出定義媒體基礎 Api 的標頭和程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="7189a-135">Lists the header and library files that define the Media Foundation APIs.</span></span> |
| [<span data-ttu-id="7189a-136">媒體基礎工具</span><span class="sxs-lookup"><span data-stu-id="7189a-136">Media Foundation Tools</span></span>](media-foundation-tools.md)                                 | <span data-ttu-id="7189a-137">描述適用于媒體基礎的開發工具。</span><span class="sxs-lookup"><span data-stu-id="7189a-137">Describes the development tools that are available for Media Foundation.</span></span>  |



 

<span data-ttu-id="7189a-138">媒體基礎不包含在 Windows 8 的 N 和 KN 版本中。</span><span class="sxs-lookup"><span data-stu-id="7189a-138">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="7189a-139">如需詳細資訊，請參閱 [Microsoft Windows Media Feature Pack 的 N 和 KN 版本的所有 Windows 8 版本](https://support.microsoft.com/kb/2703761)。</span><span class="sxs-lookup"><span data-stu-id="7189a-139">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7189a-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="7189a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7189a-141">Microsoft 媒體基礎</span><span class="sxs-lookup"><span data-stu-id="7189a-141">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



