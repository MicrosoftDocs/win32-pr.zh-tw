---
description: 將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: 'D3DXMatrixDecompose 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986760"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="42fbf-103">D3DXMatrixDecompose 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="42fbf-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="42fbf-104">將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。</span><span class="sxs-lookup"><span data-stu-id="42fbf-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="42fbf-105">語法</span><span class="sxs-lookup"><span data-stu-id="42fbf-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="42fbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="42fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42fbf-107">*pOutScale* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="42fbf-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42fbf-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="42fbf-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="42fbf-109">輸出 [**D3DXVECTOR3**](d3dxvector3.md) 的指標，其中包含沿著 x、y 和 Z 軸套用的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="42fbf-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="42fbf-110">*pOutRotation* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="42fbf-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42fbf-111">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="42fbf-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="42fbf-112">描述旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="42fbf-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="42fbf-113">*pOutTranslation* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="42fbf-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42fbf-114">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="42fbf-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="42fbf-115">描述轉譯的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。</span><span class="sxs-lookup"><span data-stu-id="42fbf-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="42fbf-116">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42fbf-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fbf-117">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="42fbf-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="42fbf-118">要分解之輸入 [**D3DXMATRIX**](d3dxmatrix.md) 矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="42fbf-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42fbf-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="42fbf-119">Return value</span></span>

<span data-ttu-id="42fbf-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42fbf-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42fbf-121">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="42fbf-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="42fbf-122">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="42fbf-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="42fbf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="42fbf-123">Requirements</span></span>



| <span data-ttu-id="42fbf-124">需求</span><span class="sxs-lookup"><span data-stu-id="42fbf-124">Requirement</span></span> | <span data-ttu-id="42fbf-125">值</span><span class="sxs-lookup"><span data-stu-id="42fbf-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42fbf-126">標頭</span><span class="sxs-lookup"><span data-stu-id="42fbf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="42fbf-127"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="42fbf-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="42fbf-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="42fbf-128">Library</span></span><br/> | <dl> <span data-ttu-id="42fbf-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42fbf-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42fbf-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42fbf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fbf-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="42fbf-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




