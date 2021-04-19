---
description: 影片捕獲介面
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: 影片捕獲介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974348"
---
# <a name="video-capture-interfaces"></a><span data-ttu-id="cdc6f-103">影片捕獲介面</span><span class="sxs-lookup"><span data-stu-id="cdc6f-103">Video Capture Interfaces</span></span>

<span data-ttu-id="cdc6f-104">這些介面支援影片捕捉、使用 Microsoft® Windows®驅動程式模型 (WDM) 裝置或適用于 Windows®® VFW (裝置的舊版 Microsoft) 影片。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-104">These interfaces support video capture, using Microsoft® Windows® Driver Model (WDM) devices or legacy Microsoft® Video for Windows® (VFW) devices.</span></span>



| <span data-ttu-id="cdc6f-105">介面</span><span class="sxs-lookup"><span data-stu-id="cdc6f-105">Interface</span></span>                                                        | <span data-ttu-id="cdc6f-106">描述</span><span class="sxs-lookup"><span data-stu-id="cdc6f-106">Description</span></span>                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdc6f-107">**IAMAnalogVideoDecoder**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-107">**IAMAnalogVideoDecoder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | <span data-ttu-id="cdc6f-108">控制 WDM 視頻捕捉卡上的影片數位化。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-108">Control video digitization on a WDM video capture card.</span></span>                                                      |
| [<span data-ttu-id="cdc6f-109">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-109">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | <span data-ttu-id="cdc6f-110">控制 pin 如何分配緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-110">Control how a pin allocates buffers.</span></span>                                                                         |
| [<span data-ttu-id="cdc6f-111">**IAMCopyCaptureFileProgress**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-111">**IAMCopyCaptureFileProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | <span data-ttu-id="cdc6f-112">用來接收檔案複製作業進度的回呼介面。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-112">Callback interface to receive the progress of a file copy operation.</span></span>                                         |
| [<span data-ttu-id="cdc6f-113">**IAMCrossbar**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-113">**IAMCrossbar**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | <span data-ttu-id="cdc6f-114">在 WDM 音訊或影片來源和 WDM 捕獲裝置之間建立硬體連接。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-114">Create a hardware connection between a WDM audio or video source and a WDM capture device.</span></span>                   |
| [<span data-ttu-id="cdc6f-115">**IAMDroppedFrames**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-115">**IAMDroppedFrames**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | <span data-ttu-id="cdc6f-116">查詢有關捕獲效能的捕獲篩選。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-116">Query a capture filter about capture performance.</span></span>                                                            |
| [<span data-ttu-id="cdc6f-117">**IAMStreamControl**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-117">**IAMStreamControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | <span data-ttu-id="cdc6f-118">控制個別資料流程的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-118">Control the start and stop times of individual streams.</span></span>                                                      |
| [<span data-ttu-id="cdc6f-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | <span data-ttu-id="cdc6f-120">查詢並設定捕獲篩選器的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-120">Query and set the capture filter's output format.</span></span>                                                            |
| [<span data-ttu-id="cdc6f-121">**IAMVfwCaptureDialogs**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-121">**IAMVfwCaptureDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | <span data-ttu-id="cdc6f-122">顯示 VFW capture 驅動程式所提供的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-122">Display the dialog boxes provided by VFW capture drivers.</span></span>                                                    |
| [<span data-ttu-id="cdc6f-123">**IAMVideoControl**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-123">**IAMVideoControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | <span data-ttu-id="cdc6f-124">從捕獲裝置控制圖片。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-124">Control the picture from a capture device.</span></span>                                                                   |
| [<span data-ttu-id="cdc6f-125">**IAMVideoProcAmp**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-125">**IAMVideoProcAmp**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | <span data-ttu-id="cdc6f-126">調整視訊訊號的品質，例如亮度、對比、色調、飽和度、gamma 和清晰度。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-126">Adjust the qualities of a video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.</span></span> |
| [<span data-ttu-id="cdc6f-127">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-127">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | <span data-ttu-id="cdc6f-128">影片捕獲的組建篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-128">Build filter graphs for video capture.</span></span>                                                                       |
| [<span data-ttu-id="cdc6f-129">**IFileSinkFilter2**</span><span class="sxs-lookup"><span data-stu-id="cdc6f-129">**IFileSinkFilter2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | <span data-ttu-id="cdc6f-130">指定輸出檔的名稱和屬性。</span><span class="sxs-lookup"><span data-stu-id="cdc6f-130">Specify the name and attributes of an output file.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="cdc6f-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="cdc6f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdc6f-132">外部裝置控制介面</span><span class="sxs-lookup"><span data-stu-id="cdc6f-132">External Device Control Interfaces</span></span>](external-device-control-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cdc6f-133">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="cdc6f-133">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



