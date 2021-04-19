---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 ID3DXMesh 物件。
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer：： ExtractToMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981994"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a><span data-ttu-id="c9b91-103">ID3DXPRTCompBuffer：： ExtractToMesh 方法</span><span class="sxs-lookup"><span data-stu-id="c9b91-103">ID3DXPRTCompBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="c9b91-104">從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**ID3DXMesh**](id3dxmesh.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c9b91-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b91-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9b91-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="c9b91-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9b91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b91-107">*NumPCA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9b91-107">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b91-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9b91-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9b91-109">要從緩衝區中解壓縮的 PCA 係數數目。</span><span class="sxs-lookup"><span data-stu-id="c9b91-109">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c9b91-110">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="c9b91-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b91-111">類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="c9b91-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="c9b91-112">網格的頂點使用方式描述。</span><span class="sxs-lookup"><span data-stu-id="c9b91-112">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="c9b91-113">請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b91-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9b91-114">*UsageIndexStart* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9b91-114">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b91-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9b91-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9b91-116">開始將 PCA 係數的索引儲存在網格中。</span><span class="sxs-lookup"><span data-stu-id="c9b91-116">Starting index for PCA coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c9b91-117">*pScene* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9b91-117">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b91-118">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="c9b91-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="c9b91-119">[**ID3DXMesh**](id3dxmesh.md)網格物件的指標，該物件會儲存 PCA 係數。</span><span class="sxs-lookup"><span data-stu-id="c9b91-119">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b91-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9b91-120">Return value</span></span>

<span data-ttu-id="c9b91-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9b91-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9b91-122">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c9b91-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c9b91-123">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c9b91-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b91-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9b91-124">Requirements</span></span>



| <span data-ttu-id="c9b91-125">需求</span><span class="sxs-lookup"><span data-stu-id="c9b91-125">Requirement</span></span> | <span data-ttu-id="c9b91-126">值</span><span class="sxs-lookup"><span data-stu-id="c9b91-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b91-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c9b91-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c9b91-128"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b91-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c9b91-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9b91-129">Library</span></span><br/> | <dl> <span data-ttu-id="c9b91-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9b91-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c9b91-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9b91-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b91-132">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="c9b91-132">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
