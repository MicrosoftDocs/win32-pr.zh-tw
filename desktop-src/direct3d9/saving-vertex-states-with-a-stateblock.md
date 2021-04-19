---
description: 狀態欄塊只能用來捕捉頂點狀態 (請參閱 (Direct3D 9) ) 的狀態欄塊儲存和還原狀態。
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: 以 StateBlock (Direct3D 9) 儲存頂點狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970901"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="6c237-103">以 StateBlock (Direct3D 9) 儲存頂點狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-103">Saving Vertex States With a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="6c237-104">狀態欄塊只能用來捕捉頂點狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c237-104">A state block can be used to capture only vertex state (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="6c237-105">下列狀態為頂點狀態：</span><span class="sxs-lookup"><span data-stu-id="6c237-105">The following state is vertex state:</span></span>

-   <span data-ttu-id="6c237-106">頂點呈現狀態 (請參閱 [頂點管線：轉譯狀態](#vertex-pipeline-render-state)) 。</span><span class="sxs-lookup"><span data-stu-id="6c237-106">Vertex render state (see [Vertex Pipeline: Render State](#vertex-pipeline-render-state)).</span></span>
-   <span data-ttu-id="6c237-107">頂點取樣器狀態 (請參閱 [頂點管線：取樣器狀態](#vertex-pipeline-sampler-state)) 。</span><span class="sxs-lookup"><span data-stu-id="6c237-107">Vertex sampler state (see [Vertex Pipeline: Sampler State](#vertex-pipeline-sampler-state)).</span></span>
-   <span data-ttu-id="6c237-108">頂點材質狀態 (請參閱 [頂點管線：材質狀態](#vertex-pipeline-texture-state)) 。</span><span class="sxs-lookup"><span data-stu-id="6c237-108">Vertex texture state (see [Vertex Pipeline: Texture State](#vertex-pipeline-texture-state)).</span></span>
-   <span data-ttu-id="6c237-109">來自 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)的 NPatch 模式區段。</span><span class="sxs-lookup"><span data-stu-id="6c237-109">The NPatch mode segments from [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>
-   <span data-ttu-id="6c237-110">[**IDirect3DDevice9：： SetLight**](/windows/desktop/api)的每個光線，以及是否使用 [**IDirect3DDevice9：： LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)來啟用光線。</span><span class="sxs-lookup"><span data-stu-id="6c237-110">Each light from [**IDirect3DDevice9::SetLight**](/windows/desktop/api), as well as whether or not the light is enabled with [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>
-   <span data-ttu-id="6c237-111">目前的頂點著色器和每個頂點著色器常數。</span><span class="sxs-lookup"><span data-stu-id="6c237-111">The current vertex shader and each of the vertex shader constants.</span></span>
-   <span data-ttu-id="6c237-112">針對每個頂點資料流程，儲存 [**IDirect3DDevice9：： SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq)的分隔值。</span><span class="sxs-lookup"><span data-stu-id="6c237-112">For each vertex stream, store the divider value from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="6c237-113">目前的頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="6c237-113">The current vertex declaration.</span></span>

<span data-ttu-id="6c237-114">若要使用狀態欄塊來捕捉頂點狀態，請 \_ 在呼叫 [**IDirect3DDevice9：： CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)時，指定 D3DSBT VERTEXSTATE。</span><span class="sxs-lookup"><span data-stu-id="6c237-114">To capture vertex state with a state block, specify D3DSBT\_VERTEXSTATE when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="vertex-pipeline-render-state"></a><span data-ttu-id="6c237-115">頂點管線：轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-115">Vertex Pipeline: Render State</span></span>

<span data-ttu-id="6c237-116">裝置轉譯狀態會影響管線幾乎所有元件的行為。</span><span class="sxs-lookup"><span data-stu-id="6c237-116">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="6c237-117">藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)來設定轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="6c237-117">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="6c237-118">下表包含設定頂點狀態的所有呈現狀態：</span><span class="sxs-lookup"><span data-stu-id="6c237-118">The following table includes all render states that set-up vertex state:</span></span>



| <span data-ttu-id="6c237-119">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-119">Render States</span></span>                           | <span data-ttu-id="6c237-120">預設值</span><span class="sxs-lookup"><span data-stu-id="6c237-120">Default Value</span></span>          |
|-----------------------------------------|------------------------|
| <span data-ttu-id="6c237-121">D3DRS \_ CULLMODE</span><span class="sxs-lookup"><span data-stu-id="6c237-121">D3DRS\_CULLMODE</span></span>                         | <span data-ttu-id="6c237-122">D3DCULL \_ CCW</span><span class="sxs-lookup"><span data-stu-id="6c237-122">D3DCULL\_CCW</span></span>           |
| <span data-ttu-id="6c237-123">D3DRS \_ FOGCOLOR</span><span class="sxs-lookup"><span data-stu-id="6c237-123">D3DRS\_FOGCOLOR</span></span>                         | <span data-ttu-id="6c237-124">0</span><span class="sxs-lookup"><span data-stu-id="6c237-124">0</span></span>                      |
| <span data-ttu-id="6c237-125">D3DRS \_ FOGTABLEMODE</span><span class="sxs-lookup"><span data-stu-id="6c237-125">D3DRS\_FOGTABLEMODE</span></span>                     | <span data-ttu-id="6c237-126">D3DFOG \_ 無</span><span class="sxs-lookup"><span data-stu-id="6c237-126">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="6c237-127">D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="6c237-127">D3DRS\_FOGSTART</span></span>                         | <span data-ttu-id="6c237-128">0</span><span class="sxs-lookup"><span data-stu-id="6c237-128">0</span></span>                      |
| <span data-ttu-id="6c237-129">D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="6c237-129">D3DRS\_FOGEND</span></span>                           | <span data-ttu-id="6c237-130">1</span><span class="sxs-lookup"><span data-stu-id="6c237-130">1</span></span>                      |
| <span data-ttu-id="6c237-131">D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="6c237-131">D3DRS\_FOGDENSITY</span></span>                       | <span data-ttu-id="6c237-132">1</span><span class="sxs-lookup"><span data-stu-id="6c237-132">1</span></span>                      |
| <span data-ttu-id="6c237-133">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="6c237-133">D3DRS\_RANGEFOGENABLE</span></span>                   | <span data-ttu-id="6c237-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6c237-134">**FALSE**</span></span>              |
| <span data-ttu-id="6c237-135">D3DRS \_ 環境</span><span class="sxs-lookup"><span data-stu-id="6c237-135">D3DRS\_AMBIENT</span></span>                          | <span data-ttu-id="6c237-136">0</span><span class="sxs-lookup"><span data-stu-id="6c237-136">0</span></span>                      |
| <span data-ttu-id="6c237-137">D3DRS \_ COLORVERTEX</span><span class="sxs-lookup"><span data-stu-id="6c237-137">D3DRS\_COLORVERTEX</span></span>                      | <span data-ttu-id="6c237-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6c237-138">**TRUE**</span></span>               |
| <span data-ttu-id="6c237-139">D3DRS \_ FOGVERTEXMODE</span><span class="sxs-lookup"><span data-stu-id="6c237-139">D3DRS\_FOGVERTEXMODE</span></span>                    | <span data-ttu-id="6c237-140">D3DFOG \_ 無</span><span class="sxs-lookup"><span data-stu-id="6c237-140">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="6c237-141">D3DRS \_ 剪切</span><span class="sxs-lookup"><span data-stu-id="6c237-141">D3DRS\_CLIPPING</span></span>                         | <span data-ttu-id="6c237-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6c237-142">**TRUE**</span></span>               |
| <span data-ttu-id="6c237-143">D3DRS \_ 光源</span><span class="sxs-lookup"><span data-stu-id="6c237-143">D3DRS\_LIGHTING</span></span>                         | <span data-ttu-id="6c237-144">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6c237-144">**TRUE**</span></span>               |
| <span data-ttu-id="6c237-145">D3DRS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="6c237-145">D3DRS\_LOCALVIEWER</span></span>                      | <span data-ttu-id="6c237-146">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6c237-146">**TRUE**</span></span>               |
| <span data-ttu-id="6c237-147">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="6c237-147">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>           | <span data-ttu-id="6c237-148">D3DMCS \_ 材質</span><span class="sxs-lookup"><span data-stu-id="6c237-148">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="6c237-149">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="6c237-149">D3DRS\_AMBIENTMATERIALSOURCE</span></span>            | <span data-ttu-id="6c237-150">D3DMCS \_ 材質</span><span class="sxs-lookup"><span data-stu-id="6c237-150">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="6c237-151">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="6c237-151">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>            | <span data-ttu-id="6c237-152">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="6c237-152">D3DMCS\_COLOR1</span></span>         |
| <span data-ttu-id="6c237-153">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="6c237-153">D3DRS\_SPECULARMATERIALSOURCE</span></span>           | <span data-ttu-id="6c237-154">D3DMCS \_ COLOR2</span><span class="sxs-lookup"><span data-stu-id="6c237-154">D3DMCS\_COLOR2</span></span>         |
| <span data-ttu-id="6c237-155">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="6c237-155">D3DRS\_VERTEXBLEND</span></span>                      | <span data-ttu-id="6c237-156">D3DVBF \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="6c237-156">D3DVBF\_DISABLE</span></span>        |
| <span data-ttu-id="6c237-157">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="6c237-157">D3DRS\_CLIPPLANEENABLE</span></span>                  | <span data-ttu-id="6c237-158">0</span><span class="sxs-lookup"><span data-stu-id="6c237-158">0</span></span>                      |
| <span data-ttu-id="6c237-159">D3DRS \_ dialog</span><span class="sxs-lookup"><span data-stu-id="6c237-159">D3DRS\_POINTSIZE</span></span>                        | <span data-ttu-id="6c237-160">驅動程式相依</span><span class="sxs-lookup"><span data-stu-id="6c237-160">Driver dependent</span></span>       |
| <span data-ttu-id="6c237-161">D3DRS \_ dialog \_ MIN</span><span class="sxs-lookup"><span data-stu-id="6c237-161">D3DRS\_POINTSIZE\_MIN</span></span>                   | <span data-ttu-id="6c237-162">1</span><span class="sxs-lookup"><span data-stu-id="6c237-162">1</span></span>                      |
| <span data-ttu-id="6c237-163">D3DRS \_ POINTSPRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="6c237-163">D3DRS\_POINTSPRITEENABLE</span></span>                | <span data-ttu-id="6c237-164">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6c237-164">**FALSE**</span></span>              |
| <span data-ttu-id="6c237-165">D3DRS \_ POINTSCALEENABLE</span><span class="sxs-lookup"><span data-stu-id="6c237-165">D3DRS\_POINTSCALEENABLE</span></span>                 | <span data-ttu-id="6c237-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6c237-166">**FALSE**</span></span>              |
| <span data-ttu-id="6c237-167">D3DRS \_ POINTSCALE \_</span><span class="sxs-lookup"><span data-stu-id="6c237-167">D3DRS\_POINTSCALE\_A</span></span>                    | <span data-ttu-id="6c237-168">1</span><span class="sxs-lookup"><span data-stu-id="6c237-168">1</span></span>                      |
| <span data-ttu-id="6c237-169">D3DRS \_ POINTSCALE \_ B</span><span class="sxs-lookup"><span data-stu-id="6c237-169">D3DRS\_POINTSCALE\_B</span></span>                    | <span data-ttu-id="6c237-170">0</span><span class="sxs-lookup"><span data-stu-id="6c237-170">0</span></span>                      |
| <span data-ttu-id="6c237-171">D3DRS \_ POINTSCALE \_ C</span><span class="sxs-lookup"><span data-stu-id="6c237-171">D3DRS\_POINTSCALE\_C</span></span>                    | <span data-ttu-id="6c237-172">0</span><span class="sxs-lookup"><span data-stu-id="6c237-172">0</span></span>                      |
| <span data-ttu-id="6c237-173">D3DRS \_ MULTISAMPLEANTIALIAS</span><span class="sxs-lookup"><span data-stu-id="6c237-173">D3DRS\_MULTISAMPLEANTIALIAS</span></span>             | <span data-ttu-id="6c237-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6c237-174">**TRUE**</span></span>               |
| <span data-ttu-id="6c237-175">D3DRS \_ MULTISAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="6c237-175">D3DRS\_MULTISAMPLEMASK</span></span>                  | <span data-ttu-id="6c237-176">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="6c237-176">0xffffffff</span></span>             |
| <span data-ttu-id="6c237-177">D3DRS \_ PATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="6c237-177">D3DRS\_PATCHEDGESTYLE</span></span>                   | <span data-ttu-id="6c237-178">D3DPATCHEDGE \_ 離散</span><span class="sxs-lookup"><span data-stu-id="6c237-178">D3DPATCHEDGE\_DISCRETE</span></span> |
| <span data-ttu-id="6c237-179">D3DRS \_ dialog \_ MAX</span><span class="sxs-lookup"><span data-stu-id="6c237-179">D3DRS\_POINTSIZE\_MAX</span></span>                   | <span data-ttu-id="6c237-180">1</span><span class="sxs-lookup"><span data-stu-id="6c237-180">1</span></span>                      |
| <span data-ttu-id="6c237-181">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="6c237-181">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>         | <span data-ttu-id="6c237-182">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6c237-182">**FALSE**</span></span>              |
| <span data-ttu-id="6c237-183">D3DRS \_ TWEENFACTOR</span><span class="sxs-lookup"><span data-stu-id="6c237-183">D3DRS\_TWEENFACTOR</span></span>                      | <span data-ttu-id="6c237-184">0</span><span class="sxs-lookup"><span data-stu-id="6c237-184">0</span></span>                      |
| <span data-ttu-id="6c237-185">D3DRS \_ POSITIONDEGREE</span><span class="sxs-lookup"><span data-stu-id="6c237-185">D3DRS\_POSITIONDEGREE</span></span>                   | <span data-ttu-id="6c237-186">D3DDEGREE \_ 立方</span><span class="sxs-lookup"><span data-stu-id="6c237-186">D3DDEGREE\_CUBIC</span></span>       |
| <span data-ttu-id="6c237-187">D3DRS \_ NORMALDEGREE</span><span class="sxs-lookup"><span data-stu-id="6c237-187">D3DRS\_NORMALDEGREE</span></span>                     | <span data-ttu-id="6c237-188">D3DDEGREE \_ 線性</span><span class="sxs-lookup"><span data-stu-id="6c237-188">D3DDEGREE\_LINEAR</span></span>      |
| <span data-ttu-id="6c237-189">D3DRS \_ MINTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="6c237-189">D3DRS\_MINTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="6c237-190">1</span><span class="sxs-lookup"><span data-stu-id="6c237-190">1</span></span>                      |
| <span data-ttu-id="6c237-191">D3DRS \_ MAXTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="6c237-191">D3DRS\_MAXTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="6c237-192">1</span><span class="sxs-lookup"><span data-stu-id="6c237-192">1</span></span>                      |
| <span data-ttu-id="6c237-193">D3DRS \_ ADAPTIVETESS \_ X</span><span class="sxs-lookup"><span data-stu-id="6c237-193">D3DRS\_ADAPTIVETESS\_X</span></span>                  | <span data-ttu-id="6c237-194">0</span><span class="sxs-lookup"><span data-stu-id="6c237-194">0</span></span>                      |
| <span data-ttu-id="6c237-195">D3DRS \_ ADAPTIVETESS \_ Y</span><span class="sxs-lookup"><span data-stu-id="6c237-195">D3DRS\_ADAPTIVETESS\_Y</span></span>                  | <span data-ttu-id="6c237-196">0</span><span class="sxs-lookup"><span data-stu-id="6c237-196">0</span></span>                      |
| <span data-ttu-id="6c237-197">D3DRS \_ ADAPTIVETESS \_ Z</span><span class="sxs-lookup"><span data-stu-id="6c237-197">D3DRS\_ADAPTIVETESS\_Z</span></span>                  | <span data-ttu-id="6c237-198">1</span><span class="sxs-lookup"><span data-stu-id="6c237-198">1</span></span>                      |
| <span data-ttu-id="6c237-199">D3DRS \_ ADAPTIVETESS \_ W</span><span class="sxs-lookup"><span data-stu-id="6c237-199">D3DRS\_ADAPTIVETESS\_W</span></span>                  | <span data-ttu-id="6c237-200">0</span><span class="sxs-lookup"><span data-stu-id="6c237-200">0</span></span>                      |
| <span data-ttu-id="6c237-201">D3DRS \_ ENABLEADAPTIVETESSELLATION "/></span><span class="sxs-lookup"><span data-stu-id="6c237-201">D3DRS\_ENABLEADAPTIVETESSELLATION"/></span></span> | <span data-ttu-id="6c237-202">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6c237-202">**FALSE**</span></span>              |



 

## <a name="vertex-pipeline-sampler-state"></a><span data-ttu-id="6c237-203">頂點管線：取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-203">Vertex Pipeline: Sampler State</span></span>

<span data-ttu-id="6c237-204">取樣器狀態會控制取樣的相關主題，例如篩選、平平貼圖和材質座標位址模式。</span><span class="sxs-lookup"><span data-stu-id="6c237-204">Sampler states control sampling related topics such as filtering, tiling, and texture coordinate address modes.</span></span> <span data-ttu-id="6c237-205">使用 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 來設定取樣器狀態 (包括鑲嵌單位中用來取樣置換地圖) 的狀態。</span><span class="sxs-lookup"><span data-stu-id="6c237-205">Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) to set up the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="6c237-206">取樣器狀態已重新命名為 "D3DSAMP \_ " 前置詞，以在從 DirectX 8 移植時啟用編譯時期錯誤偵測。</span><span class="sxs-lookup"><span data-stu-id="6c237-206">The sampler states have been renamed with a "D3DSAMP\_" prefix to enable compile time error detection when porting from DirectX 8.</span></span>

<span data-ttu-id="6c237-207">下表包含所有設定頂點狀態的取樣器狀態：</span><span class="sxs-lookup"><span data-stu-id="6c237-207">The following table includes all sampler states that set-up vertex state:</span></span>



| <span data-ttu-id="6c237-208">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-208">Sampler States</span></span>      | <span data-ttu-id="6c237-209">預設值</span><span class="sxs-lookup"><span data-stu-id="6c237-209">Default Value</span></span> |
|---------------------|---------------|
| <span data-ttu-id="6c237-210">D3DSAMP \_ DMAPOFFSET</span><span class="sxs-lookup"><span data-stu-id="6c237-210">D3DSAMP\_DMAPOFFSET</span></span> | <span data-ttu-id="6c237-211">256</span><span class="sxs-lookup"><span data-stu-id="6c237-211">256</span></span>           |



 

## <a name="vertex-pipeline-texture-state"></a><span data-ttu-id="6c237-212">頂點管線：材質狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-212">Vertex Pipeline: Texture State</span></span>

<span data-ttu-id="6c237-213">材質狀態控制多紋理 blender 的材質混合作業。</span><span class="sxs-lookup"><span data-stu-id="6c237-213">Texture states control texture blending operations of the multi-texture blender.</span></span> <span data-ttu-id="6c237-214">使用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api) 來設定材質狀態。</span><span class="sxs-lookup"><span data-stu-id="6c237-214">Use [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) to set-up texture states.</span></span> <span data-ttu-id="6c237-215">使用 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 將材質與取樣器階段產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6c237-215">Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to associate a texture with a sampler stage.</span></span>

<span data-ttu-id="6c237-216">下表包含所有設定頂點狀態的材質狀態：</span><span class="sxs-lookup"><span data-stu-id="6c237-216">The following table includes all the texture states that set-up vertex state:</span></span>



| <span data-ttu-id="6c237-217">材質狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-217">Texture States</span></span>                | <span data-ttu-id="6c237-218">預設值</span><span class="sxs-lookup"><span data-stu-id="6c237-218">Default Value</span></span>    |
|-------------------------------|------------------|
| <span data-ttu-id="6c237-219">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="6c237-219">D3DTSS\_TEXCOORDINDEX</span></span>         | <span data-ttu-id="6c237-220">0</span><span class="sxs-lookup"><span data-stu-id="6c237-220">0</span></span>                |
| <span data-ttu-id="6c237-221">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="6c237-221">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span> | <span data-ttu-id="6c237-222">D3DTTFF \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="6c237-222">D3DTTFF\_DISABLE</span></span> |



 

<span data-ttu-id="6c237-223">D3DTSS \_ TEXCOORDINDEX 是固定的函式頂點處理狀態。</span><span class="sxs-lookup"><span data-stu-id="6c237-223">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="6c237-224">如果使用可程式化的頂點著色器，則會忽略此狀態。</span><span class="sxs-lookup"><span data-stu-id="6c237-224">If a programmable vertex shader is used, this state is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c237-225">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c237-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c237-226">狀態欄塊儲存與還原狀態</span><span class="sxs-lookup"><span data-stu-id="6c237-226">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
