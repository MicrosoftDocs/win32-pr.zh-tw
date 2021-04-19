---
description: 使用調適型取樣來計算由單一 interreflected 燈彈跳產生的來源 radiance。
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'ID3DXPRTEngine：： ComputeBounceAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986124"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a><span data-ttu-id="e714c-103">ID3DXPRTEngine：： ComputeBounceAdaptive 方法</span><span class="sxs-lookup"><span data-stu-id="e714c-103">ID3DXPRTEngine::ComputeBounceAdaptive method</span></span>

<span data-ttu-id="e714c-104">使用調適型取樣來計算由單一 interreflected 燈彈跳產生的來源 radiance。</span><span class="sxs-lookup"><span data-stu-id="e714c-104">Computes the source radiance resulting from a single bounce of interreflected light, using adaptive sampling.</span></span> <span data-ttu-id="e714c-105">這個方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。</span><span class="sxs-lookup"><span data-stu-id="e714c-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="e714c-106">此方法可用於任何照明的場景，包括球形調和 (SH) 為基礎的 PRT 模型。</span><span class="sxs-lookup"><span data-stu-id="e714c-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based PRT model.</span></span>

## <a name="syntax"></a><span data-ttu-id="e714c-107">語法</span><span class="sxs-lookup"><span data-stu-id="e714c-107">Syntax</span></span>


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="e714c-108">參數</span><span class="sxs-lookup"><span data-stu-id="e714c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e714c-109">*pDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e714c-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e714c-110">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e714c-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e714c-111">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件代表前一個光線彈跳的3d 物件。</span><span class="sxs-lookup"><span data-stu-id="e714c-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="e714c-112">此輸入緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="e714c-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e714c-113">*AdaptiveThresh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e714c-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e714c-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e714c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e714c-115">用於細分網格頂點和臉部的 PRT 向量閾值。</span><span class="sxs-lookup"><span data-stu-id="e714c-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="e714c-116">如果小於 1e-6f，則會指定值為 1e-6f 的預設值。</span><span class="sxs-lookup"><span data-stu-id="e714c-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="e714c-117">*MinEdgeLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e714c-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e714c-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e714c-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e714c-119">自動調整取樣中將產生的最小臉部邊長度。</span><span class="sxs-lookup"><span data-stu-id="e714c-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="e714c-120">如果方法判斷該值太小，則會指定模型相依的值。</span><span class="sxs-lookup"><span data-stu-id="e714c-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="e714c-121">如果為零，則會指定預設值4。</span><span class="sxs-lookup"><span data-stu-id="e714c-121">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="e714c-122">*MaxSubdiv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e714c-122">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e714c-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e714c-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e714c-124">臉部的最大細分層級，將用於適應性取樣中。</span><span class="sxs-lookup"><span data-stu-id="e714c-124">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e714c-125">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e714c-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e714c-126">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e714c-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e714c-127">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e714c-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="e714c-128">此輸出緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="e714c-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e714c-129">*pDataTotal* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e714c-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e714c-130">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e714c-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e714c-131">選擇性 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，此物件會保持 pDataOut 的執行總和與每個輕量彈跳計算。</span><span class="sxs-lookup"><span data-stu-id="e714c-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that keeps a running sum of pDataOut with each light bounce computation.</span></span> <span data-ttu-id="e714c-132">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e714c-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e714c-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="e714c-133">Return value</span></span>

<span data-ttu-id="e714c-134">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e714c-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e714c-135">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e714c-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e714c-136">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e714c-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e714c-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="e714c-137">Requirements</span></span>



| <span data-ttu-id="e714c-138">需求</span><span class="sxs-lookup"><span data-stu-id="e714c-138">Requirement</span></span> | <span data-ttu-id="e714c-139">值</span><span class="sxs-lookup"><span data-stu-id="e714c-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e714c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="e714c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e714c-141"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e714c-141"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e714c-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="e714c-142">Library</span></span><br/> | <dl> <span data-ttu-id="e714c-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e714c-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e714c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e714c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e714c-145">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e714c-145">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e714c-146">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="e714c-146">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
