---
description: 霧化混色指的是 [霧化] 和 [物件色彩] 的 [霧化] 因數，以產生出現在場景中的最終色彩，如 (Direct3D 9) 中的霧化公式所述。
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: " (Direct3D 9) 的霧化混色"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108401"
---
# <a name="fog-blending-direct3d-9"></a><span data-ttu-id="fc8f4-103"> (Direct3D 9) 的霧化混色</span><span class="sxs-lookup"><span data-stu-id="fc8f4-103">Fog Blending (Direct3D 9)</span></span>

<span data-ttu-id="fc8f4-104">霧化混色指的是 [霧化] 和 [物件色彩] 的 [霧化] 因數，以產生出現在場景中的最終色彩，如 [ (Direct3D 9) 中的霧化公式 ](fog-formulas.md)所述。</span><span class="sxs-lookup"><span data-stu-id="fc8f4-104">Fog blending refers to the application of the fog factor to the fog and object colors to produce the final color that appears in a scene, as discussed in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="fc8f4-105">D3DRS \_ FOGENABLE 轉譯狀態控制項霧化混色。</span><span class="sxs-lookup"><span data-stu-id="fc8f4-105">The D3DRS\_FOGENABLE render state controls fog blending.</span></span> <span data-ttu-id="fc8f4-106">將此呈現狀態設為 **TRUE** ，以啟用霧化混合，如下列範例程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="fc8f4-106">Set this render state to **TRUE** to enable fog blending as shown in the following example code.</span></span> <span data-ttu-id="fc8f4-107">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fc8f4-107">The default is **FALSE**.</span></span>


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



<span data-ttu-id="fc8f4-108">您必須啟用圖元霧化和頂點霧化的霧化混合。</span><span class="sxs-lookup"><span data-stu-id="fc8f4-108">You must enable fog blending for both pixel fog and vertex fog.</span></span> <span data-ttu-id="fc8f4-109">如需有關使用這些類型的霧化的詳細資訊，請參閱 [ (direct3d 9 的圖元霧化) ](pixel-fog.md) 和 [ (direct3d 9) 的頂點霧化 ](vertex-fog.md)。</span><span class="sxs-lookup"><span data-stu-id="fc8f4-109">For information about using these types of fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc8f4-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc8f4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc8f4-111">霧化類型</span><span class="sxs-lookup"><span data-stu-id="fc8f4-111">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



