---
description: 頂點補間會將兩個使用者提供的位置混合 (或法線) 。
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: " (Direct3D 9) 的頂點補間"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187494"
---
# <a name="vertex-tweening-direct3d-9"></a><span data-ttu-id="85711-103"> (Direct3D 9) 的頂點補間</span><span class="sxs-lookup"><span data-stu-id="85711-103">Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="85711-104">頂點補間會將兩個使用者提供的位置混合 (或法線) 。</span><span class="sxs-lookup"><span data-stu-id="85711-104">Vertex tweening blends two user-provided positions (or normals).</span></span> <span data-ttu-id="85711-105">補間與加權的頂點混合互相排斥。</span><span class="sxs-lookup"><span data-stu-id="85711-105">Tweening is mutually exclusive from vertex blending with weights.</span></span> <span data-ttu-id="85711-106">補間是在光源和裁剪之前執行，並藉由將 D3DRS \_ VERTEXBLEND 設定為 D3DVBF 補間來啟用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="85711-106">Tweening is performed before lighting and clipping, and is enabled by setting D3DRS\_VERTEXBLEND to D3DVBF\_TWEENING.</span></span> <span data-ttu-id="85711-107">產生的頂點位置是由下列各項計算：</span><span class="sxs-lookup"><span data-stu-id="85711-107">The resulting vertex position is computed by:</span></span>


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



<span data-ttu-id="85711-108">使用相同的方法來計演算法線。</span><span class="sxs-lookup"><span data-stu-id="85711-108">The same approach is used for calculating normals.</span></span> <span data-ttu-id="85711-109">如需詳細資訊，請參閱 [使用 (Direct3D 9) 的頂點補間 ](using-vertex-tweening.md)。</span><span class="sxs-lookup"><span data-stu-id="85711-109">For more information, see [Using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85711-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="85711-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85711-111">幾何混合</span><span class="sxs-lookup"><span data-stu-id="85711-111">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



