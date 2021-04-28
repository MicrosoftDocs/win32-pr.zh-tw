---
description: D3DXComputeBoundingSphere 函式 (D3DX9Mesh) -計算網格的周框球體。
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: 'D3DXComputeBoundingSphere 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115816"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="df31c-103">D3DXComputeBoundingSphere 函式 (D3DX9Mesh) </span><span class="sxs-lookup"><span data-stu-id="df31c-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="df31c-104">計算網格的周框球體。</span><span class="sxs-lookup"><span data-stu-id="df31c-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="df31c-105">語法</span><span class="sxs-lookup"><span data-stu-id="df31c-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="df31c-106">參數</span><span class="sxs-lookup"><span data-stu-id="df31c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df31c-107">*pFirstPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df31c-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df31c-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="df31c-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="df31c-109">第一個位置的指標。</span><span class="sxs-lookup"><span data-stu-id="df31c-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="df31c-110">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df31c-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df31c-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df31c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df31c-112">頂點數目。</span><span class="sxs-lookup"><span data-stu-id="df31c-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="df31c-113">*dwStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df31c-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df31c-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df31c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df31c-115">位置向量之間的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="df31c-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="df31c-116">使用 [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md)、 [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)或 [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) 來取得頂點跨距。</span><span class="sxs-lookup"><span data-stu-id="df31c-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="df31c-117">*pCenter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df31c-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df31c-118">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="df31c-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="df31c-119">[**D3DXVECTOR3**](d3dxvector3.md) 結構，定義傳回之周框球體的座標中心。</span><span class="sxs-lookup"><span data-stu-id="df31c-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="df31c-120">*pRadius* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df31c-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df31c-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="df31c-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df31c-122">傳回之周框球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="df31c-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df31c-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="df31c-123">Return value</span></span>

<span data-ttu-id="df31c-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df31c-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df31c-125">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="df31c-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df31c-126">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="df31c-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="df31c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="df31c-127">Requirements</span></span>



| <span data-ttu-id="df31c-128">需求</span><span class="sxs-lookup"><span data-stu-id="df31c-128">Requirement</span></span> | <span data-ttu-id="df31c-129">值</span><span class="sxs-lookup"><span data-stu-id="df31c-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df31c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="df31c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="df31c-131"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="df31c-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="df31c-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="df31c-132">Library</span></span><br/> | <dl> <span data-ttu-id="df31c-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="df31c-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df31c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df31c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df31c-135">網格函數</span><span class="sxs-lookup"><span data-stu-id="df31c-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
