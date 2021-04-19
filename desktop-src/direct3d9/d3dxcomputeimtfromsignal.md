---
description: 從自訂應用程式指定的信號計算每個三角形的 IMT，這些信號會隨著格線的表面變化， (通常會高於頂點資料) 的頻率。 信號是透過使用者指定的回呼函數來評估。
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: 'D3DXComputeIMTFromSignal 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993893"
---
# <a name="d3dxcomputeimtfromsignal-function"></a><span data-ttu-id="1f755-104">D3DXComputeIMTFromSignal 函式</span><span class="sxs-lookup"><span data-stu-id="1f755-104">D3DXComputeIMTFromSignal function</span></span>

<span data-ttu-id="1f755-105">從自訂應用程式指定的信號計算每個三角形的 IMT，這些信號會隨著格線的表面變化， (通常會高於頂點資料) 的頻率。</span><span class="sxs-lookup"><span data-stu-id="1f755-105">Calculates per-triangle IMT's from a custom application-specified signal that varies over the surface of the mesh (generally at a higher frequency than vertex data).</span></span> <span data-ttu-id="1f755-106">信號是透過使用者指定的回呼函數來評估。</span><span class="sxs-lookup"><span data-stu-id="1f755-106">The signal is evaluated via a user-specified callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f755-107">語法</span><span class="sxs-lookup"><span data-stu-id="1f755-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="1f755-108">參數</span><span class="sxs-lookup"><span data-stu-id="1f755-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f755-109">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f755-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-110">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1f755-111">輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算 IMT 的物件幾何。</span><span class="sxs-lookup"><span data-stu-id="1f755-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="1f755-112">*dwTextureIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f755-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f755-114">以零為基礎的材質座標索引，識別要使用的材質座標集。</span><span class="sxs-lookup"><span data-stu-id="1f755-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="1f755-115">*uSignalDimension* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f755-115">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f755-117">信號中每個資料點的元件數目。</span><span class="sxs-lookup"><span data-stu-id="1f755-117">The number of components in each data point in the signal.</span></span>

</dd> <dt>

<span data-ttu-id="1f755-118">*fMaxUVDistance* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f755-118">*fMaxUVDistance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-119">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f755-120">頂點之間的最大距離;演算法會繼續進行細分，直到所有頂點之間的距離小於或等於 fMaxUVDistance 為止。</span><span class="sxs-lookup"><span data-stu-id="1f755-120">The maximum distance between vertices; the algorithm continues subdividing until the distance between all vertices is less than or equal to fMaxUVDistance.</span></span>

</dd> <dt>

<span data-ttu-id="1f755-121">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f755-121">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f755-123">材質換行選項。</span><span class="sxs-lookup"><span data-stu-id="1f755-123">Texture wrap options.</span></span> <span data-ttu-id="1f755-124">這是一或多個 [**D3DXIMT 旗標**](./d3dximt-flags.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="1f755-124">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f755-125">*pSignalCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f755-125">*pSignalCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-126">類型： **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-126">Type: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span></span>

<span data-ttu-id="1f755-127">使用者提供的評估工具函式的指標，該函式將用來計算任意 U、V 座標的信號值。</span><span class="sxs-lookup"><span data-stu-id="1f755-127">A pointer to a user-provided evaluator function, which will be used to compute the signal value at arbitrary U,V coordinates.</span></span> <span data-ttu-id="1f755-128">函數會遵循 [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)的原型。</span><span class="sxs-lookup"><span data-stu-id="1f755-128">The function follows the prototype of [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f755-129">*pUserData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f755-129">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-130">類型： **VOID \***</span><span class="sxs-lookup"><span data-stu-id="1f755-130">Type: **VOID\***</span></span>

<span data-ttu-id="1f755-131">傳遞給信號回呼函式的使用者定義值指標。</span><span class="sxs-lookup"><span data-stu-id="1f755-131">A pointer to a user-defined value which is passed to the signal callback function.</span></span> <span data-ttu-id="1f755-132">通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="1f755-132">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="1f755-133">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="1f755-133">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="1f755-134">類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-134">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="1f755-135">回呼函式的指標，可監視 IMT 計算進度。</span><span class="sxs-lookup"><span data-stu-id="1f755-135">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="1f755-136">*pUserCoNtext*</span><span class="sxs-lookup"><span data-stu-id="1f755-136">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="1f755-137">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f755-137">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f755-138">使用者自訂變數的指標，該變數會傳遞至狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1f755-138">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="1f755-139">通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="1f755-139">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="1f755-140">*ppIMTData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1f755-140">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f755-141">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f755-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1f755-142">緩衝區的指標 (查看包含所傳回 IMT 陣列的 [**ID3DXBuffer**](id3dxbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1f755-142">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="1f755-143">您可以提供此陣列作為 D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) 函式的輸入，來排列材質參數化中材質配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="1f755-143">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f755-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f755-144">Return value</span></span>

<span data-ttu-id="1f755-145">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f755-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f755-146">如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="1f755-146">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f755-147">備註</span><span class="sxs-lookup"><span data-stu-id="1f755-147">Remarks</span></span>

<span data-ttu-id="1f755-148">此函式要求輸入網格必須包含 (ie 的信號到網格材質對應。材質座標) 。</span><span class="sxs-lookup"><span data-stu-id="1f755-148">This function requires that the input mesh contain a signal-to-mesh texture mapping (ie. texture coordinates).</span></span> <span data-ttu-id="1f755-149">它可讓使用者在網格表面上任意定義信號。</span><span class="sxs-lookup"><span data-stu-id="1f755-149">It allows the user to define a signal arbitrarily over the surface of the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f755-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f755-150">Requirements</span></span>



| <span data-ttu-id="1f755-151">需求</span><span class="sxs-lookup"><span data-stu-id="1f755-151">Requirement</span></span> | <span data-ttu-id="1f755-152">值</span><span class="sxs-lookup"><span data-stu-id="1f755-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f755-153">標頭</span><span class="sxs-lookup"><span data-stu-id="1f755-153">Header</span></span><br/>  | <dl> <span data-ttu-id="1f755-154"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f755-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1f755-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f755-155">Library</span></span><br/> | <dl> <span data-ttu-id="1f755-156"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f755-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1f755-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f755-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f755-158">UVAtlas 函式</span><span class="sxs-lookup"><span data-stu-id="1f755-158">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="1f755-159">使用 UVAtlas (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1f755-159">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
