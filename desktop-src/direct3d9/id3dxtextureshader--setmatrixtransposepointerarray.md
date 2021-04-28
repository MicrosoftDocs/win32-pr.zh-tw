---
description: ID3DXTextureShader：： SetMatrixTransposePointerArray 方法-將指標陣列設定為已轉換的矩陣。
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'ID3DXTextureShader：： SetMatrixTransposePointerArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 46e04c8c86bd0cdf7acea44872d00ad19f620ee6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090146"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="2c272-103">ID3DXTextureShader：： SetMatrixTransposePointerArray 方法</span><span class="sxs-lookup"><span data-stu-id="2c272-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="2c272-104">將指標的陣列設定為已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="2c272-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c272-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c272-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2c272-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c272-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c272-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c272-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2c272-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2c272-109">矩陣常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c272-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="2c272-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="2c272-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c272-111">*ppMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c272-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c272-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="2c272-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="2c272-113">已轉置矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="2c272-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="2c272-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="2c272-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c272-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c272-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c272-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c272-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c272-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="2c272-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c272-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c272-118">Return value</span></span>

<span data-ttu-id="2c272-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c272-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c272-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2c272-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2c272-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2c272-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c272-122">備註</span><span class="sxs-lookup"><span data-stu-id="2c272-122">Remarks</span></span>

<span data-ttu-id="2c272-123">已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。</span><span class="sxs-lookup"><span data-stu-id="2c272-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c272-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c272-124">Requirements</span></span>



| <span data-ttu-id="2c272-125">需求</span><span class="sxs-lookup"><span data-stu-id="2c272-125">Requirement</span></span> | <span data-ttu-id="2c272-126">值</span><span class="sxs-lookup"><span data-stu-id="2c272-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c272-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2c272-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2c272-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c272-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2c272-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c272-129">Library</span></span><br/> | <dl> <span data-ttu-id="2c272-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c272-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2c272-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c272-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c272-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2c272-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
