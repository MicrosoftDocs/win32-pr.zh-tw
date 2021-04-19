---
description: 使用時態壓縮的影片編碼
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: 使用時態壓縮 (Microsoft 媒體基礎) 的影片編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983560"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a><span data-ttu-id="716e2-103">使用時態壓縮 (Microsoft 媒體基礎) 的影片編碼</span><span class="sxs-lookup"><span data-stu-id="716e2-103">Video Encoding with Temporal Compression (Microsoft Media Foundation)</span></span>

<span data-ttu-id="716e2-104">為了達到可能的最高壓縮率，Windows Media 視訊編解碼器會使用 *時態性壓縮*。</span><span class="sxs-lookup"><span data-stu-id="716e2-104">To achieve the highest compression ratios possible, the Windows Media Video codecs use *temporal compression*.</span></span> <span data-ttu-id="716e2-105">暫時壓縮是一種減少壓縮影片大小的技巧，而不會將每個畫面格編碼為完整影像。</span><span class="sxs-lookup"><span data-stu-id="716e2-105">Temporal compression is a technique of reducing compressed video size by not encoding each frame as a complete image.</span></span> <span data-ttu-id="716e2-106">完整編碼的框架 (像是靜態影像) ，稱為 *主要畫面* 格。</span><span class="sxs-lookup"><span data-stu-id="716e2-106">The frames that are encoded completely (like a static image) are called *key frames*.</span></span> <span data-ttu-id="716e2-107">影片中的所有其他畫面格都會以指定最後一個畫面格之後變更的資料來表示。</span><span class="sxs-lookup"><span data-stu-id="716e2-107">All other frames in the video are represented by data specifying the change since the last frame.</span></span> <span data-ttu-id="716e2-108">這些框架稱為 *delta 框架*。</span><span class="sxs-lookup"><span data-stu-id="716e2-108">These frames are called *delta frames*.</span></span>

<span data-ttu-id="716e2-109">使用時態壓縮可達成的壓縮量取決於內容。</span><span class="sxs-lookup"><span data-stu-id="716e2-109">The amount of compression that can be achieved using temporal compression depends upon the content.</span></span> <span data-ttu-id="716e2-110">如果影片是靜態的，而沒有大量動作或影像中的其他變更，則可以為每個主要畫面格建立許多差異框架。</span><span class="sxs-lookup"><span data-stu-id="716e2-110">If the video is static, without a lot of motion or other changes in image, many delta frames can be created for each key frame.</span></span> <span data-ttu-id="716e2-111">使用的差異畫面越多，編碼的影片資料流程就越小。</span><span class="sxs-lookup"><span data-stu-id="716e2-111">The more delta frames that are used, the smaller the encoded video stream.</span></span> <span data-ttu-id="716e2-112">但是，如果影片是動態的，則有許多動作或變更色彩，使用時態壓縮的優點較小。</span><span class="sxs-lookup"><span data-stu-id="716e2-112">However, if the video is dynamic, with lots of motion or changing colors, the benefit of using temporal compression is smaller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="716e2-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="716e2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="716e2-114">使用影片</span><span class="sxs-lookup"><span data-stu-id="716e2-114">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



