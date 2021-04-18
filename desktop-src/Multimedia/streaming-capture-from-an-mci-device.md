---
title: 從 MCI 裝置串流捕獲
description: 從 MCI 裝置串流捕獲
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (媒體控制介面) 、串流捕獲
- WM_CAP_SET_MCI_DEVICE 訊息
- capSetMCIDeviceName 宏
- WM_CAP_GET_MCI_DEVICE 訊息
- capGetMCIDeviceName 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8cf358a87a812024328abf7fc1aae0509a126f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507373"
---
# <a name="streaming-capture-from-an-mci-device"></a><span data-ttu-id="d8d45-108">從 MCI 裝置串流捕獲</span><span class="sxs-lookup"><span data-stu-id="d8d45-108">Streaming Capture from an MCI Device</span></span>

<span data-ttu-id="d8d45-109">MCI 裝置會在即時捕捉和逐步執行框架捕獲中增強捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="d8d45-109">MCI devices augment the capture operation in real-time capture and step-frame capture.</span></span> <span data-ttu-id="d8d45-110">您可以使用 [ [**WM \_ CAP \_ SET \_ MCI \_ 裝置**](wm-cap-set-mci-device.md) 訊息] (或 [ [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) ] 宏) 並指定裝置的名稱，指定 MCI 裝置，例如 videodisc 或攝影機 (VCR) ，作為您的捕獲操作影片來源。</span><span class="sxs-lookup"><span data-stu-id="d8d45-110">You can specify the MCI device, such as a videodisc or video-cassette recorder (VCR), acting as the video source for your capture operation by using the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message (or the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro) and specifying the name of the device.</span></span> <span data-ttu-id="d8d45-111">您也可以使用 [ [**WM \_ CAP \_ 取得 \_ MCI \_ 裝置**](wm-cap-get-mci-device.md) 訊息 (] 或 [ [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) 宏) ，來取出目前設定的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="d8d45-111">You can also retrieve the device name currently set by using the [**WM\_CAP\_GET\_MCI\_DEVICE**](wm-cap-get-mci-device.md) message (or the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro).</span></span>

<span data-ttu-id="d8d45-112">在即時捕捉中，[捕獲] 視窗會同步處理捕獲作業，並補償與放置 MCI 影片來源和初始化 (資源相關的延遲（例如捕獲資料時所需的擷取緩衝區) ）。</span><span class="sxs-lookup"><span data-stu-id="d8d45-112">In real-time capture, the capture window synchronizes the capture operation and compensates for delays associated with positioning the MCI video source and initializing the resources (such as capture buffers) required for capturing data.</span></span> <span data-ttu-id="d8d45-113">[Capture （capture）] 視窗預期在系統中安裝有效的 MCI video 裝置，以透過這種方式來捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="d8d45-113">The capture window expects a valid MCI video device to be installed in the system for capturing data this way.</span></span>

<span data-ttu-id="d8d45-114">控制 MCI 裝置的規格會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構的成員中。</span><span class="sxs-lookup"><span data-stu-id="d8d45-114">Specifications for controlling an MCI device are stored in the members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="d8d45-115">MCI 相容的影片來源包含 Vcr 和 laserdiscs。</span><span class="sxs-lookup"><span data-stu-id="d8d45-115">MCI-compatible video sources include VCRs and laserdiscs.</span></span> <span data-ttu-id="d8d45-116">如果此結構的 **fMCIControl** 成員設定為 **TRUE**，則 [捕獲] 視窗會協調 MCI 作業。</span><span class="sxs-lookup"><span data-stu-id="d8d45-116">If the **fMCIControl** member of this structure is set to **TRUE**, the capture window coordinates MCI operation.</span></span> <span data-ttu-id="d8d45-117">[捕獲] 視窗會使用 **dwMCIStartTime** 和 **dwMCIStopTime** 成員中指定的參數，來取得序列的開始和停止位置（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8d45-117">The capture window uses the parameters specified in the **dwMCIStartTime** and **dwMCIStopTime** members to obtain the starting and stopping positions, in milliseconds, of the sequence.</span></span> <span data-ttu-id="d8d45-118">如果 **fMCIControl** 的值為 **FALSE**，則不會將影片來源視為 MCI 裝置，而且會忽略 **dwMCIStartTime** 和 **dwMCIStopTime** 的內容。</span><span class="sxs-lookup"><span data-stu-id="d8d45-118">If the value of **fMCIControl** is **FALSE**, the video source is not treated as an MCI device and the contents of **dwMCIStartTime** and **dwMCIStopTime** are ignored.</span></span>

<span data-ttu-id="d8d45-119">您可以使用 Media Player 快速確認 MCI video 裝置已正確連接至系統。</span><span class="sxs-lookup"><span data-stu-id="d8d45-119">You can use Media Player to quickly verify that an MCI video device is properly connected to the system.</span></span> <span data-ttu-id="d8d45-120">使用 Media Player 播放裝置會確認裝置的 MCI 設定是否正確。</span><span class="sxs-lookup"><span data-stu-id="d8d45-120">Playing a device with Media Player verifies that the MCI configuration for the device is correct.</span></span> <span data-ttu-id="d8d45-121">如果影像顯示在影片顯示器上，則影片來源會正確地連接到「捕獲硬體」。</span><span class="sxs-lookup"><span data-stu-id="d8d45-121">If an image appears on the video display, the video source is connected properly to the capture hardware.</span></span>

<span data-ttu-id="d8d45-122">在 [逐步執行] 視窗中，[捕獲] 視窗會同步處理捕獲作業，並補償與放置 MCI 影片來源和初始化所需資源的相關延遲。</span><span class="sxs-lookup"><span data-stu-id="d8d45-122">In step-frame capture, the capture window synchronizes the capture operation and compensates for the delays associated with positioning the MCI video source and initializing the resources required for capturing data.</span></span> <span data-ttu-id="d8d45-123">此外，[capture （capture）] 視窗可確保不會卸載任何框架;它會個別逐步執行影片畫面，以確保在影片串流中的下一個畫面格之前，會先捕捉並儲存畫面格。</span><span class="sxs-lookup"><span data-stu-id="d8d45-123">In addition, the capture window ensures that no frames are dropped; it steps through the video frames individually, ensuring that the frame is captured and stored before capturing the next frame in the video stream.</span></span>

<span data-ttu-id="d8d45-124">控制步驟框架捕獲的規格會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構的成員中。</span><span class="sxs-lookup"><span data-stu-id="d8d45-124">Specifications for controlling step-frame capture are stored in the members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="d8d45-125">除了用於即時捕捉的成員之外，步驟框架捕獲還會使用下列成員： **fStepMCIDevice**、 **fStepCaptureAt2x** 和 **wStepCaptureAverageFrames**。</span><span class="sxs-lookup"><span data-stu-id="d8d45-125">Step-frame capture uses the following members in addition to the members used for real-time capture: **fStepMCIDevice**, **fStepCaptureAt2x**, and **wStepCaptureAverageFrames**.</span></span> <span data-ttu-id="d8d45-126">如果 **fStepMCIDevice** 成員設定為 **TRUE**，則 [捕獲] 視窗會協調步驟框架捕獲。</span><span class="sxs-lookup"><span data-stu-id="d8d45-126">If the **fStepMCIDevice** member is set to **TRUE**, the capture window coordinates step-frame capture.</span></span> <span data-ttu-id="d8d45-127">[捕獲] 視窗會使用 **dwMCIStartTime** 和 **dwMCIStopTime** 成員中指定的參數，來進行序列的開始和停止位置（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8d45-127">The capture window uses the parameters specified in the **dwMCIStartTime** and **dwMCIStopTime** members for the starting and stopping positions, in milliseconds, of the sequence.</span></span> <span data-ttu-id="d8d45-128">[Capture （capture）] 視窗會使用 **fStepCaptureAt2x** 來判斷捕獲硬體是否應該以一般解析度的兩倍來捕獲影片畫面，並使用 **wStepCaptureAverageFrames** 來指定取樣的每個畫面格所經過的次數。</span><span class="sxs-lookup"><span data-stu-id="d8d45-128">The capture window uses **fStepCaptureAt2x** to determine if the capture hardware should capture video frames at twice the normal resolution and uses **wStepCaptureAverageFrames** to specify the number of times each frame in the capture operation is sampled.</span></span>

<span data-ttu-id="d8d45-129">如果 **fStepMCIDevice** 為 **FALSE**，則會使用即時捕捉，而不是逐步執行框架捕獲和 **fStepCaptureAt2x** 的內容，而且會忽略 **wStepCaptureAverageFrames** 。</span><span class="sxs-lookup"><span data-stu-id="d8d45-129">If **fStepMCIDevice** is **FALSE**, real-time capture is used instead of step-frame capture and the contents of **fStepCaptureAt2x**, and **wStepCaptureAverageFrames** are ignored.</span></span>

<span data-ttu-id="d8d45-130">如果指定了步驟框架捕獲，且 **fStepCaptureAt2x** 設定為 **TRUE**，則捕獲硬體會以指定的解析度兩倍來捕捉。</span><span class="sxs-lookup"><span data-stu-id="d8d45-130">If a step-frame capture is specified and **fStepCaptureAt2x** is set to **TRUE**, the capture hardware captures at twice the specified resolution.</span></span> <span data-ttu-id="d8d45-131"> (高度和寬度的解析度加倍。 ) 軟體會將圖元插在較高解析度的影像中，以指定的解析度產生映射。</span><span class="sxs-lookup"><span data-stu-id="d8d45-131">(The resolutions of both the height and width are doubled.) The software interpolates the pixels in the higher resolution image to produce the image at the specified resolution.</span></span> <span data-ttu-id="d8d45-132">這種形式的平均可以改善框架中影像的邊緣定義。</span><span class="sxs-lookup"><span data-stu-id="d8d45-132">This form of averaging can improve the edge definition of images in a frame.</span></span> <span data-ttu-id="d8d45-133">如果硬體不支援以硬體為基礎的減去，而且您是以 RGB 格式進行捕捉，則可以啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="d8d45-133">You can enable this option if the hardware does not support hardware-based decimation and you are capturing in the RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="d8d45-134">如果您的硬體支援以硬體為基礎的減去，它可以以比指定更高的速率來捕捉範例，並使用這些額外的範例來取得與原始影像更一致的色彩定義。</span><span class="sxs-lookup"><span data-stu-id="d8d45-134">If your hardware supports hardware-based decimation, it can capture samples at a higher rate than specified and use these additional samples to obtain color definitions that are more consistent with the original image.</span></span> <span data-ttu-id="d8d45-135">使用之後會捨棄額外的範例，而硬體會以指定的速率將範例傳至 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d8d45-135">The additional samples are discarded after they are used, and the hardware passes samples to the capture driver at the specified rate.</span></span>

 

<span data-ttu-id="d8d45-136">如果指定了步驟框架捕獲， **wStepCaptureAverageFrames** 成員會指定根據平均範例建立框架時，所取樣的框架次數。</span><span class="sxs-lookup"><span data-stu-id="d8d45-136">If a step-frame capture is specified, the **wStepCaptureAverageFrames** member specifies the number of times a frame is sampled when creating a frame based on the average sample.</span></span> <span data-ttu-id="d8d45-137">這種平均技術可減少出現在框架中的亂數字化雜訊。</span><span class="sxs-lookup"><span data-stu-id="d8d45-137">This averaging technique reduces the random digitization noise appearing in a frame.</span></span> <span data-ttu-id="d8d45-138">平均值的一般值為5。</span><span class="sxs-lookup"><span data-stu-id="d8d45-138">A typical value for the number of averages is 5.</span></span>

<span data-ttu-id="d8d45-139">如需 MCI 的詳細資訊，請參閱 [mci](mci.md)。</span><span class="sxs-lookup"><span data-stu-id="d8d45-139">For more information about MCI, see [MCI](mci.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8d45-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8d45-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8d45-141">捕捉變化</span><span class="sxs-lookup"><span data-stu-id="d8d45-141">Capture Variations</span></span>](capture-variations.md)
</dt> </dl>

 

 




