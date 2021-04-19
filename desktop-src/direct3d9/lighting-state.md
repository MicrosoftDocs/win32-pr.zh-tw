---
description: 如果您不亮著頂點著色器或圖元著色器，則可以選擇在執行時間中使用光源引擎。
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: " (Direct3D 9) 的燈光狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971921"
---
# <a name="lighting-state-direct3d-9"></a><span data-ttu-id="dbbc6-103"> (Direct3D 9) 的燈光狀態</span><span class="sxs-lookup"><span data-stu-id="dbbc6-103">Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="dbbc6-104">如果您不亮著頂點著色器或圖元著色器，則可以選擇在執行時間中使用光源引擎。</span><span class="sxs-lookup"><span data-stu-id="dbbc6-104">If you do not light with a vertex shader or a pixel shader, you may choose to use the lighting engine in the runtime.</span></span> <span data-ttu-id="dbbc6-105">光源引擎要求頂點資料必須包含每個頂點的法線：沒有一般資料的頂點會在所有光源計算中產生一個零的點乘積。</span><span class="sxs-lookup"><span data-stu-id="dbbc6-105">The lighting engine requires that the vertex data contains per-vertex normals; vertices without normal data will generate a dot product of zero in all lighting computations.</span></span> <span data-ttu-id="dbbc6-106">光源計算在 [ (Direct3D 9) 的數學數學 ](mathematics-of-lighting.md)中有更詳細的討論。</span><span class="sxs-lookup"><span data-stu-id="dbbc6-106">The lighting calculations are covered in more detail in [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="dbbc6-107">若要啟用光源引擎，請使用：</span><span class="sxs-lookup"><span data-stu-id="dbbc6-107">To enable the lighting engine, use:</span></span>


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a><span data-ttu-id="dbbc6-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="dbbc6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbbc6-109">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="dbbc6-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



