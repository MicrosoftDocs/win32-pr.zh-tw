---
description: 準備裝置以繪製 sprite。
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite：： Begin 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992328"
---
# <a name="id3dxspritebegin-method"></a><span data-ttu-id="c7d68-103">ID3DXSprite：： Begin 方法</span><span class="sxs-lookup"><span data-stu-id="c7d68-103">ID3DXSprite::Begin method</span></span>

<span data-ttu-id="c7d68-104">準備裝置以繪製 sprite。</span><span class="sxs-lookup"><span data-stu-id="c7d68-104">Prepares a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d68-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7d68-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="c7d68-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7d68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d68-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c7d68-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d68-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7d68-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7d68-109">描述 sprite 轉譯選項的零或多個旗標組合。</span><span class="sxs-lookup"><span data-stu-id="c7d68-109">Combination of zero or more flags that describe sprite rendering options.</span></span> <span data-ttu-id="c7d68-110">針對此方法，有效的旗標為：</span><span class="sxs-lookup"><span data-stu-id="c7d68-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="c7d68-111">D3DXSPRITE \_ ALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="c7d68-111">D3DXSPRITE\_ALPHABLEND</span></span>
-   <span data-ttu-id="c7d68-112">D3DXSPRITE \_ \_ 佈告欄</span><span class="sxs-lookup"><span data-stu-id="c7d68-112">D3DXSPRITE\_\_BILLBOARD</span></span>
-   <span data-ttu-id="c7d68-113">D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE</span><span class="sxs-lookup"><span data-stu-id="c7d68-113">D3DXSPRITE\_DONOTMODIFY\_RENDERSTATE</span></span>
-   <span data-ttu-id="c7d68-114">D3DXSPRITE \_ DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="c7d68-114">D3DXSPRITE\_DONOTSAVESTATE</span></span>
-   <span data-ttu-id="c7d68-115">D3DXSPRITE \_ OBJECTSPACE</span><span class="sxs-lookup"><span data-stu-id="c7d68-115">D3DXSPRITE\_OBJECTSPACE</span></span>
-   <span data-ttu-id="c7d68-116">D3DXSPRITE \_ \_ 排序 \_ 深度 \_ BACKTOFRONT</span><span class="sxs-lookup"><span data-stu-id="c7d68-116">D3DXSPRITE\_\_SORT\_DEPTH\_BACKTOFRONT</span></span>
-   <span data-ttu-id="c7d68-117">D3DXSPRITE \_ \_ 排序 \_ 深度 \_ FRONTTOBACK</span><span class="sxs-lookup"><span data-stu-id="c7d68-117">D3DXSPRITE\_\_SORT\_DEPTH\_FRONTTOBACK</span></span>
-   <span data-ttu-id="c7d68-118">D3DXSPRITE \_ \_ 排序 \_ 材質</span><span class="sxs-lookup"><span data-stu-id="c7d68-118">D3DXSPRITE\_\_SORT\_TEXTURE</span></span>

