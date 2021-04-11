---
description: 計算網格的周框球體。
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: 'D3DXComputeBoundingSphere 函式 (D3DX10math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c8e59b4d39652d02ce19f4c1bf6b0617fee7772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196382"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="7df84-103">D3DXComputeBoundingSphere 函式 (D3DX10math) </span><span class="sxs-lookup"><span data-stu-id="7df84-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="7df84-104">計算網格的周框球體。</span><span class="sxs-lookup"><span data-stu-id="7df84-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df84-105">語法</span><span class="sxs-lookup"><span data-stu-id="7df84-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="7df84-106">參數</span><span class="sxs-lookup"><span data-stu-id="7df84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df84-107">*pFirstPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7df84-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df84-108">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7df84-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7df84-109">第一個位置的指標。</span><span class="sxs-lookup"><span data-stu-id="7df84-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="7df84-110">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7df84-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df84-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7df84-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7df84-112">頂點數目。</span><span class="sxs-lookup"><span data-stu-id="7df84-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="7df84-113">*dwStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7df84-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df84-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7df84-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7df84-115">位置向量之間的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="7df84-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="7df84-116">*pCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7df84-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df84-117">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7df84-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7df84-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) 結構，定義傳回之周框球體的座標中心。</span><span class="sxs-lookup"><span data-stu-id="7df84-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="7df84-119">*pRadius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7df84-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df84-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7df84-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7df84-121">傳回之周框球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="7df84-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df84-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="7df84-122">Return value</span></span>

<span data-ttu-id="7df84-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7df84-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7df84-124">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7df84-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7df84-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="7df84-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df84-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="7df84-126">Requirements</span></span>



| <span data-ttu-id="7df84-127">需求</span><span class="sxs-lookup"><span data-stu-id="7df84-127">Requirement</span></span> | <span data-ttu-id="7df84-128">值</span><span class="sxs-lookup"><span data-stu-id="7df84-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7df84-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7df84-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7df84-130"><dt>D3DX10math。h</dt></span><span class="sxs-lookup"><span data-stu-id="7df84-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="7df84-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="7df84-131">Library</span></span><br/> | <dl> <span data-ttu-id="7df84-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7df84-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7df84-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7df84-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df84-134">網格函數</span><span class="sxs-lookup"><span data-stu-id="7df84-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
