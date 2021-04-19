---
description: Per-Pixel Alpha 混色
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel Alpha 混色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000041"
---
# <a name="per-pixel-alpha-blending"></a><span data-ttu-id="6f377-103">Per-Pixel Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="6f377-103">Per-Pixel Alpha Blending</span></span>

<span data-ttu-id="6f377-104">已針對每個圖元的 Alpha 混色定義四個媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="6f377-104">Four media subtypes have been defined for per-pixel alpha blending.</span></span> <span data-ttu-id="6f377-105">只有當 VMR 處於混合模式時，才支援這些子類型。</span><span class="sxs-lookup"><span data-stu-id="6f377-105">These subtypes are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="6f377-106">當上游篩選嘗試使用其中一個子類型進行連線時，如果連線不在混合模式中，VMR 將會拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="6f377-106">The VMR will reject the connection if it is not in mixing mode when an upstream filter attempts to connect using one of these subtypes.</span></span> <span data-ttu-id="6f377-107">這些子類型定義于 uuid 中：</span><span class="sxs-lookup"><span data-stu-id="6f377-107">These subtypes are defined in uuids.h:</span></span>

-   <span data-ttu-id="6f377-108">MEDIASUBTYPE \_ ARGB1555</span><span class="sxs-lookup"><span data-stu-id="6f377-108">MEDIASUBTYPE\_ARGB1555</span></span>
-   <span data-ttu-id="6f377-109">MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="6f377-109">MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="6f377-110">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="6f377-110">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="6f377-111">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="6f377-111">MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="6f377-112">如需詳細資訊，請參閱 [未壓縮的 RGB 影片子類型](uncompressed-rgb-video-subtypes.md) 和 [**YUV 影片子類型**](yuv-video-subtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="6f377-112">For more information, see [Uncompressed RGB Video Subtypes](uncompressed-rgb-video-subtypes.md) and [**YUV Video Subtypes**](yuv-video-subtypes.md).</span></span>

 

 



