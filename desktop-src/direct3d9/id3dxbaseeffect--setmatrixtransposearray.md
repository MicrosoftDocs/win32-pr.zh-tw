---
description: 設定已轉置矩陣的陣列。
ms.assetid: 5dc65424-b0cd-490d-900e-60b9f7536ace
title: 'ID3DXBaseEffect：： SetMatrixTransposeArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e646761435f75688fe652683281297ca2b8de99e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988199"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a><span data-ttu-id="7d743-103">ID3DXBaseEffect：： SetMatrixTransposeArray 方法</span><span class="sxs-lookup"><span data-stu-id="7d743-103">ID3DXBaseEffect::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="7d743-104">設定已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="7d743-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d743-105">語法</span><span class="sxs-lookup"><span data-stu-id="7d743-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="7d743-106">參數</span><span class="sxs-lookup"><span data-stu-id="7d743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d743-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d743-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d743-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7d743-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7d743-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d743-109">Unique identifier.</span></span> <span data-ttu-id="7d743-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="7d743-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d743-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d743-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d743-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d743-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7d743-113">已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="7d743-113">Array of transposed matrices.</span></span> <span data-ttu-id="7d743-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="7d743-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d743-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d743-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d743-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d743-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d743-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="7d743-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d743-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d743-118">Return value</span></span>

<span data-ttu-id="7d743-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d743-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d743-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7d743-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7d743-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="7d743-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d743-122">備註</span><span class="sxs-lookup"><span data-stu-id="7d743-122">Remarks</span></span>

<span data-ttu-id="7d743-123">已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。</span><span class="sxs-lookup"><span data-stu-id="7d743-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="7d743-124">如果目的地矩陣小於來源矩陣，則會忽略來源矩陣的其他元件。</span><span class="sxs-lookup"><span data-stu-id="7d743-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d743-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d743-125">Requirements</span></span>



| <span data-ttu-id="7d743-126">需求</span><span class="sxs-lookup"><span data-stu-id="7d743-126">Requirement</span></span> | <span data-ttu-id="7d743-127">值</span><span class="sxs-lookup"><span data-stu-id="7d743-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d743-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7d743-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7d743-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d743-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7d743-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d743-130">Library</span></span><br/> | <dl> <span data-ttu-id="7d743-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d743-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7d743-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d743-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d743-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7d743-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="7d743-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="7d743-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
