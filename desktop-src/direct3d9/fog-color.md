---
description: 圖元和頂點霧化的霧化色彩是透過 D3DRS FOGCOLOR 轉譯狀態來設定 \_ 。 轉譯狀態值可以是任何 RGB 色彩，以指定為 RGBA 色彩。 Alpha 元件會被忽略。
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: " (Direct3D 9) 的霧化色彩"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025601"
---
# <a name="fog-color-direct3d-9"></a><span data-ttu-id="15d22-105"> (Direct3D 9) 的霧化色彩</span><span class="sxs-lookup"><span data-stu-id="15d22-105">Fog Color (Direct3D 9)</span></span>

<span data-ttu-id="15d22-106">圖元和頂點霧化的霧化色彩是透過 D3DRS FOGCOLOR 轉譯狀態來設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="15d22-106">Fog color for both pixel and vertex fog is set through the D3DRS\_FOGCOLOR render state.</span></span> <span data-ttu-id="15d22-107">轉譯狀態值可以是任何 RGB 色彩，以指定為 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="15d22-107">The render state values can be any RGB color, specified as an RGBA color.</span></span> <span data-ttu-id="15d22-108">Alpha 元件會被忽略。</span><span class="sxs-lookup"><span data-stu-id="15d22-108">The alpha component is ignored.</span></span>

<span data-ttu-id="15d22-109">下列 c + + 範例會將霧化色彩設定為白色。</span><span class="sxs-lookup"><span data-stu-id="15d22-109">The following C++ example sets the fog color to white.</span></span>


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



<span data-ttu-id="15d22-110">固定函式管線和可程式化管線會以不同的方式套用霧化。</span><span class="sxs-lookup"><span data-stu-id="15d22-110">Fog is applied differently by the fixed function pipeline and the programmable pipeline.</span></span>

1.  <span data-ttu-id="15d22-111">如果驅動程式支援 D3DPMISCCAPS \_ FOGANDSPECULARALPHA：</span><span class="sxs-lookup"><span data-stu-id="15d22-111">If the driver supports D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="15d22-112">如果使用固定函式管線，且 \_ 已設定 D3DRS FOGCOLOR，則圖元著色器中的 v1. w () 等於在霧化 renderstate 中設定的值。</span><span class="sxs-lookup"><span data-stu-id="15d22-112">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, v1.w (in the pixel shader) equals the value set in fog renderstate.</span></span>
    -   <span data-ttu-id="15d22-113">如果使用可程式化管線，則在圖元著色器中 (v1. w) 等於0，即使 oD1 是在頂點著色器中明確寫入。</span><span class="sxs-lookup"><span data-stu-id="15d22-113">If the programmable pipeline is used, then v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>
2.  <span data-ttu-id="15d22-114">如果驅動程式不支援 D3DPMISCCAPS \_ FOGANDSPECULARALPHA：</span><span class="sxs-lookup"><span data-stu-id="15d22-114">If the driver does NOT support D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="15d22-115">如果使用固定函式管線，並 \_ 設定 D3DRS FOGCOLOR，則圖元著色器中的 v1. w () 等於在霧化 renderstate 中設定的值。</span><span class="sxs-lookup"><span data-stu-id="15d22-115">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, then v1.w (in the pixel shader) equals value set in fog renderstate.</span></span>
    -   <span data-ttu-id="15d22-116">如果 oFog 是在頂點著色器中明確寫入，則在圖元著色器中為 v1. w () 等於 oFog，壓制介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="15d22-116">If oFog is explicitly written in a vertex shader, v1.w (in the pixel shader) equals oFog, clamped between 0 and 1.</span></span>
    -   <span data-ttu-id="15d22-117">如果上述兩個案例都不適用，則在圖元著色器中的 v1. w () 等於0，即使 oD1 是在頂點著色器中明確寫入。</span><span class="sxs-lookup"><span data-stu-id="15d22-117">If neither of the above two cases applies, v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>

<span data-ttu-id="15d22-118">如需詳細資訊，請參閱 [D3DPMISCCAPS](d3dpmisccaps.md)。</span><span class="sxs-lookup"><span data-stu-id="15d22-118">For more information, see [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="15d22-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="15d22-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15d22-120">霧化類型</span><span class="sxs-lookup"><span data-stu-id="15d22-120">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



