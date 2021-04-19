---
description: 從單一通道緩衝區解壓縮係數資料，並將資料加入至 ID3DXMesh 物件。
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer：： ExtractToMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988222"
---
# <a name="id3dxprtbufferextracttomesh-method"></a><span data-ttu-id="32b32-103">ID3DXPRTBuffer：： ExtractToMesh 方法</span><span class="sxs-lookup"><span data-stu-id="32b32-103">ID3DXPRTBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="32b32-104">從單一通道緩衝區解壓縮係數資料，並將資料加入至 [**ID3DXMesh**](id3dxmesh.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="32b32-104">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b32-105">語法</span><span class="sxs-lookup"><span data-stu-id="32b32-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="32b32-106">參數</span><span class="sxs-lookup"><span data-stu-id="32b32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b32-107">*NumCoefficients* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32b32-107">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32b32-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32b32-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32b32-109">要從緩衝區中解壓縮的係數數目。</span><span class="sxs-lookup"><span data-stu-id="32b32-109">Number of coefficients to extract from the buffer.</span></span> <span data-ttu-id="32b32-110">使用球面調和 (SH) 預先計算 radiance transfer (PRT) 時，係數的數目應該是 Order ²。</span><span class="sxs-lookup"><span data-stu-id="32b32-110">When using spherical harmonic (SH) precomputed radiance transfer (PRT), the number of coefficients should be Order ².</span></span> <span data-ttu-id="32b32-111">順序必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="32b32-111">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="32b32-112">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="32b32-112">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32b32-113">類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="32b32-113">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="32b32-114">網格的頂點使用方式描述。</span><span class="sxs-lookup"><span data-stu-id="32b32-114">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="32b32-115">請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。</span><span class="sxs-lookup"><span data-stu-id="32b32-115">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="32b32-116">*UsageIndexStart* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32b32-116">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32b32-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32b32-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32b32-118">開始要儲存在網格中之係數的索引。</span><span class="sxs-lookup"><span data-stu-id="32b32-118">Starting index for coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="32b32-119">*pScene* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32b32-119">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32b32-120">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="32b32-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="32b32-121">[**ID3DXMesh**](id3dxmesh.md)網格物件的指標，該物件會儲存係數。</span><span class="sxs-lookup"><span data-stu-id="32b32-121">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b32-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="32b32-122">Return value</span></span>

<span data-ttu-id="32b32-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32b32-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32b32-124">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="32b32-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="32b32-125">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="32b32-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b32-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="32b32-126">Requirements</span></span>



| <span data-ttu-id="32b32-127">需求</span><span class="sxs-lookup"><span data-stu-id="32b32-127">Requirement</span></span> | <span data-ttu-id="32b32-128">值</span><span class="sxs-lookup"><span data-stu-id="32b32-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32b32-129">標頭</span><span class="sxs-lookup"><span data-stu-id="32b32-129">Header</span></span><br/>  | <dl> <span data-ttu-id="32b32-130"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="32b32-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="32b32-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="32b32-131">Library</span></span><br/> | <dl> <span data-ttu-id="32b32-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="32b32-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32b32-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32b32-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b32-134">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="32b32-134">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
