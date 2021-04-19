---
description: 將每個預先計算 radiance 傳輸 (PRT) 向量乘以每個頂點 >albedo。
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine：： MultiplyAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991491"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a><span data-ttu-id="85d0b-103">ID3DXPRTEngine：： MultiplyAlbedo 方法</span><span class="sxs-lookup"><span data-stu-id="85d0b-103">ID3DXPRTEngine::MultiplyAlbedo method</span></span>

<span data-ttu-id="85d0b-104">將每個預先計算 radiance 傳輸 (PRT) 向量乘以每個頂點 >albedo。</span><span class="sxs-lookup"><span data-stu-id="85d0b-104">Multiplies each precomputed radiance transfer (PRT) vector by the per-vertex albedo.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="85d0b-105">Syntax</span></span>


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="85d0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="85d0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d0b-107">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="85d0b-107">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d0b-108">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="85d0b-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="85d0b-109">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件將包含 PRT 向量乘以每個頂點 >albedo。</span><span class="sxs-lookup"><span data-stu-id="85d0b-109">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will contain PRT vectors multiplied by the per-vertex albedo.</span></span> <span data-ttu-id="85d0b-110">如果這個輸出緩衝區是材質物件，則必須小心將材質的 >albedo 儲存為模擬緩衝區的相同解析度。</span><span class="sxs-lookup"><span data-stu-id="85d0b-110">If this output buffer is a texture object, then care must be taken to store the albedo of the texture at the same resolution as the simulation buffer.</span></span> <span data-ttu-id="85d0b-111">您可以在具有 [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)的 >albedo 上設定適當的解決方式，並套用材質裝訂邊區域（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="85d0b-111">You can set the proper resolution on the albedo with [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applying texture gutter regions if appropriate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d0b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="85d0b-112">Return value</span></span>

<span data-ttu-id="85d0b-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85d0b-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85d0b-114">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="85d0b-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85d0b-115">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="85d0b-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d0b-116">備註</span><span class="sxs-lookup"><span data-stu-id="85d0b-116">Remarks</span></span>

<span data-ttu-id="85d0b-117">ID3DXPRTEngine：： Computexxx 方法會計算輸出緩衝區，其中燈的信號尚未乘以 >albedo。</span><span class="sxs-lookup"><span data-stu-id="85d0b-117">The ID3DXPRTEngine::Computexxx methods compute output buffers in which the light signal has not been multiplied by albedo.</span></span> <span data-ttu-id="85d0b-118">藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="85d0b-118">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="85d0b-119">若要在呈現的光線模型中包含 >albedo，請在其中一個 Computexxx 方法之後呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="85d0b-119">To include albedo in the rendered-light model, call this method after one of the Computexxx methods.</span></span>

<span data-ttu-id="85d0b-120">呼叫這個方法之前，應該先呼叫 [**ID3DXPRTEngine：： SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) 。</span><span class="sxs-lookup"><span data-stu-id="85d0b-120">[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) should be called before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d0b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="85d0b-121">Requirements</span></span>



| <span data-ttu-id="85d0b-122">需求</span><span class="sxs-lookup"><span data-stu-id="85d0b-122">Requirement</span></span> | <span data-ttu-id="85d0b-123">值</span><span class="sxs-lookup"><span data-stu-id="85d0b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85d0b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="85d0b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="85d0b-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="85d0b-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85d0b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="85d0b-126">Library</span></span><br/> | <dl> <span data-ttu-id="85d0b-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="85d0b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85d0b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85d0b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d0b-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="85d0b-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="85d0b-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="85d0b-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




