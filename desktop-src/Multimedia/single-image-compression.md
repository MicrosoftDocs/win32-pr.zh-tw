---
title: Single-Image 壓縮
description: Single-Image 壓縮
ms.assetid: 8e2273f6-c9f4-4b1f-9db4-de031902a630
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) 、單一映射壓縮
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) 、單一影像壓縮
- ICImageCompress 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4fc8132a515fea20c730d4ffc46a8eb6fb4273
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184135"
---
# <a name="single-image-compression"></a><span data-ttu-id="4b47b-106">Single-Image 壓縮</span><span class="sxs-lookup"><span data-stu-id="4b47b-106">Single-Image Compression</span></span>

<span data-ttu-id="4b47b-107">您可以使用 [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress) 函式來壓縮單一映射。</span><span class="sxs-lookup"><span data-stu-id="4b47b-107">You can use the [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress) function to compress a single image.</span></span> <span data-ttu-id="4b47b-108">此函式會傳回壓縮的裝置獨立點陣圖 (DIB) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4b47b-108">This function returns a handle of the compressed device-independent bitmap (DIB).</span></span> <span data-ttu-id="4b47b-109">壓縮的 DIB 會使用 CF \_ DIB 格式來封裝。</span><span class="sxs-lookup"><span data-stu-id="4b47b-109">The compressed DIB is packed using the CF\_DIB format.</span></span>

 

 