<span data-ttu-id="c7d68-119">如需旗標的描述，以及如何控制裝置狀態捕捉和裝置視圖轉換的詳細資訊，請參閱 [D3DXSPRITE](d3dxsprite.md)。</span><span class="sxs-lookup"><span data-stu-id="c7d68-119">For a description of the flags and for information on how to control device state capture and device view transforms, see [D3DXSPRITE](d3dxsprite.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d68-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7d68-120">Return value</span></span>

<span data-ttu-id="c7d68-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7d68-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7d68-122">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c7d68-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c7d68-123">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c7d68-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7d68-124">備註</span><span class="sxs-lookup"><span data-stu-id="c7d68-124">Remarks</span></span>

<span data-ttu-id="c7d68-125">您必須從 [**IDirect3DDevice9：： BeginScene**](/windows/desktop/api) 內部呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c7d68-125">This method must be called from inside a [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) .</span></span> <span data-ttu-id="c7d68-126">.</span><span class="sxs-lookup"><span data-stu-id="c7d68-126">.</span></span> <span data-ttu-id="c7d68-127">.</span><span class="sxs-lookup"><span data-stu-id="c7d68-127">.</span></span> <span data-ttu-id="c7d68-128">[**IDirect3DDevice9：： EndScene**](/windows/desktop/api) sequence。</span><span class="sxs-lookup"><span data-stu-id="c7d68-128">[**IDirect3DDevice9::EndScene**](/windows/desktop/api) sequence.</span></span> <span data-ttu-id="c7d68-129">**ID3DXSprite：： Begin** 不能用來取代 **IDirect3DDevice9：： BeginScene** 或 [**ID3DXRenderToSurface：： BeginScene**](id3dxrendertosurface--beginscene.md)。</span><span class="sxs-lookup"><span data-stu-id="c7d68-129">**ID3DXSprite::Begin** cannot be used as a substitute for either **IDirect3DDevice9::BeginScene** or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

<span data-ttu-id="c7d68-130">此方法會在裝置上設定下列狀態。</span><span class="sxs-lookup"><span data-stu-id="c7d68-130">This method will set the following states on the device.</span></span>

<span data-ttu-id="c7d68-131">轉譯狀態：</span><span class="sxs-lookup"><span data-stu-id="c7d68-131">Render States:</span></span>



| <span data-ttu-id="c7d68-132">輸入 ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) </span><span class="sxs-lookup"><span data-stu-id="c7d68-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span></span> | <span data-ttu-id="c7d68-133">值</span><span class="sxs-lookup"><span data-stu-id="c7d68-133">Value</span></span>                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d68-134">D3DRS \_ ALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-134">D3DRS\_ALPHABLENDENABLE</span></span>                                       | <span data-ttu-id="c7d68-135">true</span><span class="sxs-lookup"><span data-stu-id="c7d68-135">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="c7d68-136">D3DRS \_ ALPHAFUNC</span><span class="sxs-lookup"><span data-stu-id="c7d68-136">D3DRS\_ALPHAFUNC</span></span>                                              | <span data-ttu-id="c7d68-137">D3DCMP \_ 更大</span><span class="sxs-lookup"><span data-stu-id="c7d68-137">D3DCMP\_GREATER</span></span>                                                                                                   |
| <span data-ttu-id="c7d68-138">D3DRS \_ ALPHAREF</span><span class="sxs-lookup"><span data-stu-id="c7d68-138">D3DRS\_ALPHAREF</span></span>                                               | <span data-ttu-id="c7d68-139">0x00</span><span class="sxs-lookup"><span data-stu-id="c7d68-139">0x00</span></span>                                                                                                              |
| <span data-ttu-id="c7d68-140">D3DRS \_ ALPHATESTENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-140">D3DRS\_ALPHATESTENABLE</span></span>                                        | <span data-ttu-id="c7d68-141">AlphaCmpCaps</span><span class="sxs-lookup"><span data-stu-id="c7d68-141">AlphaCmpCaps</span></span>                                                                                                      |
| <span data-ttu-id="c7d68-142">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="c7d68-142">D3DRS\_BLENDOP</span></span>                                                | <span data-ttu-id="c7d68-143">D3DBLENDOP \_ 新增</span><span class="sxs-lookup"><span data-stu-id="c7d68-143">D3DBLENDOP\_ADD</span></span>                                                                                                   |
| <span data-ttu-id="c7d68-144">D3DRS \_ 剪切</span><span class="sxs-lookup"><span data-stu-id="c7d68-144">D3DRS\_CLIPPING</span></span>                                               | <span data-ttu-id="c7d68-145">true</span><span class="sxs-lookup"><span data-stu-id="c7d68-145">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="c7d68-146">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-146">D3DRS\_CLIPPLANEENABLE</span></span>                                        | <span data-ttu-id="c7d68-147">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-147">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-148">D3DRS \_ COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-148">D3DRS\_COLORWRITEENABLE</span></span>                                       | <span data-ttu-id="c7d68-149">D3DCOLORWRITEENABLE \_ ALPHA \| D3DCOLORWRITEENABLE \_ BLUE \| D3DCOLORWRITEENABLE \_ 綠 \| D3DCOLORWRITEENABLE \_ RED</span><span class="sxs-lookup"><span data-stu-id="c7d68-149">D3DCOLORWRITEENABLE\_ALPHA \| D3DCOLORWRITEENABLE\_BLUE \| D3DCOLORWRITEENABLE\_GREEN \| D3DCOLORWRITEENABLE\_RED</span></span> |
| <span data-ttu-id="c7d68-150">D3DRS \_ CULLMODE</span><span class="sxs-lookup"><span data-stu-id="c7d68-150">D3DRS\_CULLMODE</span></span>                                               | <span data-ttu-id="c7d68-151">D3DCULL \_ 無</span><span class="sxs-lookup"><span data-stu-id="c7d68-151">D3DCULL\_NONE</span></span>                                                                                                     |
| <span data-ttu-id="c7d68-152">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="c7d68-152">D3DRS\_DESTBLEND</span></span>                                              | <span data-ttu-id="c7d68-153">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="c7d68-153">D3DBLEND\_INVSRCALPHA</span></span>                                                                                             |
| <span data-ttu-id="c7d68-154">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="c7d68-154">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>                                  | <span data-ttu-id="c7d68-155">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="c7d68-155">D3DMCS\_COLOR1</span></span>                                                                                                    |
| <span data-ttu-id="c7d68-156">D3DRS \_ ENABLEADAPTIVETESSELLATION</span><span class="sxs-lookup"><span data-stu-id="c7d68-156">D3DRS\_ENABLEADAPTIVETESSELLATION</span></span>                             | <span data-ttu-id="c7d68-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-157">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-158">D3DRS \_ FILLMODE</span><span class="sxs-lookup"><span data-stu-id="c7d68-158">D3DRS\_FILLMODE</span></span>                                               | <span data-ttu-id="c7d68-159">D3DFILL \_ 固態</span><span class="sxs-lookup"><span data-stu-id="c7d68-159">D3DFILL\_SOLID</span></span>                                                                                                    |
| <span data-ttu-id="c7d68-160">D3DRS \_ FOGENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-160">D3DRS\_FOGENABLE</span></span>                                              | <span data-ttu-id="c7d68-161">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-161">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-162">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-162">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>                               | <span data-ttu-id="c7d68-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-163">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-164">D3DRS \_ 光源</span><span class="sxs-lookup"><span data-stu-id="c7d68-164">D3DRS\_LIGHTING</span></span>                                               | <span data-ttu-id="c7d68-165">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-165">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-166">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-166">D3DRS\_RANGEFOGENABLE</span></span>                                         | <span data-ttu-id="c7d68-167">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-167">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-168">D3DRS \_ SEPARATEALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-168">D3DRS\_SEPARATEALPHABLENDENABLE</span></span>                               | <span data-ttu-id="c7d68-169">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-169">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-170">D3DRS \_ SHADEMODE</span><span class="sxs-lookup"><span data-stu-id="c7d68-170">D3DRS\_SHADEMODE</span></span>                                              | <span data-ttu-id="c7d68-171">D3DSHADE \_ GOURAUD</span><span class="sxs-lookup"><span data-stu-id="c7d68-171">D3DSHADE\_GOURAUD</span></span>                                                                                                 |
| <span data-ttu-id="c7d68-172">D3DRS \_ SPECULARENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-172">D3DRS\_SPECULARENABLE</span></span>                                         | <span data-ttu-id="c7d68-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-173">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-174">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="c7d68-174">D3DRS\_SRCBLEND</span></span>                                               | <span data-ttu-id="c7d68-175">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="c7d68-175">D3DBLEND\_SRCALPHA</span></span>                                                                                                |
| <span data-ttu-id="c7d68-176">D3DRS \_ SRGBWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-176">D3DRS\_SRGBWRITEENABLE</span></span>                                        | <span data-ttu-id="c7d68-177">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-177">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-178">D3DRS \_ STENCILENABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-178">D3DRS\_STENCILENABLE</span></span>                                          | <span data-ttu-id="c7d68-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-179">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-180">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="c7d68-180">D3DRS\_VERTEXBLEND</span></span>                                            | <span data-ttu-id="c7d68-181">FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d68-181">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="c7d68-182">D3DRS \_ WRAP0</span><span class="sxs-lookup"><span data-stu-id="c7d68-182">D3DRS\_WRAP0</span></span>                                                  | <span data-ttu-id="c7d68-183">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-183">0</span></span>                                                                                                                 |



 

