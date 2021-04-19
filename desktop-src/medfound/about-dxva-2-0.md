---
description: DXVA 2 以及其與 DXVA 1 的關聯性總覽。
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: 關於 DXVA 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970624"
---
# <a name="about-dxva-20"></a><span data-ttu-id="e9111-103">關於 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="e9111-103">About DXVA 2.0</span></span>

<span data-ttu-id="e9111-104">DirectX Video 加速 (DXVA) 是 API 和對應的 DDI，可使用硬體加速來加速影片處理。</span><span class="sxs-lookup"><span data-stu-id="e9111-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware acceleration to speed up video processing.</span></span> <span data-ttu-id="e9111-105">軟體編解碼器和軟體視頻處理器可以使用 DXVA，將某些需要大量 CPU 的作業卸載至 GPU。</span><span class="sxs-lookup"><span data-stu-id="e9111-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="e9111-106">例如，軟體解碼器可以卸載反向離散余弦轉換 (iDCT) 至 GPU。</span><span class="sxs-lookup"><span data-stu-id="e9111-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="e9111-107">在 DXVA 中，某些解碼作業是由圖形硬體驅動程式所執行。</span><span class="sxs-lookup"><span data-stu-id="e9111-107">In DXVA, some decoding operations are implemented by the graphics hardware driver.</span></span> <span data-ttu-id="e9111-108">這組功能稱為 *加速器*。</span><span class="sxs-lookup"><span data-stu-id="e9111-108">This set of functionality is termed the *accelerator*.</span></span> <span data-ttu-id="e9111-109">其他解碼作業是由使用者模式應用程式軟體（稱為 *主機解碼* 或 *軟體解碼器*）所執行。</span><span class="sxs-lookup"><span data-stu-id="e9111-109">Other decoding operations are implemented by user-mode application software, called the *host decoder* or *software decoder*.</span></span> <span data-ttu-id="e9111-110"> (「 *主機解碼器* 」和「 *軟體解碼器* 」等詞彙都相等。此加速器所執行的 ) 處理稱為「 *外部主機處理*」。</span><span class="sxs-lookup"><span data-stu-id="e9111-110">(The terms *host decoder* and *software decoder* are equivalent.) Processing performed by the accelerator is called *off-host processing*.</span></span> <span data-ttu-id="e9111-111">加速器通常會使用 GPU 來加速某些作業。</span><span class="sxs-lookup"><span data-stu-id="e9111-111">Typically the accelerator uses the GPU to speed up some operations.</span></span> <span data-ttu-id="e9111-112">每當加速器執行解碼作業時，主機解碼必須傳遞至包含執行作業所需資訊的加速器緩衝區</span><span class="sxs-lookup"><span data-stu-id="e9111-112">Whenever the accelerator performs a decoding operation, the host decoder must convey to the accelerator buffers containing the information needed to perform the operation</span></span>

<span data-ttu-id="e9111-113">DXVA 2 API 需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e9111-113">The DXVA 2 API requires Windows Vista or later.</span></span> <span data-ttu-id="e9111-114">Windows Vista 仍支援 DXVA 1 API，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="e9111-114">The DXVA 1 API is still supported in Windows Vista for backward compatibility.</span></span> <span data-ttu-id="e9111-115">系統會提供模擬層，以在任一版本的 API 和相反版本的 DDI 之間進行轉換：</span><span class="sxs-lookup"><span data-stu-id="e9111-115">An emulation layer is provided that converts between either version of the API and the opposite version of the DDI:</span></span>

-   <span data-ttu-id="e9111-116">如果圖形驅動程式符合 Windows 顯示驅動程式模型 (WDDM) ，DXVA 1 API 呼叫會轉換成 DXVA 2 DDI 呼叫。</span><span class="sxs-lookup"><span data-stu-id="e9111-116">If the graphics driver conforms to the Windows Display Driver Model (WDDM), DXVA 1 API calls are converted to DXVA 2 DDI calls.</span></span>
-   <span data-ttu-id="e9111-117">如果圖形驅動程式使用舊版的 Windows XP 顯示驅動程式模型 (XPDM) ，DXVA 2 API 呼叫會轉換成 DXVA 1 DDI 呼叫。</span><span class="sxs-lookup"><span data-stu-id="e9111-117">If the graphics drivers uses the older Windows XP Display Driver Model (XPDM), DXVA 2 API calls are converted to DXVA 1 DDI calls.</span></span>

