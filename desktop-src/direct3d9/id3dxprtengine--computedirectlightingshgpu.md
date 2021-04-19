---
description: 使用 GPU 來計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。 計算 GPU 的照明通常會比 CPU 更快。
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine：： ComputeDirectLightingSHGPU 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974898"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a><span data-ttu-id="968b0-104">ID3DXPRTEngine：： ComputeDirectLightingSHGPU 方法</span><span class="sxs-lookup"><span data-stu-id="968b0-104">ID3DXPRTEngine::ComputeDirectLightingSHGPU method</span></span>

<span data-ttu-id="968b0-105">使用 GPU 來計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。</span><span class="sxs-lookup"><span data-stu-id="968b0-105">Uses the GPU to compute the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span> <span data-ttu-id="968b0-106">計算 GPU 的照明通常會比 CPU 更快。</span><span class="sxs-lookup"><span data-stu-id="968b0-106">Computing the lighting on the GPU will generally be much faster than on the CPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="968b0-107">語法</span><span class="sxs-lookup"><span data-stu-id="968b0-107">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="968b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="968b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="968b0-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="968b0-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="968b0-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="968b0-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="968b0-111">用來在 GPU 上執行模擬之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 裝置物件的指標。</span><span class="sxs-lookup"><span data-stu-id="968b0-111">Pointer to the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used to run the simulation on the GPU.</span></span> <span data-ttu-id="968b0-112">裝置必須支援 [ps \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) 圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="968b0-112">The device must support [ps\_2\_0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel shaders.</span></span>

> [!Note]  
> <span data-ttu-id="968b0-113">回呼函式不應使用 GPU 模擬器所使用的 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="968b0-113">Callback functions should not use the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used by the GPU simulator.</span></span>

 

</dd> <dt>

<span data-ttu-id="968b0-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="968b0-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="968b0-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="968b0-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="968b0-116">定義陰影 z 緩衝區解析度的 GPU 模擬參數。</span><span class="sxs-lookup"><span data-stu-id="968b0-116">GPU simulation parameter that defines the resolution of the shadow z-buffer.</span></span> <span data-ttu-id="968b0-117">應設定為 [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md)中的其中一個常數值。</span><span class="sxs-lookup"><span data-stu-id="968b0-117">Should be set to one of the constant values from [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span></span> <span data-ttu-id="968b0-118">若要指定更高的精確度模擬，D3DXSHGPUSIMOPT \_ HIGHQUALITY 值可以與其中一個 D3DXSHGPUSIMOPT \_ SHADOWRESxxx 值結合。</span><span class="sxs-lookup"><span data-stu-id="968b0-118">To specifiy higher precision simulation, the D3DXSHGPUSIMOPT\_HIGHQUALITY value may be combined with one of the D3DXSHGPUSIMOPT\_SHADOWRESxxx values.</span></span>

</dd> <dt>

<span data-ttu-id="968b0-119">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="968b0-119">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="968b0-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="968b0-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="968b0-121">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="968b0-121">Order of the SH evaluation.</span></span> <span data-ttu-id="968b0-122">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="968b0-122">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="968b0-123">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="968b0-123">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="968b0-124">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="968b0-124">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="968b0-125">*ZBias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="968b0-125">*ZBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="968b0-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="968b0-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="968b0-127">正常方向的偏差。</span><span class="sxs-lookup"><span data-stu-id="968b0-127">Bias in the normal direction.</span></span>

</dd> <dt>

<span data-ttu-id="968b0-128">*ZAngleBias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="968b0-128">*ZAngleBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="968b0-129">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="968b0-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="968b0-130">一般方向的偏差，以淺光線乘以角度的余弦值減一。</span><span class="sxs-lookup"><span data-stu-id="968b0-130">Bias in the normal direction, scaled by one minus the cosine of the angle with the light ray.</span></span>

</dd> <dt>

<span data-ttu-id="968b0-131">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="968b0-131">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="968b0-132">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="968b0-132">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="968b0-133">[**ID3DXPRTBuffer**](id3dxprtbuffer.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="968b0-133">Pointer to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="968b0-134">這個緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="968b0-134">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="968b0-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="968b0-135">Return value</span></span>

<span data-ttu-id="968b0-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="968b0-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="968b0-137">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="968b0-137">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="968b0-138">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="968b0-138">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="968b0-139">備註</span><span class="sxs-lookup"><span data-stu-id="968b0-139">Remarks</span></span>

<span data-ttu-id="968b0-140">在這個方法中，>albedo 不會乘以淺信號，而且模擬器中只會整合連入的光線。</span><span class="sxs-lookup"><span data-stu-id="968b0-140">In this method, the albedo is not multiplied by the light signal, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="968b0-141">藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="968b0-141">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="968b0-142">呼叫 [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個預先計算 radiance 傳輸 (PRT) 向量乘以 >albedo。</span><span class="sxs-lookup"><span data-stu-id="968b0-142">Call [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="968b0-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="968b0-143">Requirements</span></span>



| <span data-ttu-id="968b0-144">需求</span><span class="sxs-lookup"><span data-stu-id="968b0-144">Requirement</span></span> | <span data-ttu-id="968b0-145">值</span><span class="sxs-lookup"><span data-stu-id="968b0-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="968b0-146">標頭</span><span class="sxs-lookup"><span data-stu-id="968b0-146">Header</span></span><br/>  | <dl> <span data-ttu-id="968b0-147"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="968b0-147"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="968b0-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="968b0-148">Library</span></span><br/> | <dl> <span data-ttu-id="968b0-149"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="968b0-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="968b0-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="968b0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968b0-151">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="968b0-151">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
