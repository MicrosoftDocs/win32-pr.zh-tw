---
description: 調整所有與指定 submesh 相關聯的範例。 方法適用于計算地下散佈。
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'ID3DXPRTEngine：： ScaleMeshChunk 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986541"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a><span data-ttu-id="b6823-104">ID3DXPRTEngine：： ScaleMeshChunk 方法</span><span class="sxs-lookup"><span data-stu-id="b6823-104">ID3DXPRTEngine::ScaleMeshChunk method</span></span>

<span data-ttu-id="b6823-105">調整所有與指定 submesh 相關聯的範例。</span><span class="sxs-lookup"><span data-stu-id="b6823-105">Scales all the samples associated with a given submesh.</span></span> <span data-ttu-id="b6823-106">方法適用于計算地下散佈。</span><span class="sxs-lookup"><span data-stu-id="b6823-106">The method is useful for computing subsurface scattering.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6823-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6823-107">Syntax</span></span>


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="b6823-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6823-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6823-109">*uMeshChunk* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6823-109">*uMeshChunk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6823-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6823-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6823-111">在網格中開始調整範例的位置。</span><span class="sxs-lookup"><span data-stu-id="b6823-111">Location in the mesh at which to start scaling samples.</span></span>

</dd> <dt>

<span data-ttu-id="b6823-112">*fScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6823-112">*fScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6823-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6823-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6823-114">用來將 submesh 中的每個向量相乘的值。</span><span class="sxs-lookup"><span data-stu-id="b6823-114">Value by which to multiply each vector in the submesh.</span></span>

</dd> <dt>

<span data-ttu-id="b6823-115">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b6823-115">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6823-116">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b6823-116">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b6823-117">[**ID3DXPRTBuffer**](id3dxprtbuffer.md)物件的指標，用來接收 submesh 中的重新調整範例。</span><span class="sxs-lookup"><span data-stu-id="b6823-117">Pointer to a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object to receive rescaled samples in the submesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6823-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6823-118">Return value</span></span>

<span data-ttu-id="b6823-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6823-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6823-120">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b6823-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b6823-121">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b6823-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6823-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6823-122">Requirements</span></span>



| <span data-ttu-id="b6823-123">需求</span><span class="sxs-lookup"><span data-stu-id="b6823-123">Requirement</span></span> | <span data-ttu-id="b6823-124">值</span><span class="sxs-lookup"><span data-stu-id="b6823-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6823-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b6823-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b6823-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6823-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b6823-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6823-127">Library</span></span><br/> | <dl> <span data-ttu-id="b6823-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6823-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b6823-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6823-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6823-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b6823-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
