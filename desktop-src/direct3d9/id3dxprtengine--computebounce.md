---
description: 計算 interreflected 燈的單一彈跳所產生的來源 radiance。 此方法可用於任何照明的場景，包括球面調和 (SH) 為基礎的預先計算 radiance 傳輸 (PRT) 模型。
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'ID3DXPRTEngine：： ComputeBounce 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323259"
---
# <a name="id3dxprtenginecomputebounce-method"></a><span data-ttu-id="ccd52-104">ID3DXPRTEngine：： ComputeBounce 方法</span><span class="sxs-lookup"><span data-stu-id="ccd52-104">ID3DXPRTEngine::ComputeBounce method</span></span>

<span data-ttu-id="ccd52-105">計算 interreflected 燈的單一彈跳所產生的來源 radiance。</span><span class="sxs-lookup"><span data-stu-id="ccd52-105">Computes the source radiance resulting from a single bounce of interreflected light.</span></span> <span data-ttu-id="ccd52-106">此方法可用於任何照明的場景，包括球面調和 (SH) 為基礎的預先計算 radiance 傳輸 (PRT) 模型。</span><span class="sxs-lookup"><span data-stu-id="ccd52-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based precomputed radiance transfer (PRT) model.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd52-107">語法</span><span class="sxs-lookup"><span data-stu-id="ccd52-107">Syntax</span></span>


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="ccd52-108">參數</span><span class="sxs-lookup"><span data-stu-id="ccd52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd52-109">*pDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccd52-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd52-110">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ccd52-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="ccd52-111">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件代表前一個光線彈跳的3d 物件。</span><span class="sxs-lookup"><span data-stu-id="ccd52-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="ccd52-112">此輸入緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="ccd52-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="ccd52-113">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ccd52-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd52-114">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ccd52-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="ccd52-115">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會將 interreflected 光線的單一彈跳進行模型。</span><span class="sxs-lookup"><span data-stu-id="ccd52-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the interreflected light.</span></span> <span data-ttu-id="ccd52-116">此輸出緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="ccd52-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="ccd52-117">*pDataTotal* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ccd52-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd52-118">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ccd52-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="ccd52-119">選擇性 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件為所有先前 pDataOut 輸出的執行總和。</span><span class="sxs-lookup"><span data-stu-id="ccd52-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="ccd52-120">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ccd52-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd52-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccd52-121">Return value</span></span>

<span data-ttu-id="ccd52-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccd52-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccd52-123">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ccd52-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ccd52-124">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ccd52-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccd52-125">備註</span><span class="sxs-lookup"><span data-stu-id="ccd52-125">Remarks</span></span>

<span data-ttu-id="ccd52-126">您可以使用下列呼叫順序，以直接光源來建立多個光線彈跳的模型。</span><span class="sxs-lookup"><span data-stu-id="ccd52-126">Use the following calling sequence to model multiple light bounces with direct lighting.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



<span data-ttu-id="ccd52-127">使用下列呼叫順序來建立多個使用地下散佈的燈光彈跳模型。</span><span class="sxs-lookup"><span data-stu-id="ccd52-127">Use the following calling sequence to model multiple light bounces with subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



<span data-ttu-id="ccd52-128">此方法的輸出不包含 >albedo，而且模擬器中只會整合連入的光線。</span><span class="sxs-lookup"><span data-stu-id="ccd52-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="ccd52-129">藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="ccd52-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="ccd52-130">呼叫 [**ID3DXPRTEngine：： MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個 PRT 向量乘以 >albedo。</span><span class="sxs-lookup"><span data-stu-id="ccd52-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd52-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccd52-131">Requirements</span></span>



| <span data-ttu-id="ccd52-132">需求</span><span class="sxs-lookup"><span data-stu-id="ccd52-132">Requirement</span></span> | <span data-ttu-id="ccd52-133">值</span><span class="sxs-lookup"><span data-stu-id="ccd52-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd52-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ccd52-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ccd52-135"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd52-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ccd52-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="ccd52-136">Library</span></span><br/> | <dl> <span data-ttu-id="ccd52-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccd52-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ccd52-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccd52-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd52-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="ccd52-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="ccd52-140">**ID3DXPRTEngine::ComputeSS**</span><span class="sxs-lookup"><span data-stu-id="ccd52-140">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 




