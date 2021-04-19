---
description: 從每個頂點的資料計算每個三角形的 IMT。 此函式可讓您根據網格 (色彩、正常等) 中的任何值來計算 IMT。
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: 'D3DXComputeIMTFromPerVertexSignal 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997401"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a><span data-ttu-id="c8b11-104">D3DXComputeIMTFromPerVertexSignal 函式</span><span class="sxs-lookup"><span data-stu-id="c8b11-104">D3DXComputeIMTFromPerVertexSignal function</span></span>

<span data-ttu-id="c8b11-105">從每個頂點的資料計算每個三角形的 IMT。</span><span class="sxs-lookup"><span data-stu-id="c8b11-105">Calculate per-triangle IMT's from from per-vertex data.</span></span> <span data-ttu-id="c8b11-106">此函式可讓您根據網格 (色彩、正常等) 中的任何值來計算 IMT。</span><span class="sxs-lookup"><span data-stu-id="c8b11-106">This function allows you to calculate the IMT based off of any value in a mesh (color, normal, etc).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b11-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8b11-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="c8b11-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8b11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b11-109">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8b11-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b11-110">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b11-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="c8b11-111">輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算 IMT 的物件幾何。</span><span class="sxs-lookup"><span data-stu-id="c8b11-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="c8b11-112">*pfVertexSignal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8b11-112">*pfVertexSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b11-113">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8b11-113">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c8b11-114">將計算 IMT 的每個頂點資料陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c8b11-114">A pointer to an array of per-vertex data from which IMT will be computed.</span></span> <span data-ttu-id="c8b11-115">陣列大小是 uSignalStride \* v，其中 v 是網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="c8b11-115">The array size is uSignalStride \* v, where v is the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c8b11-116">*uSignalDimension* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8b11-116">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b11-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b11-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8b11-118">每個頂點的浮點數。</span><span class="sxs-lookup"><span data-stu-id="c8b11-118">The number of floats per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c8b11-119">*uSignalStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8b11-119">*uSignalStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b11-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b11-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8b11-121">陣列中每個頂點的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c8b11-121">The number of bytes per vertex in the array.</span></span> <span data-ttu-id="c8b11-122">這必須是 sizeof (浮點數中的倍數) </span><span class="sxs-lookup"><span data-stu-id="c8b11-122">This must be a multiple of sizeof(float)</span></span>

</dd> <dt>

<span data-ttu-id="c8b11-123">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8b11-123">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b11-124">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b11-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8b11-125">材質換行選項。</span><span class="sxs-lookup"><span data-stu-id="c8b11-125">Texture wrap options.</span></span> <span data-ttu-id="c8b11-126">這是一或多個 [**D3DXIMT 旗標**](./d3dximt-flags.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="c8b11-126">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b11-127">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="c8b11-127">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b11-128">類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b11-128">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="c8b11-129">回呼函式的指標，可監視 IMT 計算進度。</span><span class="sxs-lookup"><span data-stu-id="c8b11-129">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="c8b11-130">*pUserCoNtext*</span><span class="sxs-lookup"><span data-stu-id="c8b11-130">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b11-131">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8b11-131">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8b11-132">使用者自訂變數的指標，該變數會傳遞至狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c8b11-132">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="c8b11-133">通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="c8b11-133">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c8b11-134">*ppIMTData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8b11-134">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b11-135">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8b11-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c8b11-136">緩衝區的指標 (查看包含所傳回 IMT 陣列的 [**ID3DXBuffer**](id3dxbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c8b11-136">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="c8b11-137">您可以提供此陣列作為 D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) 函式的輸入，來排列材質參數化中材質配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c8b11-137">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b11-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8b11-138">Return value</span></span>

<span data-ttu-id="c8b11-139">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8b11-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8b11-140">如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c8b11-140">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b11-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8b11-141">Requirements</span></span>



| <span data-ttu-id="c8b11-142">需求</span><span class="sxs-lookup"><span data-stu-id="c8b11-142">Requirement</span></span> | <span data-ttu-id="c8b11-143">值</span><span class="sxs-lookup"><span data-stu-id="c8b11-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b11-144">標頭</span><span class="sxs-lookup"><span data-stu-id="c8b11-144">Header</span></span><br/>  | <dl> <span data-ttu-id="c8b11-145"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b11-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c8b11-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8b11-146">Library</span></span><br/> | <dl> <span data-ttu-id="c8b11-147"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8b11-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8b11-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8b11-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b11-149">UVAtlas 函式</span><span class="sxs-lookup"><span data-stu-id="c8b11-149">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="c8b11-150">使用 UVAtlas (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="c8b11-150">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
