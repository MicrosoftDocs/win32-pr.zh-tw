---
description: ID3DXTextureGutterHelper 介面是用來建立和管理材質中的裝訂區區域。 裝訂邊區域會將材質分開，並允許雙線性插補，以避免在材質界限呈現成品。
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: 'ID3DXTextureGutterHelper 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323223"
---
# <a name="id3dxtexturegutterhelper-interface"></a><span data-ttu-id="d5c49-104">ID3DXTextureGutterHelper 介面</span><span class="sxs-lookup"><span data-stu-id="d5c49-104">ID3DXTextureGutterHelper interface</span></span>

<span data-ttu-id="d5c49-105">ID3DXTextureGutterHelper 介面是用來建立和管理材質中的裝訂區區域。</span><span class="sxs-lookup"><span data-stu-id="d5c49-105">The ID3DXTextureGutterHelper interface is used to build and manage gutter regions in a texture.</span></span> <span data-ttu-id="d5c49-106">裝訂邊區域會將材質分開，並允許雙線性插補，以避免在材質界限呈現成品。</span><span class="sxs-lookup"><span data-stu-id="d5c49-106">Gutter regions separate textures and allow for bilinear interpolation to avoid rendering artifacts at texture boundaries.</span></span>

<span data-ttu-id="d5c49-107">Get .。。方法可讓您存取 Apply 所使用的資料結構 .。。方法。</span><span class="sxs-lookup"><span data-stu-id="d5c49-107">The Get... methods provide access to the data structures used by the Apply... methods.</span></span>

## <a name="members"></a><span data-ttu-id="d5c49-108">成員</span><span class="sxs-lookup"><span data-stu-id="d5c49-108">Members</span></span>

<span data-ttu-id="d5c49-109">**ID3DXTextureGutterHelper** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d5c49-109">The **ID3DXTextureGutterHelper** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5c49-110">**ID3DXTextureGutterHelper** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d5c49-110">**ID3DXTextureGutterHelper** also has these types of members:</span></span>

