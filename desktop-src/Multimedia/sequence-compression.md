---
title: 序列壓縮
description: 序列壓縮
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，序列壓縮
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，序列壓縮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932162"
---
# <a name="sequence-compression"></a><span data-ttu-id="ad171-105">序列壓縮</span><span class="sxs-lookup"><span data-stu-id="ad171-105">Sequence Compression</span></span>

<span data-ttu-id="ad171-106">您的應用程式可以使用 [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)、 [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)和 [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) 函式來壓縮一系列的畫面格。</span><span class="sxs-lookup"><span data-stu-id="ad171-106">Your application can use the [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart), and [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) functions to compress a sequence of frames.</span></span> <span data-ttu-id="ad171-107">這些函數會使用 [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) 結構中所儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="ad171-107">These functions use the data stored in the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure.</span></span> <span data-ttu-id="ad171-108">應用程式會使用 [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) 函式，讓使用者選取壓縮程式、開啟它，並在 **COMPVARS** 結構中設定壓縮參數;不過，應用程式可以手動設定結構中的參數。</span><span class="sxs-lookup"><span data-stu-id="ad171-108">Applications use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to allow the user to select a compressor, open it, and set the compression parameters in the **COMPVARS** structure; however, applications can set the parameters in the structure manually.</span></span>

<span data-ttu-id="ad171-109">在應用程式開始壓縮一系列的畫面格之前，它必須使用 **ICSeqCompressFrameStart** 來配置所需的資源。</span><span class="sxs-lookup"><span data-stu-id="ad171-109">Before an application can begin compressing a sequence of frames, it must use **ICSeqCompressFrameStart** to allocate the necessary resources.</span></span> <span data-ttu-id="ad171-110">配置資源之後，應用程式可以使用 **ICSeqCompressFrame** 來個別壓縮每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="ad171-110">After the resources are allocated, the application can use **ICSeqCompressFrame** to compress each frame individually.</span></span> <span data-ttu-id="ad171-111">用來壓縮順序的畫面播放速率和主要畫面格頻率，是在 **COMPVARS** 結構的成員中指定。</span><span class="sxs-lookup"><span data-stu-id="ad171-111">The frame rate and key-frame frequency used in compressing the sequence are specified in members of the **COMPVARS** structure.</span></span> <span data-ttu-id="ad171-112">**ICSeqCompressFrame** 的傳回值指向壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="ad171-112">The return value for **ICSeqCompressFrame** points to the compressed data.</span></span>

<span data-ttu-id="ad171-113">當應用程式完成序列的壓縮之後，它就可以使用 **ICSeqCompressFrameEnd** 來釋出配置給 **ICSeqCompressFrameStart** 的系統資源。</span><span class="sxs-lookup"><span data-stu-id="ad171-113">When an application finishes compressing a sequence, it can use **ICSeqCompressFrameEnd** to free system resources allocated for **ICSeqCompressFrameStart**.</span></span> <span data-ttu-id="ad171-114">若要釋放配置給 **COMPVARS** 結構的資源，應用程式可以使用 [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) 函數。</span><span class="sxs-lookup"><span data-stu-id="ad171-114">To free the resources allocated for the **COMPVARS** structure, the application can use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function.</span></span>

 

 




