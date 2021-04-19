---
description: 計算每個材質資料的每個三角形 IMT。 此函式類似于 D3DXComputeIMTFromTexture，但它會使用浮點數陣列來傳入資料，而且它可以計算高於4的維度值。
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: 'D3DXComputeIMTFromPerTexelSignal 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981836"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a><span data-ttu-id="f3bf8-104">D3DXComputeIMTFromPerTexelSignal 函式</span><span class="sxs-lookup"><span data-stu-id="f3bf8-104">D3DXComputeIMTFromPerTexelSignal function</span></span>

<span data-ttu-id="f3bf8-105">計算每個材質資料的每個三角形 IMT。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-105">Calculate per-triangle IMT's from per-texel data.</span></span> <span data-ttu-id="f3bf8-106">此函式類似于 [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md)，但它會使用浮點數陣列來傳入資料，而且它可以計算高於4的維度值。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-106">This function is similar to [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), but it uses a float array to pass in the data, and it can calculate higher dimensional values than 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3bf8-107">語法</span><span class="sxs-lookup"><span data-stu-id="f3bf8-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="f3bf8-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3bf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3bf8-109">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-110">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f3bf8-111">輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算 IMT 的物件幾何。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-112">*dwTextureIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3bf8-114">以零為基礎的材質座標索引，識別要使用的材質座標集。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-115">*pfTexelSignal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-115">*pfTexelSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-116">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3bf8-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f3bf8-117">將計算 IMT 的輸入材質陣列指標。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-117">A pointer to an array of input texels from which IMT will be computed.</span></span> <span data-ttu-id="f3bf8-118">陣列大小是 uWidth \* uHeight \* uComponents。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-118">The array size is uWidth\*uHeight\*uComponents.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-119">*uWidth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-119">*uWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3bf8-121">材質寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-121">Texture width in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-122">*uHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-122">*uHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3bf8-124">材質高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-124">Texture height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-125">*uSignalDimension* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-125">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3bf8-127">每個元件在信號陣列的每個元素中的浮點數。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-127">The number of floats per-component in each element of the signal array.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-128">*uComponents* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-128">*uComponents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-129">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3bf8-130">每個材質中的元件數目。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-130">The number of components in each texel.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-131">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-131">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3bf8-133">材質換行選項。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-133">Texture wrap options.</span></span> <span data-ttu-id="f3bf8-134">這是一或多個 [**D3DXIMT 旗標**](./d3dximt-flags.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-134">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-135">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="f3bf8-135">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="f3bf8-136">類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="f3bf8-137">回呼函式的指標，可監視 IMT 計算進度。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-137">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-138">*pUserCoNtext*</span><span class="sxs-lookup"><span data-stu-id="f3bf8-138">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="f3bf8-139">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-139">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3bf8-140">使用者自訂變數的指標，該變數會傳遞至狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-140">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="f3bf8-141">通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-141">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="f3bf8-142">*ppIMTData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3bf8-142">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3bf8-143">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3bf8-143">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f3bf8-144">緩衝區的指標 (查看包含所傳回 IMT 陣列的 [**ID3DXBuffer**](id3dxbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-144">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="f3bf8-145">您可以提供此陣列作為 D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) 函式的輸入，來排列材質參數化中材質配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-145">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3bf8-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3bf8-146">Return value</span></span>

<span data-ttu-id="f3bf8-147">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3bf8-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3bf8-148">如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f3bf8-148">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3bf8-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3bf8-149">Requirements</span></span>



| <span data-ttu-id="f3bf8-150">需求</span><span class="sxs-lookup"><span data-stu-id="f3bf8-150">Requirement</span></span> | <span data-ttu-id="f3bf8-151">值</span><span class="sxs-lookup"><span data-stu-id="f3bf8-151">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3bf8-152">標頭</span><span class="sxs-lookup"><span data-stu-id="f3bf8-152">Header</span></span><br/>  | <dl> <span data-ttu-id="f3bf8-153"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3bf8-153"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f3bf8-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3bf8-154">Library</span></span><br/> | <dl> <span data-ttu-id="f3bf8-155"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3bf8-155"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3bf8-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3bf8-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3bf8-157">UVAtlas 函式</span><span class="sxs-lookup"><span data-stu-id="f3bf8-157">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="f3bf8-158">使用 UVAtlas (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="f3bf8-158">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
