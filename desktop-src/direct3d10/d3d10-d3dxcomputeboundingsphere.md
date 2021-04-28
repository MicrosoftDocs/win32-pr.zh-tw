---
description: D3DXComputeBoundingSphere 函式 (D3DX10math) -計算網格的周框球體。
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
ms.openlocfilehash: 0041d775b21d1af37bc51d6ec2f432e616b2abd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113296"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="d3b61-103">D3DXComputeBoundingSphere 函式 (D3DX10math) </span><span class="sxs-lookup"><span data-stu-id="d3b61-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="d3b61-104">計算網格的周框球體。</span><span class="sxs-lookup"><span data-stu-id="d3b61-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b61-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3b61-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="d3b61-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3b61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b61-107">*pFirstPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b61-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b61-108">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3b61-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3b61-109">第一個位置的指標。</span><span class="sxs-lookup"><span data-stu-id="d3b61-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="d3b61-110">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b61-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b61-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3b61-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3b61-112">頂點數目。</span><span class="sxs-lookup"><span data-stu-id="d3b61-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d3b61-113">*dwStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b61-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b61-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3b61-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3b61-115">位置向量之間的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d3b61-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="d3b61-116">*pCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b61-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b61-117">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3b61-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3b61-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) 結構，定義傳回之周框球體的座標中心。</span><span class="sxs-lookup"><span data-stu-id="d3b61-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="d3b61-119">*pRadius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3b61-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3b61-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3b61-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d3b61-121">傳回之周框球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="d3b61-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b61-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3b61-122">Return value</span></span>

<span data-ttu-id="d3b61-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3b61-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3b61-124">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d3b61-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d3b61-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d3b61-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b61-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3b61-126">Requirements</span></span>



| <span data-ttu-id="d3b61-127">需求</span><span class="sxs-lookup"><span data-stu-id="d3b61-127">Requirement</span></span> | <span data-ttu-id="d3b61-128">值</span><span class="sxs-lookup"><span data-stu-id="d3b61-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b61-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d3b61-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d3b61-130"><dt>D3DX10math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b61-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="d3b61-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3b61-131">Library</span></span><br/> | <dl> <span data-ttu-id="d3b61-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3b61-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3b61-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3b61-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b61-134">網格函數</span><span class="sxs-lookup"><span data-stu-id="d3b61-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
