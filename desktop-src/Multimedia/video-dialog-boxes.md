---
title: 影片對話方塊
description: 影片對話方塊
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE 訊息
- capDlgVideoSource 宏
- WM_CAP_DLG_VIDEOFORMAT 訊息
- capDlgVideoFormat 宏
- WM_CAP_DLG_VIDEODISPLAY 訊息
- capDlgVideoDisplay 宏
- WM_CAP_DLG_VIDEOCOMPRESSION 訊息
- capDlgVideoCompression 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965161"
---
# <a name="video-dialog-boxes"></a><span data-ttu-id="9e817-111">影片對話方塊</span><span class="sxs-lookup"><span data-stu-id="9e817-111">Video Dialog Boxes</span></span>

<span data-ttu-id="9e817-112">每個 capture 驅動程式最多可以提供四個對話方塊來控制影片數位化和捕捉流程的各個層面，以及定義用於縮減影片資料大小的壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="9e817-112">Each capture driver can provide up to four dialog boxes to control aspects of the video digitization and capture process, and to define compression attributes used in reducing the size of the video data.</span></span> <span data-ttu-id="9e817-113">這些對話方塊的內容是由影片捕獲驅動程式所定義。</span><span class="sxs-lookup"><span data-stu-id="9e817-113">The contents of these dialog boxes are defined by the video capture driver.</span></span>

<span data-ttu-id="9e817-114">[影片來源] 對話方塊會控制影片輸入頻道和參數的選取專案，這些參數會影響在框架緩衝區中數位化的影片影像。</span><span class="sxs-lookup"><span data-stu-id="9e817-114">The Video Source dialog box controls the selection of video input channels and parameters affecting the video image being digitized in the frame buffer.</span></span> <span data-ttu-id="9e817-115">此對話方塊會列舉將影片來源連接到捕捉卡的信號類型 (通常會 SVHS 和複合輸入) ，並且提供控制項來變更色調、對比或飽和度。</span><span class="sxs-lookup"><span data-stu-id="9e817-115">This dialog box enumerates the types of signals that connect the video source to the capture card (typically SVHS and composite inputs), and provides controls to change hue, contrast, or saturation.</span></span> <span data-ttu-id="9e817-116">如果影片捕獲驅動程式支援此對話方塊，您可以使用 [**WM \_ CAP \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (或 [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) 宏) 來顯示和更新此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9e817-116">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (or the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro).</span></span>

<span data-ttu-id="9e817-117">[影片格式] 對話方塊會控制所捕獲影片的數位化影片框架維度和影像深度，以及壓縮選項。</span><span class="sxs-lookup"><span data-stu-id="9e817-117">The Video Format dialog box controls selection of the digitized video frame dimensions and image-depth, and compression options of the captured video.</span></span> <span data-ttu-id="9e817-118">如果影片捕獲驅動程式支援此對話方塊，您可以使用 [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (或 [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) 宏) 來顯示和更新此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9e817-118">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro).</span></span>

<span data-ttu-id="9e817-119">[影片顯示] 對話方塊會控制在捕捉期間監視的影片外觀。</span><span class="sxs-lookup"><span data-stu-id="9e817-119">The Video Display dialog box controls the appearance of the video on the monitor during capture.</span></span> <span data-ttu-id="9e817-120">此對話方塊中的控制項對數位化的影片資料沒有影響，但可能會影響數位化信號的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="9e817-120">The controls in this dialog box have no effect on the digitized video data, but they might affect the presentation of the digitized signal.</span></span> <span data-ttu-id="9e817-121">例如，捕捉支援重迭的裝置可能會允許改變重迭的色調和飽和度、按鍵色彩或對齊。</span><span class="sxs-lookup"><span data-stu-id="9e817-121">For example, capture devices that support overlay might allow altering hue and saturation, key color, or alignment of the overlay.</span></span> <span data-ttu-id="9e817-122">如果影片捕獲驅動程式支援此對話方塊，您可以使用 [**WM \_ CAP \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (或 [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) 宏) 來顯示和更新此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9e817-122">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (or the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro).</span></span>

<span data-ttu-id="9e817-123">[影片壓縮] 對話方塊會控制後續的影片壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="9e817-123">The Video Compression dialog box controls the post-capture video compression attributes.</span></span> <span data-ttu-id="9e817-124">如果影片捕獲驅動程式支援此對話方塊，您可以使用 [**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (或 [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) 宏) 來顯示和更新此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9e817-124">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (or the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro).</span></span>

 

 




