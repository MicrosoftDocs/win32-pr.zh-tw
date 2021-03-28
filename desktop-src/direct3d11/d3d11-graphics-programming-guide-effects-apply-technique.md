---
title: '將技術套用 (Direct3D 11) '
description: 宣告並初始化常數、紋理和著色器狀態之後，唯一要做的事就是在裝置中設定效果狀態。
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e67668b27c1f0271974f20edc62619a7b1ae8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021537"
---
# <a name="apply-a-technique-direct3d-11"></a><span data-ttu-id="ea75b-103">將技術套用 (Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="ea75b-103">Apply a Technique (Direct3D 11)</span></span>

<span data-ttu-id="ea75b-104">宣告並初始化常數、紋理和著色器狀態之後，唯一要做的事就是在裝置中設定效果狀態。</span><span class="sxs-lookup"><span data-stu-id="ea75b-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="ea75b-105">設定裝置中的非著色器狀態</span><span class="sxs-lookup"><span data-stu-id="ea75b-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="ea75b-106">某些管線狀態不是由效果設定。</span><span class="sxs-lookup"><span data-stu-id="ea75b-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="ea75b-107">例如，清除轉譯目標可準備資料的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="ea75b-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="ea75b-108">在裝置上設定效果狀態之前，以下是清除輸出緩衝區的範例。</span><span class="sxs-lookup"><span data-stu-id="ea75b-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="ea75b-109">在裝置中設定效果狀態</span><span class="sxs-lookup"><span data-stu-id="ea75b-109">Set Effect State in the Device</span></span>

<span data-ttu-id="ea75b-110">設定效果狀態是藉由在轉譯迴圈內套用效果狀態來完成。</span><span class="sxs-lookup"><span data-stu-id="ea75b-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="ea75b-111">這是從的外部進行。</span><span class="sxs-lookup"><span data-stu-id="ea75b-111">This is done from the outside in.</span></span> <span data-ttu-id="ea75b-112">也就是說，請選取一項技術，然後根據您想要的結果) ，設定每個通過 (的狀態。</span><span class="sxs-lookup"><span data-stu-id="ea75b-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D11_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



<span data-ttu-id="ea75b-113">效果不會轉譯任何事物，而只會將效果狀態設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="ea75b-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="ea75b-114">轉譯程式碼會在效果狀態更新裝置狀態之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="ea75b-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="ea75b-115">在此範例中，DrawIndexed 呼叫會執行轉譯。</span><span class="sxs-lookup"><span data-stu-id="ea75b-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea75b-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea75b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea75b-117">轉譯 (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="ea75b-117">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