<span data-ttu-id="e9111-118">下表顯示每個 DXVA API 版本的作業系統需求和支援的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="e9111-118">The following table shows the operating system requirements and the supported video renderers for each version of the DXVA API.</span></span>



| <span data-ttu-id="e9111-119">API 版本</span><span class="sxs-lookup"><span data-stu-id="e9111-119">API Version</span></span> | <span data-ttu-id="e9111-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9111-120">Requirements</span></span>          | <span data-ttu-id="e9111-121">影片轉譯器支援</span><span class="sxs-lookup"><span data-stu-id="e9111-121">Video Renderer Support</span></span>                        |
|-------------|-----------------------|-----------------------------------------------|
| <span data-ttu-id="e9111-122">DXVA 1</span><span class="sxs-lookup"><span data-stu-id="e9111-122">DXVA 1</span></span>      | <span data-ttu-id="e9111-123">Windows 2000 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e9111-123">Windows 2000 or later</span></span> | <span data-ttu-id="e9111-124">重迭混音器、VMR-7、VMR-9 (DirectShow 僅) </span><span class="sxs-lookup"><span data-stu-id="e9111-124">Overlay Mixer, VMR-7, VMR-9 (DirectShow only)</span></span> |
| <span data-ttu-id="e9111-125">DXVA 2</span><span class="sxs-lookup"><span data-stu-id="e9111-125">DXVA 2</span></span>      | <span data-ttu-id="e9111-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9111-126">Windows Vista</span></span>         | <span data-ttu-id="e9111-127">EVR (DirectShow 和媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="e9111-127">EVR (DirectShow and Media Foundation)</span></span>         |



 

<span data-ttu-id="e9111-128">在 DXVA 1 中，軟體解碼器必須透過影片轉譯器存取 API。</span><span class="sxs-lookup"><span data-stu-id="e9111-128">In DXVA 1, the software decoder must access the API through the video renderer.</span></span> <span data-ttu-id="e9111-129">沒有任何方法可以使用 DXVA 1 API，而不需要呼叫影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="e9111-129">There is no way to use the DXVA 1 API without calling into the video renderer.</span></span> <span data-ttu-id="e9111-130">DXVA 2 已移除這項限制。</span><span class="sxs-lookup"><span data-stu-id="e9111-130">This limitation has been removed with DXVA 2.</span></span> <span data-ttu-id="e9111-131">使用 DXVA 2，主機解碼 (或任何應用程式) 都可以透過 [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面直接存取 API。</span><span class="sxs-lookup"><span data-stu-id="e9111-131">Using DXVA 2, the host decoder (or any application) can access the API directly, through the [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>

<span data-ttu-id="e9111-132">DXVA 1 檔說明用於下列影片標準的解碼結構：</span><span class="sxs-lookup"><span data-stu-id="e9111-132">The DXVA 1 documentation describes the decoding structures used for the following video standards:</span></span>

-   <span data-ttu-id="e9111-133">ITU-T Rec. H. 261</span><span class="sxs-lookup"><span data-stu-id="e9111-133">ITU-T Rec. H.261</span></span>
-   <span data-ttu-id="e9111-134">ITU-T Rec</span><span class="sxs-lookup"><span data-stu-id="e9111-134">ITU-T Rec. H.263</span></span>
-   <span data-ttu-id="e9111-135">MPEG-2 影片</span><span class="sxs-lookup"><span data-stu-id="e9111-135">MPEG-1 video</span></span>
-   <span data-ttu-id="e9111-136">MPEG-2 主要設定檔影片</span><span class="sxs-lookup"><span data-stu-id="e9111-136">MPEG-2 Main Profile video</span></span>

<span data-ttu-id="e9111-137">下列規格定義適用于其他影片標準的 DXVA 延伸模組：</span><span class="sxs-lookup"><span data-stu-id="e9111-137">The following specifications define DXVA extensions for other video standards:</span></span>

-   [<span data-ttu-id="e9111-138">H.264/AVC 解碼的 DXVA 規格</span><span class="sxs-lookup"><span data-stu-id="e9111-138">DXVA Specification for H.264/AVC Decoding</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [<span data-ttu-id="e9111-139">DXVA 規格： h.264/MPEG-2 AVC 多型的) 多型影片編碼 (MVC，包括身歷聲 High 設定檔</span><span class="sxs-lookup"><span data-stu-id="e9111-139">DXVA Specification for H.264/MPEG-4 AVC Multiview Video Coding (MVC), Including the Stereo High Profile</span></span>](https://www.microsoft.com/download/details.aspx?id=25200)
-   <span data-ttu-id="e9111-140">[MPEG-2 VLD 的 DXVA 規格和組合的 mpeg-2/MPEG-2 VLD 影片解碼](https://www.microsoft.com/download/details.aspx?id=9374)。</span><span class="sxs-lookup"><span data-stu-id="e9111-140">[DXVA Specification for MPEG-1 VLD and Combined MPEG-1/MPEG-2 VLD Video Decoding](https://www.microsoft.com/download/details.aspx?id=9374).</span></span>
-   [<span data-ttu-id="e9111-141">適用于 MPEG-2 的 Off-Host VLD 模式的 DXVA 規格第2部分影片解碼</span><span class="sxs-lookup"><span data-stu-id="e9111-141">DXVA Specification for Off-Host VLD Mode for MPEG-4 Part 2 Video Decoding</span></span>](https://www.microsoft.com/download/details.aspx?id=21100)
-   [<span data-ttu-id="e9111-142">Windows Media 視訊® v8、v9 和 vA 解碼 (的 DXVA 規格，包括 SMPTE 421M "VC-1" ) </span><span class="sxs-lookup"><span data-stu-id="e9111-142">DXVA Specification for Windows Media Video® v8, v9 and vA Decoding (Including SMPTE 421M "VC-1")</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [<span data-ttu-id="e9111-143">DirectX Video 加速 (DXVA) 規格，適用于 h.264/MPEG 4 可調整的影片編碼 (SVC) Off-Host VLD 模式解碼</span><span class="sxs-lookup"><span data-stu-id="e9111-143">DirectX Video Acceleration (DXVA) Specification for H.264/MPEG-4 Scalable Video Coding (SVC) Off-Host VLD Mode Decoding</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [<span data-ttu-id="e9111-144">適用于 VP8 和 VP9 影片編碼的 DirectX 影片加速規格</span><span class="sxs-lookup"><span data-stu-id="e9111-144">DirectX Video Acceleration Specification for VP8 and VP9 Video Coding</span></span>](https://www.microsoft.com/download/details.aspx?id=49188)

<span data-ttu-id="e9111-145">DXVA 1 和 DXVA 2 使用相同的資料結構進行解碼。</span><span class="sxs-lookup"><span data-stu-id="e9111-145">DXVA 1 and DXVA 2 use the same data structures for decoding.</span></span> <span data-ttu-id="e9111-146">不過，設定解碼會話的程式已變更。</span><span class="sxs-lookup"><span data-stu-id="e9111-146">However, the procedure for configuring the decoding session has changed.</span></span> <span data-ttu-id="e9111-147">DXVA 1 使用「探查和鎖定」機制，其中主機解碼器可以測試各種設定，然後在加速器上設定所需的設定。</span><span class="sxs-lookup"><span data-stu-id="e9111-147">DXVA 1 uses a "probe and lock" mechanism, wherein the host decoder can test various configurations before setting the desired configuration on the accelerator.</span></span> <span data-ttu-id="e9111-148">在 DXVA 2 中，加速器會傳回一份支援的設定清單，而主機解碼器會從清單中選取一個。</span><span class="sxs-lookup"><span data-stu-id="e9111-148">In DXVA 2, the accelerator returns a list of supported configurations and the host decoder selects one from the list.</span></span> <span data-ttu-id="e9111-149">下列各節提供詳細資料：</span><span class="sxs-lookup"><span data-stu-id="e9111-149">Details are given in the following sections:</span></span>

-   [<span data-ttu-id="e9111-150">支援 DirectShow 中的 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="e9111-150">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)
-   [<span data-ttu-id="e9111-151">媒體基礎中支援 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="e9111-151">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a><span data-ttu-id="e9111-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9111-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9111-153">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="e9111-153">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="e9111-154">DXVA 1.0 規格</span><span class="sxs-lookup"><span data-stu-id="e9111-154">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
