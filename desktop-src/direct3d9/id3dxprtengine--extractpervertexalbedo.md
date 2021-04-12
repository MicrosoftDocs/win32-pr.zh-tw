---
description: 從網格複製每個頂點的 >albedo 值。
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'ID3DXPRTEngine：： ExtractPerVertexAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946232"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a><span data-ttu-id="4bb01-103">ID3DXPRTEngine：： ExtractPerVertexAlbedo 方法</span><span class="sxs-lookup"><span data-stu-id="4bb01-103">ID3DXPRTEngine::ExtractPerVertexAlbedo method</span></span>

<span data-ttu-id="4bb01-104">從網格複製每個頂點的 >albedo 值。</span><span class="sxs-lookup"><span data-stu-id="4bb01-104">Copies per-vertex albedo values from a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb01-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bb01-105">Syntax</span></span>


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a><span data-ttu-id="4bb01-106">參數</span><span class="sxs-lookup"><span data-stu-id="4bb01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bb01-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bb01-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb01-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="4bb01-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="4bb01-109">[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)中用來建立 [**ID3DXPRTEngine**](id3dxprtengine.md)物件之 [**ID3DXMesh**](id3dxmesh.md)網格物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4bb01-109">Pointer to the [**ID3DXMesh**](id3dxmesh.md) mesh object used in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to create the [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="4bb01-110">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="4bb01-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb01-111">類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="4bb01-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="4bb01-112">要從網格複製的頂點使用方式描述。</span><span class="sxs-lookup"><span data-stu-id="4bb01-112">Vertex usage descriptions to copy from the mesh.</span></span> <span data-ttu-id="4bb01-113">請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。</span><span class="sxs-lookup"><span data-stu-id="4bb01-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="4bb01-114">*NumChanIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bb01-114">*NumChanIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb01-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bb01-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bb01-116">要從網格複製的色彩頻道數目。</span><span class="sxs-lookup"><span data-stu-id="4bb01-116">Number of color channels to copy from the mesh.</span></span> <span data-ttu-id="4bb01-117">設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。</span><span class="sxs-lookup"><span data-stu-id="4bb01-117">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bb01-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bb01-118">Return value</span></span>

<span data-ttu-id="4bb01-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4bb01-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4bb01-120">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4bb01-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4bb01-121">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="4bb01-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb01-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bb01-122">Requirements</span></span>



| <span data-ttu-id="4bb01-123">需求</span><span class="sxs-lookup"><span data-stu-id="4bb01-123">Requirement</span></span> | <span data-ttu-id="4bb01-124">值</span><span class="sxs-lookup"><span data-stu-id="4bb01-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb01-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4bb01-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4bb01-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb01-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4bb01-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="4bb01-127">Library</span></span><br/> | <dl> <span data-ttu-id="4bb01-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bb01-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bb01-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bb01-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb01-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="4bb01-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
