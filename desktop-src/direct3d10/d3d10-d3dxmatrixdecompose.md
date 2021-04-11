---
description: 將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: 'D3DXMatrixDecompose 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196409"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="5b1b7-103">D3DXMatrixDecompose 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="5b1b7-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="5b1b7-104">將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。</span><span class="sxs-lookup"><span data-stu-id="5b1b7-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b1b7-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5b1b7-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b1b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1b7-107">*pOutScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b1b7-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1b7-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b1b7-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5b1b7-109">輸出 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標，其中包含沿著 x、y 和 Z 軸套用的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="5b1b7-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="5b1b7-110">*pOutRotation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b1b7-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1b7-111">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b1b7-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5b1b7-112">描述旋轉之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="5b1b7-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="5b1b7-113">*pOutTranslation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b1b7-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1b7-114">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b1b7-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5b1b7-115">描述轉譯的 D3DXVECTOR3 向量指標。</span><span class="sxs-lookup"><span data-stu-id="5b1b7-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="5b1b7-116">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b1b7-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b1b7-117">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5b1b7-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5b1b7-118">要分解之輸入 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="5b1b7-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1b7-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b1b7-119">Return value</span></span>

<span data-ttu-id="5b1b7-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b1b7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b1b7-121">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5b1b7-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5b1b7-122">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5b1b7-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1b7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b1b7-123">Requirements</span></span>



| <span data-ttu-id="5b1b7-124">需求</span><span class="sxs-lookup"><span data-stu-id="5b1b7-124">Requirement</span></span> | <span data-ttu-id="5b1b7-125">值</span><span class="sxs-lookup"><span data-stu-id="5b1b7-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1b7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5b1b7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5b1b7-127"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b1b7-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5b1b7-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b1b7-128">Library</span></span><br/> | <dl> <span data-ttu-id="5b1b7-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b1b7-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b1b7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b1b7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1b7-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="5b1b7-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
