---
description: 捕獲 DV 至檔案
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: 捕獲 DV 至檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317743"
---
# <a name="capture-dv-to-file"></a><span data-ttu-id="116bf-103">捕獲 DV 至檔案</span><span class="sxs-lookup"><span data-stu-id="116bf-103">Capture DV to File</span></span>

<span data-ttu-id="116bf-104">本節說明如何從 DV 攝影機或 VTR 磁帶捕捉數位視訊 (DV) 。</span><span class="sxs-lookup"><span data-stu-id="116bf-104">This section describes how to capture digital video (DV) from a DV camera or from a VTR tape.</span></span>

1.  <span data-ttu-id="116bf-105">建立 [MSDV 驅動程式](msdv-driver.md) 篩選器的實例。</span><span class="sxs-lookup"><span data-stu-id="116bf-105">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="116bf-106">如需詳細資訊，請參閱 [選取擷取裝置](selecting-a-capture-device.md)。</span><span class="sxs-lookup"><span data-stu-id="116bf-106">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="116bf-107">如 [關於 Capture graph](about-the-capture-graph-builder.md)產生器中所述，初始化 Capture graph builder。</span><span class="sxs-lookup"><span data-stu-id="116bf-107">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
3.  <span data-ttu-id="116bf-108">根據目的檔案類型建立 capture graph：</span><span class="sxs-lookup"><span data-stu-id="116bf-108">Build the capture graph, depending on the target file type:</span></span>
    -   [<span data-ttu-id="116bf-109">捕捉類型 1 DV 檔案</span><span class="sxs-lookup"><span data-stu-id="116bf-109">Capture a Type-1 DV File</span></span>](capture-a-type-1-dv-file.md)
    -   [<span data-ttu-id="116bf-110">捕捉類型 2 DV 檔案</span><span class="sxs-lookup"><span data-stu-id="116bf-110">Capture a Type-2 DV File</span></span>](capture-a-type-2-dv-file.md)
    -   [<span data-ttu-id="116bf-111">將 DV 捕獲到未壓縮的 RGB</span><span class="sxs-lookup"><span data-stu-id="116bf-111">Capture DV to Uncompressed RGB</span></span>](capture-dv-to-uncompressed-rgb.md)
4.  <span data-ttu-id="116bf-112">執行圖形。</span><span class="sxs-lookup"><span data-stu-id="116bf-112">Run the graph.</span></span>

<span data-ttu-id="116bf-113">從 VTR 磁帶進行捕捉的運作方式，就像是從相機中捕捉即時影片，但您必須播放磁帶，如 [控制 DV](controlling-a-dv-camcorder.md)攝影機所述。</span><span class="sxs-lookup"><span data-stu-id="116bf-113">Capturing from a VTR tape works just like capturing live video from the camera, except that you must play the tape, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span> <span data-ttu-id="116bf-114">若要避免遺失任何框架，請先執行圖形，然後播放磁帶。</span><span class="sxs-lookup"><span data-stu-id="116bf-114">To avoid losing any frames, run the graph first, and then play the tape.</span></span> <span data-ttu-id="116bf-115">當您完成傳送時，請先停止磁帶，然後再停止圖形。</span><span class="sxs-lookup"><span data-stu-id="116bf-115">When you are done transmitting, stop the tape first and then stop the graph.</span></span>

> [!Note]  
> <span data-ttu-id="116bf-116">攝像機必須處於 VTR 模式。</span><span class="sxs-lookup"><span data-stu-id="116bf-116">The camcorder must be in VTR mode.</span></span> <span data-ttu-id="116bf-117">請參閱 [裝置模式](device-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="116bf-117">See [Device Mode](device-mode.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="116bf-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="116bf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="116bf-119">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="116bf-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="116bf-120">類型1與類型 2 DV AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="116bf-120">Type-1 vs. Type-2 DV AVI Files</span></span>](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[<span data-ttu-id="116bf-121">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="116bf-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