-   [<span data-ttu-id="d5c49-111">方法</span><span class="sxs-lookup"><span data-stu-id="d5c49-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5c49-112">方法</span><span class="sxs-lookup"><span data-stu-id="d5c49-112">Methods</span></span>

<span data-ttu-id="d5c49-113">**ID3DXTextureGutterHelper** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d5c49-113">The **ID3DXTextureGutterHelper** interface has these methods.</span></span>



| <span data-ttu-id="d5c49-114">方法</span><span class="sxs-lookup"><span data-stu-id="d5c49-114">Method</span></span>                                                                   | <span data-ttu-id="d5c49-115">描述</span><span class="sxs-lookup"><span data-stu-id="d5c49-115">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5c49-116">**ApplyGuttersFloat**</span><span class="sxs-lookup"><span data-stu-id="d5c49-116">**ApplyGuttersFloat**</span></span>](id3dxtexturegutterhelper--applyguttersfloat.md) | <span data-ttu-id="d5c49-117">將裝訂邊套用至 FLOAT 材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d5c49-117">Applies gutters to a FLOAT texture buffer.</span></span><br/>                                                  |
| [<span data-ttu-id="d5c49-118">**ApplyGuttersPRT**</span><span class="sxs-lookup"><span data-stu-id="d5c49-118">**ApplyGuttersPRT**</span></span>](id3dxtexturegutterhelper--applyguttersprt.md)     | <span data-ttu-id="d5c49-119">將裝訂邊套用至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="d5c49-119">Applies gutters to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer object.</span></span><br/>               |
| [<span data-ttu-id="d5c49-120">**ApplyGuttersTex**</span><span class="sxs-lookup"><span data-stu-id="d5c49-120">**ApplyGuttersTex**</span></span>](id3dxtexturegutterhelper--applygutterstex.md)     | <span data-ttu-id="d5c49-121">將裝訂邊套用至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 材質物件。</span><span class="sxs-lookup"><span data-stu-id="d5c49-121">Applies gutters to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object.</span></span><br/>        |
| [<span data-ttu-id="d5c49-122">**GetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-122">**GetBaryMap**</span></span>](id3dxtexturegutterhelper--getbarymap.md)               | <span data-ttu-id="d5c49-123">抓取材質 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="d5c49-123">Retrieves texel barycentric coordinates.</span></span><br/>                                                    |
| [<span data-ttu-id="d5c49-124">**GetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-124">**GetFaceMap**</span></span>](id3dxtexturegutterhelper--getfacemap.md)               | <span data-ttu-id="d5c49-125">抓取每個材質所屬之網格臉部的索引。</span><span class="sxs-lookup"><span data-stu-id="d5c49-125">Retrieves the index of the mesh face to which each texel belongs.</span></span><br/>                           |
| [<span data-ttu-id="d5c49-126">**GetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-126">**GetGutterMap**</span></span>](id3dxtexturegutterhelper--getguttermap.md)           | <span data-ttu-id="d5c49-127">接收材質類別值，指出根據每個材質位置的材質類別。</span><span class="sxs-lookup"><span data-stu-id="d5c49-127">Receives a texel class value that indicates texel class according to each texel's location.</span></span><br/> |
| [<span data-ttu-id="d5c49-128">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="d5c49-128">**GetHeight**</span></span>](id3dxtexturegutterhelper--getheight.md)                 | <span data-ttu-id="d5c49-129">抓取紋理的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5c49-129">Retrieves the height of the texture, in pixels.</span></span><br/>                                             |
| [<span data-ttu-id="d5c49-130">**GetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-130">**GetTexelMap**</span></span>](id3dxtexturegutterhelper--gettexelmap.md)             | <span data-ttu-id="d5c49-131">抓取每個材質的 (u，v) 材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5c49-131">Retrieves the (u, v) texture coordinates of each texel.</span></span><br/>                                     |
| [<span data-ttu-id="d5c49-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="d5c49-132">**GetWidth**</span></span>](id3dxtexturegutterhelper--getwidth.md)                   | <span data-ttu-id="d5c49-133">抓取紋理的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5c49-133">Retrieves the width of the texture, in pixels.</span></span><br/>                                              |
| [<span data-ttu-id="d5c49-134">**ResampleTex**</span><span class="sxs-lookup"><span data-stu-id="d5c49-134">**ResampleTex**</span></span>](id3dxtexturegutterhelper--resampletex.md)             | <span data-ttu-id="d5c49-135">將材質 Resamples 到這個 gutterhelper 的參數化。</span><span class="sxs-lookup"><span data-stu-id="d5c49-135">Resamples a texture into this gutterhelper's parameterization.</span></span><br/>                              |
| [<span data-ttu-id="d5c49-136">**SetBaryMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-136">**SetBaryMap**</span></span>](id3dxtexturegutterhelper--setbarymap.md)               | <span data-ttu-id="d5c49-137">設定材質 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="d5c49-137">Sets texel barycentric coordinates.</span></span><br/>                                                         |
| [<span data-ttu-id="d5c49-138">**SetFaceMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-138">**SetFaceMap**</span></span>](id3dxtexturegutterhelper--setfacemap.md)               | <span data-ttu-id="d5c49-139">設定每個材質所屬之網格臉部的索引。</span><span class="sxs-lookup"><span data-stu-id="d5c49-139">Sets the index of the mesh face to which each texel belongs.</span></span><br/>                                |
| [<span data-ttu-id="d5c49-140">**SetGutterMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-140">**SetGutterMap**</span></span>](id3dxtexturegutterhelper--setguttermap.md)           | <span data-ttu-id="d5c49-141">設定材質類別值，指出根據每個材質位置的材質類別。</span><span class="sxs-lookup"><span data-stu-id="d5c49-141">Sets a texel class value that indicates texel class according to each texel's location.</span></span><br/>     |
| [<span data-ttu-id="d5c49-142">**SetTexelMap**</span><span class="sxs-lookup"><span data-stu-id="d5c49-142">**SetTexelMap**</span></span>](id3dxtexturegutterhelper--settexelmap.md)             | <span data-ttu-id="d5c49-143">設定每個材質的 (u，v) 材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5c49-143">Sets the (u, v) texture coordinates of each texel.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="d5c49-144">備註</span><span class="sxs-lookup"><span data-stu-id="d5c49-144">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5c49-145">搭配預先計算 radiance transfer (PRT) 使用時，此介面需要模型的唯一參數化。</span><span class="sxs-lookup"><span data-stu-id="d5c49-145">When used with precomputed radiance transfer (PRT), this interface requires a unique parameterization of the model.</span></span> <span data-ttu-id="d5c49-146">每個材質都必須對應到模型表面上的單一點，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="d5c49-146">Every texel must correspond to a single point on the surface of the model and vice-versa.</span></span> <span data-ttu-id="d5c49-147">如果模型包含多個紋理，則必須將它分割成個別的片段，每個材質各包含一個裝訂邊協助程式物件。</span><span class="sxs-lookup"><span data-stu-id="d5c49-147">If the model includes multiple textures, it must be split into separate pieces that each contain one gutter helper object per texture.</span></span>

 

<span data-ttu-id="d5c49-148">這個介面可以用來在材質空間中產生地圖，其中每個材質都是在四個類別中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="d5c49-148">This interface can be used to generate a map in texture space in which each texel is in one of four classes.</span></span>



| <span data-ttu-id="d5c49-149">材質類別</span><span class="sxs-lookup"><span data-stu-id="d5c49-149">Texel Class</span></span> | <span data-ttu-id="d5c49-150">材質位置</span><span class="sxs-lookup"><span data-stu-id="d5c49-150">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c49-151">0</span><span class="sxs-lookup"><span data-stu-id="d5c49-151">0</span></span>           | <span data-ttu-id="d5c49-152">不正確點;將不會使用材質。</span><span class="sxs-lookup"><span data-stu-id="d5c49-152">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d5c49-153">1</span><span class="sxs-lookup"><span data-stu-id="d5c49-153">1</span></span>           | <span data-ttu-id="d5c49-154">在三角形內。</span><span class="sxs-lookup"><span data-stu-id="d5c49-154">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d5c49-155">2</span><span class="sxs-lookup"><span data-stu-id="d5c49-155">2</span></span>           | <span data-ttu-id="d5c49-156">在裝訂邊內。</span><span class="sxs-lookup"><span data-stu-id="d5c49-156">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d5c49-157">4</span><span class="sxs-lookup"><span data-stu-id="d5c49-157">4</span></span>           | <span data-ttu-id="d5c49-158">內部裝訂邊;材質將會評估為 [**ID3DXTextureGutterHelper：： ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md)、 [**ID3DXTextureGutterHelper：： ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)或 [**ID3DXTextureGutterHelper：： ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) 方法中的完整範例。</span><span class="sxs-lookup"><span data-stu-id="d5c49-158">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

<span data-ttu-id="d5c49-159">針對類別1和2，材質會與它所屬的臉部一起儲存，以及該臉部前兩個頂點的 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="d5c49-159">For classes 1 and 2, a texel is stored with the face it belongs to, along with barycentric coordinates of the first two vertices of that face.</span></span> <span data-ttu-id="d5c49-160">裝訂邊頂點會指派至材質空間中最接近的邊緣。</span><span class="sxs-lookup"><span data-stu-id="d5c49-160">Gutter vertices are assigned to the closest edge in texture space.</span></span>

<span data-ttu-id="d5c49-161">沒有材質類別3。</span><span class="sxs-lookup"><span data-stu-id="d5c49-161">There is no texel class 3.</span></span>

<span data-ttu-id="d5c49-162">**ID3DXTextureGutterHelper** 介面是藉由呼叫 [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="d5c49-162">The **ID3DXTextureGutterHelper** interface is obtained by calling the [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) function.</span></span>

<span data-ttu-id="d5c49-163">LPD3DXTEXTUREGUTTERHELPER 型別定義為 **ID3DXTextureGutterHelper** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d5c49-163">The LPD3DXTEXTUREGUTTERHELPER type is defined as a pointer to the **ID3DXTextureGutterHelper** interface.</span></span>


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a><span data-ttu-id="d5c49-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5c49-164">Requirements</span></span>



| <span data-ttu-id="d5c49-165">需求</span><span class="sxs-lookup"><span data-stu-id="d5c49-165">Requirement</span></span> | <span data-ttu-id="d5c49-166">值</span><span class="sxs-lookup"><span data-stu-id="d5c49-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c49-167">標頭</span><span class="sxs-lookup"><span data-stu-id="d5c49-167">Header</span></span><br/>  | <dl> <span data-ttu-id="d5c49-168"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c49-168"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d5c49-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5c49-169">Library</span></span><br/> | <dl> <span data-ttu-id="d5c49-170"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5c49-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5c49-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5c49-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c49-172">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="d5c49-172">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
