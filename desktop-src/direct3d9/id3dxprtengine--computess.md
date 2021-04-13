---
description: 使用 ID3DXPRTEngine：： SetMeshMaterials 設定的材質屬性，計算地下散佈所產生的來源 radiance。 這個方法僅適用于網格物件中每個頂點定義的材質。
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'ID3DXPRTEngine：： ComputeSS 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323403"
---
# <a name="id3dxprtenginecomputess-method"></a><span data-ttu-id="bebc2-104">ID3DXPRTEngine：： ComputeSS 方法</span><span class="sxs-lookup"><span data-stu-id="bebc2-104">ID3DXPRTEngine::ComputeSS method</span></span>

<span data-ttu-id="bebc2-105">使用 [**ID3DXPRTEngine：： SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)設定的材質屬性，計算地下散佈所產生的來源 radiance。</span><span class="sxs-lookup"><span data-stu-id="bebc2-105">Computes the source radiance resulting from subsurface scattering, using material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="bebc2-106">這個方法僅適用于網格物件中每個頂點定義的材質。</span><span class="sxs-lookup"><span data-stu-id="bebc2-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebc2-107">語法</span><span class="sxs-lookup"><span data-stu-id="bebc2-107">Syntax</span></span>


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="bebc2-108">參數</span><span class="sxs-lookup"><span data-stu-id="bebc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bebc2-109">*pDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bebc2-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bebc2-110">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bebc2-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bebc2-111">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件代表前一個光線彈跳的3d 物件。</span><span class="sxs-lookup"><span data-stu-id="bebc2-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="bebc2-112">此輸入緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="bebc2-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="bebc2-113">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bebc2-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bebc2-114">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bebc2-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bebc2-115">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會為地下分散的光線建立單一彈跳的模型。</span><span class="sxs-lookup"><span data-stu-id="bebc2-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="bebc2-116">此輸出緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="bebc2-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="bebc2-117">*pDataTotal* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bebc2-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bebc2-118">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bebc2-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bebc2-119">選擇性 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件為所有先前 pDataOut 輸出的執行總和。</span><span class="sxs-lookup"><span data-stu-id="bebc2-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="bebc2-120">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bebc2-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bebc2-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="bebc2-121">Return value</span></span>

<span data-ttu-id="bebc2-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bebc2-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bebc2-123">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="bebc2-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bebc2-124">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="bebc2-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bebc2-125">備註</span><span class="sxs-lookup"><span data-stu-id="bebc2-125">Remarks</span></span>

<span data-ttu-id="bebc2-126">若要建立地下散佈的模型，請在呼叫 ID3DXPRTEngine：： ComputeDirectLighting 方法之後，針對每個燈光彈跳呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="bebc2-126">To model subsurface scattering, call this method for each light bounce after an ID3DXPRTEngine::ComputeDirectLighting method is called.</span></span>

<span data-ttu-id="bebc2-127">使用下列呼叫順序來建立地下散佈模型。</span><span class="sxs-lookup"><span data-stu-id="bebc2-127">Use the following calling sequence to model subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



<span data-ttu-id="bebc2-128">此方法的輸出不包含 >albedo，而且模擬器中只會整合連入的光線。</span><span class="sxs-lookup"><span data-stu-id="bebc2-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="bebc2-129">藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="bebc2-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="bebc2-130">呼叫 [**ID3DXPRTEngine：： MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個預先計算 radiance 傳輸 (PRT) vector 乘以 >albedo。</span><span class="sxs-lookup"><span data-stu-id="bebc2-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="bebc2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bebc2-131">Requirements</span></span>



| <span data-ttu-id="bebc2-132">需求</span><span class="sxs-lookup"><span data-stu-id="bebc2-132">Requirement</span></span> | <span data-ttu-id="bebc2-133">值</span><span class="sxs-lookup"><span data-stu-id="bebc2-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bebc2-134">標頭</span><span class="sxs-lookup"><span data-stu-id="bebc2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="bebc2-135"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="bebc2-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bebc2-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="bebc2-136">Library</span></span><br/> | <dl> <span data-ttu-id="bebc2-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bebc2-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bebc2-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bebc2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebc2-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="bebc2-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="bebc2-140">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="bebc2-140">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




