---
description: 說明如何使用 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 。
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: DXVA-HD 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847633"
---
# <a name="dxva-hd-sample"></a><span data-ttu-id="74b6e-103">DXVA-HD 範例</span><span class="sxs-lookup"><span data-stu-id="74b6e-103">DXVA-HD Sample</span></span>

<span data-ttu-id="74b6e-104">說明如何使用 Microsoft DirectX Video 加速 High Definition (DXVA-HD) 。</span><span class="sxs-lookup"><span data-stu-id="74b6e-104">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>

<span data-ttu-id="74b6e-105">此範例本質上是 [DXVA2 \_ VideoProc 範例](dxva2-videoproc-sample.md)的埠。</span><span class="sxs-lookup"><span data-stu-id="74b6e-105">This sample is essentially a port of the [DXVA2\_VideoProc Sample](dxva2-videoproc-sample.md).</span></span> <span data-ttu-id="74b6e-106">它具有相同的基本功能，而大部分的鍵盤命令都相同。</span><span class="sxs-lookup"><span data-stu-id="74b6e-106">It has the same basic functions, and most of the keyboard commands are the same.</span></span>

<span data-ttu-id="74b6e-107">此範例會以程式設計方式產生具有主要資料流程和子資料流程的影片。</span><span class="sxs-lookup"><span data-stu-id="74b6e-107">The sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="74b6e-108">主要資料流程會顯示 SMPTE 色軸。</span><span class="sxs-lookup"><span data-stu-id="74b6e-108">The primary stream displays SMPTE color bars.</span></span> <span data-ttu-id="74b6e-109">子資料流程會使用 luma 金鑰混合在主要資料流程上進行 Alpha 混合。</span><span class="sxs-lookup"><span data-stu-id="74b6e-109">The substream is alpha-blended onto the primary stream using luma keying.</span></span> <span data-ttu-id="74b6e-110">使用者可以變更影片處理參數，包括平面 Alpha 值、來源和目的地矩形、色彩調整和色彩空間。</span><span class="sxs-lookup"><span data-stu-id="74b6e-110">The user can change the video processing parameters, including the planar alpha value, source and destination rectangles, color adjustments, and color space.</span></span> <span data-ttu-id="74b6e-111">下圖顯示產生的影片。</span><span class="sxs-lookup"><span data-stu-id="74b6e-111">The following image shows that video that is generated.</span></span>

![dxva-hd 範例的螢幕擷取畫面](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="74b6e-113">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="74b6e-113">APIs Demonstrated</span></span>

<span data-ttu-id="74b6e-114">此範例示範下列 DXVA HD 介面：</span><span class="sxs-lookup"><span data-stu-id="74b6e-114">This sample demonstrates the following DXVA-HD interfaces:</span></span>

-   [<span data-ttu-id="74b6e-115">**IDXVAHD \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="74b6e-115">**IDXVAHD\_Device**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [<span data-ttu-id="74b6e-116">**IDXVAHD \_ VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="74b6e-116">**IDXVAHD\_VideoProcessor**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a><span data-ttu-id="74b6e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="74b6e-117">Requirements</span></span>



| <span data-ttu-id="74b6e-118">產品</span><span class="sxs-lookup"><span data-stu-id="74b6e-118">Product</span></span>                                                        | <span data-ttu-id="74b6e-119">版本</span><span class="sxs-lookup"><span data-stu-id="74b6e-119">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="74b6e-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="74b6e-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="74b6e-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74b6e-121">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="74b6e-122">下載範例</span><span class="sxs-lookup"><span data-stu-id="74b6e-122">Downloading the Sample</span></span>

<span data-ttu-id="74b6e-123">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD)中取得。</span><span class="sxs-lookup"><span data-stu-id="74b6e-123">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74b6e-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="74b6e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74b6e-125">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="74b6e-125">DXVA-HD</span></span>](dxva-hd.md)
</dt> <dt>

[<span data-ttu-id="74b6e-126">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="74b6e-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