<span data-ttu-id="c7d68-184">材質階段狀態：</span><span class="sxs-lookup"><span data-stu-id="c7d68-184">Texture Stage States:</span></span>



| <span data-ttu-id="c7d68-185">階段識別碼</span><span class="sxs-lookup"><span data-stu-id="c7d68-185">Stage Identifier</span></span> | <span data-ttu-id="c7d68-186">輸入 ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) </span><span class="sxs-lookup"><span data-stu-id="c7d68-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span></span> | <span data-ttu-id="c7d68-187">值</span><span class="sxs-lookup"><span data-stu-id="c7d68-187">Value</span></span>            |
|------------------|---------------------------------------------------------------------------|------------------|
| <span data-ttu-id="c7d68-188">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-188">0</span></span>                | <span data-ttu-id="c7d68-189">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="c7d68-189">D3DTSS\_ALPHAARG1</span></span>                                                         | <span data-ttu-id="c7d68-190">D3DTA \_ 材質</span><span class="sxs-lookup"><span data-stu-id="c7d68-190">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="c7d68-191">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-191">0</span></span>                | <span data-ttu-id="c7d68-192">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="c7d68-192">D3DTSS\_ALPHAARG2</span></span>                                                         | <span data-ttu-id="c7d68-193">D3DTA \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="c7d68-193">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="c7d68-194">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-194">0</span></span>                | <span data-ttu-id="c7d68-195">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="c7d68-195">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="c7d68-196">D3DTOP \_ lambert</span><span class="sxs-lookup"><span data-stu-id="c7d68-196">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="c7d68-197">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-197">0</span></span>                | <span data-ttu-id="c7d68-198">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="c7d68-198">D3DTSS\_COLORARG1</span></span>                                                         | <span data-ttu-id="c7d68-199">D3DTA \_ 材質</span><span class="sxs-lookup"><span data-stu-id="c7d68-199">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="c7d68-200">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-200">0</span></span>                | <span data-ttu-id="c7d68-201">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="c7d68-201">D3DTSS\_COLORARG2</span></span>                                                         | <span data-ttu-id="c7d68-202">D3DTA \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="c7d68-202">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="c7d68-203">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-203">0</span></span>                | <span data-ttu-id="c7d68-204">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="c7d68-204">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="c7d68-205">D3DTOP \_ lambert</span><span class="sxs-lookup"><span data-stu-id="c7d68-205">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="c7d68-206">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-206">0</span></span>                | <span data-ttu-id="c7d68-207">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="c7d68-207">D3DTSS\_TEXCOORDINDEX</span></span>                                                     | <span data-ttu-id="c7d68-208">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-208">0</span></span>                |
| <span data-ttu-id="c7d68-209">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-209">0</span></span>                | <span data-ttu-id="c7d68-210">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="c7d68-210">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>                                             | <span data-ttu-id="c7d68-211">D3DTTFF \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-211">D3DTTFF\_DISABLE</span></span> |
| <span data-ttu-id="c7d68-212">1</span><span class="sxs-lookup"><span data-stu-id="c7d68-212">1</span></span>                | <span data-ttu-id="c7d68-213">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="c7d68-213">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="c7d68-214">D3DTOP \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-214">D3DTOP\_DISABLE</span></span>  |
| <span data-ttu-id="c7d68-215">1</span><span class="sxs-lookup"><span data-stu-id="c7d68-215">1</span></span>                | <span data-ttu-id="c7d68-216">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="c7d68-216">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="c7d68-217">D3DTOP \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="c7d68-217">D3DTOP\_DISABLE</span></span>  |



 

