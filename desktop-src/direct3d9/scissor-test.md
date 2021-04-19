---
description: 剪下測試選出在剪下矩形之外的圖元，也就是呈現目標的使用者定義矩形子區段。
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: " (Direct3D 9) 的剪式測試"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971119"
---
# <a name="scissor-test-direct3d-9"></a><span data-ttu-id="f9aee-103"> (Direct3D 9) 的剪式測試</span><span class="sxs-lookup"><span data-stu-id="f9aee-103">Scissor Test (Direct3D 9)</span></span>

<span data-ttu-id="f9aee-104">剪下測試選出在剪下矩形之外的圖元，也就是呈現目標的使用者定義矩形子區段。</span><span class="sxs-lookup"><span data-stu-id="f9aee-104">The scissor test culls pixels that are outside of the scissor rectangle, a user-defined rectangular sub-section of the render target.</span></span>

<span data-ttu-id="f9aee-105">剪式矩形可用來指出繪製遊戲世界的呈現目的地區域。</span><span class="sxs-lookup"><span data-stu-id="f9aee-105">The scissor rectangle could be used to indicate the area of the render target where the game world is drawn.</span></span> <span data-ttu-id="f9aee-106">矩形外的區域是挑選，而且可能專門用於遊戲的 GUI。</span><span class="sxs-lookup"><span data-stu-id="f9aee-106">The area outside the rectangle is culled and could be devoted to a game's GUI.</span></span> <span data-ttu-id="f9aee-107">剪式測試無法挑選非矩形區域。</span><span class="sxs-lookup"><span data-stu-id="f9aee-107">The scissor test cannot cull non-rectangular areas.</span></span>

<span data-ttu-id="f9aee-108">剪式矩形的設定不能大於轉譯目標，但可以設定為大於視口的範圍。</span><span class="sxs-lookup"><span data-stu-id="f9aee-108">Scissor rectangles cannot be set larger than the render target, but they can be set larger than the viewport.</span></span>

<span data-ttu-id="f9aee-109">剪式矩形是由裝置呈現狀態所管理。</span><span class="sxs-lookup"><span data-stu-id="f9aee-109">The scissor rectangle is managed by a device render state.</span></span> <span data-ttu-id="f9aee-110">將 renderstate 設為 **TRUE** 或 **FALSE**，以啟用或停用剪下測試。</span><span class="sxs-lookup"><span data-stu-id="f9aee-110">A scissor test is enabled or disabled by setting the renderstate to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="f9aee-111">這項測試是在計算片段色彩之後，但在 Alpha 測試之前執行。</span><span class="sxs-lookup"><span data-stu-id="f9aee-111">This test is performed after the fragment color is computed but before alpha testing.</span></span> <span data-ttu-id="f9aee-112">[**IDirect3DDevice9：： SetRenderTarget**](/windows/desktop/api) 會將剪式矩形重設為完整轉譯目標，類似于重設區域。</span><span class="sxs-lookup"><span data-stu-id="f9aee-112">[**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) resets the scissor rectangle to the full render target, analogous to the viewport reset.</span></span> <span data-ttu-id="f9aee-113">[**IDirect3DDevice9：： SetScissorRect**](/windows/desktop/api) 是由 stateblocks 所記錄，而 [**IDirect3DDevice9：： CreateStateBlock**](/windows/desktop/api) 具有 [全部狀態] 設定 (D3DSBT \_) [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md) 中的所有值。</span><span class="sxs-lookup"><span data-stu-id="f9aee-113">[**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) is recorded by stateblocks, and [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) with the all state setting (D3DSBT\_ALL value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span></span> <span data-ttu-id="f9aee-114">剪式測試也會影響裝置 [**IDirect3DDevice9：： Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) 操作。</span><span class="sxs-lookup"><span data-stu-id="f9aee-114">The scissor test also affects the device [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) operation.</span></span>


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



<span data-ttu-id="f9aee-115">預設的剪式矩形是完整的視口。</span><span class="sxs-lookup"><span data-stu-id="f9aee-115">The default scissor rectangle is the full viewport.</span></span>

<span data-ttu-id="f9aee-116">在圖元著色器或固定函式管線完成圖元處理之後，剪下測試就會完成，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f9aee-116">Scissor testing is done just after pixel processing is completed by a pixel shader or the fixed function pipeline, as shown in the following diagram.</span></span>

![相對於其他步驟執行剪式測試的圖表](images/scissor-test.png)

## <a name="related-topics"></a><span data-ttu-id="f9aee-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9aee-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9aee-119">圖元管線</span><span class="sxs-lookup"><span data-stu-id="f9aee-119">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
