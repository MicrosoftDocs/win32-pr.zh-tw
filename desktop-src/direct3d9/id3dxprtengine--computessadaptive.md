---
description: 計算使用 ID3DXPRTEngine：： SetMeshMaterials 所設定的調適型取樣和材質屬性，將來源 radiance 對應至地下散佈所產生之結束 radiance 的傳輸向量。
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'ID3DXPRTEngine：： ComputeSSAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993920"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a><span data-ttu-id="2b5ef-103">ID3DXPRTEngine：： ComputeSSAdaptive 方法</span><span class="sxs-lookup"><span data-stu-id="2b5ef-103">ID3DXPRTEngine::ComputeSSAdaptive method</span></span>

<span data-ttu-id="2b5ef-104">計算使用 [**ID3DXPRTEngine：： SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)所設定的調適型取樣和材質屬性，將來源 radiance 對應至地下散佈所產生之結束 radiance 的傳輸向量。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-104">Computes a transfer vector that maps source radiance to exit radiance resulting from subsurface scattering, using adaptive sampling and material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="2b5ef-105">方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-105">The method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="2b5ef-106">這個方法僅適用于網格物件中每個頂點定義的材質。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b5ef-107">語法</span><span class="sxs-lookup"><span data-stu-id="2b5ef-107">Syntax</span></span>


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="2b5ef-108">參數</span><span class="sxs-lookup"><span data-stu-id="2b5ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5ef-109">*pDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b5ef-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5ef-110">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="2b5ef-111">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件代表前一個光線彈跳的3d 物件。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="2b5ef-112">此輸入緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="2b5ef-113">*AdaptiveThresh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b5ef-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5ef-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b5ef-115">用於細分網格頂點和臉部的 PRT 向量閾值。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="2b5ef-116">如果小於 1e-6f，則會指定值為 1e-6f 的預設值。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="2b5ef-117">*MinEdgeLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b5ef-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5ef-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b5ef-119">自動調整取樣中將產生的最小臉部邊長度。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="2b5ef-120">如果方法判斷該值太小，則會指定模型相依的值。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span>

</dd> <dt>

<span data-ttu-id="2b5ef-121">*MaxSubdiv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b5ef-121">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5ef-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b5ef-123">臉部的最大細分層級，將用於適應性取樣中。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-123">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="2b5ef-124">如果為零，則會指定預設值4。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-124">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="2b5ef-125">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2b5ef-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5ef-126">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="2b5ef-127">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會為地下分散的光線建立單一彈跳的模型。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="2b5ef-128">此輸出緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="2b5ef-129">*pDataTotal* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2b5ef-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5ef-130">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="2b5ef-131">選擇性 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件為所有先前 pDataOut 輸出的執行總和。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="2b5ef-132">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5ef-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b5ef-133">Return value</span></span>

<span data-ttu-id="2b5ef-134">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b5ef-135">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b5ef-136">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b5ef-137">備註</span><span class="sxs-lookup"><span data-stu-id="2b5ef-137">Remarks</span></span>

<span data-ttu-id="2b5ef-138">若要建立地下散佈的模型，請在呼叫 [**ID3DXPRTEngine：： ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) 方法之後，針對每個燈光彈跳呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-138">To model subsurface scattering, call this method for each light bounce after an [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) method is called.</span></span>

<span data-ttu-id="2b5ef-139">此方法的輸出不包含 >albedo，而且模擬器中只會整合連入的光線。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-139">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="2b5ef-140">藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-140">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="2b5ef-141">呼叫 [**ID3DXPRTEngine：： MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個 PRT 向量乘以 >albedo。</span><span class="sxs-lookup"><span data-stu-id="2b5ef-141">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b5ef-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b5ef-142">Requirements</span></span>



| <span data-ttu-id="2b5ef-143">需求</span><span class="sxs-lookup"><span data-stu-id="2b5ef-143">Requirement</span></span> | <span data-ttu-id="2b5ef-144">值</span><span class="sxs-lookup"><span data-stu-id="2b5ef-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b5ef-145">標頭</span><span class="sxs-lookup"><span data-stu-id="2b5ef-145">Header</span></span><br/>  | <dl> <span data-ttu-id="2b5ef-146"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b5ef-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2b5ef-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b5ef-147">Library</span></span><br/> | <dl> <span data-ttu-id="2b5ef-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b5ef-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b5ef-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b5ef-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5ef-150">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="2b5ef-150">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="2b5ef-151">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-151">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> <dt>

[<span data-ttu-id="2b5ef-152">**ID3DXPRTEngine::ComputeSS**</span><span class="sxs-lookup"><span data-stu-id="2b5ef-152">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 