<span data-ttu-id="c7d68-218">取樣器狀態：</span><span class="sxs-lookup"><span data-stu-id="c7d68-218">Sampler States:</span></span>



| <span data-ttu-id="c7d68-219">取樣器階段索引</span><span class="sxs-lookup"><span data-stu-id="c7d68-219">Sampler Stage Index</span></span> | <span data-ttu-id="c7d68-220">輸入 ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) </span><span class="sxs-lookup"><span data-stu-id="c7d68-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span></span> | <span data-ttu-id="c7d68-221">值</span><span class="sxs-lookup"><span data-stu-id="c7d68-221">Value</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d68-222">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-222">0</span></span>                   | <span data-ttu-id="c7d68-223">D3DSAMP \_ ADDRESSU</span><span class="sxs-lookup"><span data-stu-id="c7d68-223">D3DSAMP\_ADDRESSU</span></span>                                               | <span data-ttu-id="c7d68-224">D3DTADDRESS \_ 夾具</span><span class="sxs-lookup"><span data-stu-id="c7d68-224">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="c7d68-225">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-225">0</span></span>                   | <span data-ttu-id="c7d68-226">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="c7d68-226">D3DSAMP\_ADDRESSV</span></span>                                               | <span data-ttu-id="c7d68-227">D3DTADDRESS \_ 夾具</span><span class="sxs-lookup"><span data-stu-id="c7d68-227">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="c7d68-228">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-228">0</span></span>                   | <span data-ttu-id="c7d68-229">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="c7d68-229">D3DSAMP\_MAGFILTER</span></span>                                              | <span data-ttu-id="c7d68-230">\_如果 TextureFilterCaps 包含 D3DPTFILTERCAPS MAGFANISOTROPIC，則為 D3DTEXF \_ ，否則為 D3DTEXF \_ 線性</span><span class="sxs-lookup"><span data-stu-id="c7d68-230">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MAGFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="c7d68-231">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-231">0</span></span>                   | <span data-ttu-id="c7d68-232">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="c7d68-232">D3DSAMP\_MAXMIPLEVEL</span></span>                                            | <span data-ttu-id="c7d68-233">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-233">0</span></span>                                                                                                              |
| <span data-ttu-id="c7d68-234">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-234">0</span></span>                   | <span data-ttu-id="c7d68-235">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="c7d68-235">D3DSAMP\_MAXANISOTROPY</span></span>                                          | <span data-ttu-id="c7d68-236">MaxAnisotropy</span><span class="sxs-lookup"><span data-stu-id="c7d68-236">MaxAnisotropy</span></span>                                                                                                  |
| <span data-ttu-id="c7d68-237">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-237">0</span></span>                   | <span data-ttu-id="c7d68-238">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="c7d68-238">D3DSAMP\_MINFILTER</span></span>                                              | <span data-ttu-id="c7d68-239">\_如果 TextureFilterCaps 包含 D3DPTFILTERCAPS MINFANISOTROPIC，則為 D3DTEXF \_ ，否則為 D3DTEXF \_ 線性</span><span class="sxs-lookup"><span data-stu-id="c7d68-239">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MINFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="c7d68-240">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-240">0</span></span>                   | <span data-ttu-id="c7d68-241">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="c7d68-241">D3DSAMP\_MIPFILTER</span></span>                                              | <span data-ttu-id="c7d68-242">\_如果 TextureFilterCaps 包含 D3DPTFILTERCAPS \_ MIPFLINEAR，則為線性 D3DTEXF，否則為 D3DTEXF \_ 點</span><span class="sxs-lookup"><span data-stu-id="c7d68-242">D3DTEXF\_LINEAR if TextureFilterCaps includes D3DPTFILTERCAPS\_MIPFLINEAR; otherwise D3DTEXF\_POINT</span></span>            |
| <span data-ttu-id="c7d68-243">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-243">0</span></span>                   | <span data-ttu-id="c7d68-244">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="c7d68-244">D3DSAMP\_MIPMAPLODBIAS</span></span>                                          | <span data-ttu-id="c7d68-245">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-245">0</span></span>                                                                                                              |
| <span data-ttu-id="c7d68-246">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-246">0</span></span>                   | <span data-ttu-id="c7d68-247">D3DSAMP \_ SRGBTEXTURE</span><span class="sxs-lookup"><span data-stu-id="c7d68-247">D3DSAMP\_SRGBTEXTURE</span></span>                                            | <span data-ttu-id="c7d68-248">0</span><span class="sxs-lookup"><span data-stu-id="c7d68-248">0</span></span>                                                                                                              |



 

> [!Note]  
> <span data-ttu-id="c7d68-249">這個方法會停用 N 個修補程式。</span><span class="sxs-lookup"><span data-stu-id="c7d68-249">This method disables N-patches.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7d68-250">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7d68-250">Requirements</span></span>



| <span data-ttu-id="c7d68-251">需求</span><span class="sxs-lookup"><span data-stu-id="c7d68-251">Requirement</span></span> | <span data-ttu-id="c7d68-252">值</span><span class="sxs-lookup"><span data-stu-id="c7d68-252">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d68-253">標頭</span><span class="sxs-lookup"><span data-stu-id="c7d68-253">Header</span></span><br/>  | <dl> <span data-ttu-id="c7d68-254"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7d68-254"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c7d68-255">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7d68-255">Library</span></span><br/> | <dl> <span data-ttu-id="c7d68-256"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7d68-256"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7d68-257">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7d68-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d68-258">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="c7d68-258">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="c7d68-259">D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="c7d68-259">D3DXSPRITE</span></span>](d3dxsprite.md)
</dt> </dl>

 

 
