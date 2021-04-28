---
description: ID3DXTextureShader：： SetMatrixTransposeArray 方法-設定已轉置矩陣的陣列。
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: 'ID3DXTextureShader：： SetMatrixTransposeArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663f49f600c000ff37974c8ecd4da56ba59630d1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090206"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="40ebe-103">ID3DXTextureShader：： SetMatrixTransposeArray 方法</span><span class="sxs-lookup"><span data-stu-id="40ebe-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="40ebe-104">設定已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="40ebe-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ebe-105">語法</span><span class="sxs-lookup"><span data-stu-id="40ebe-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="40ebe-106">參數</span><span class="sxs-lookup"><span data-stu-id="40ebe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ebe-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40ebe-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ebe-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="40ebe-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="40ebe-109">矩陣常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="40ebe-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="40ebe-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="40ebe-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ebe-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40ebe-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ebe-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="40ebe-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="40ebe-113">已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="40ebe-113">Array of transposed matrices.</span></span> <span data-ttu-id="40ebe-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="40ebe-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="40ebe-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40ebe-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ebe-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40ebe-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40ebe-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="40ebe-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ebe-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="40ebe-118">Return value</span></span>

<span data-ttu-id="40ebe-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40ebe-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40ebe-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="40ebe-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="40ebe-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="40ebe-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="40ebe-122">備註</span><span class="sxs-lookup"><span data-stu-id="40ebe-122">Remarks</span></span>

<span data-ttu-id="40ebe-123">已轉換的矩陣包含資料行主要資料;也就是說，每個向量都包含在資料行中。</span><span class="sxs-lookup"><span data-stu-id="40ebe-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ebe-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="40ebe-124">Requirements</span></span>



| <span data-ttu-id="40ebe-125">需求</span><span class="sxs-lookup"><span data-stu-id="40ebe-125">Requirement</span></span> | <span data-ttu-id="40ebe-126">值</span><span class="sxs-lookup"><span data-stu-id="40ebe-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ebe-127">標頭</span><span class="sxs-lookup"><span data-stu-id="40ebe-127">Header</span></span><br/>  | <dl> <span data-ttu-id="40ebe-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="40ebe-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="40ebe-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="40ebe-129">Library</span></span><br/> | <dl> <span data-ttu-id="40ebe-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="40ebe-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="40ebe-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40ebe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ebe-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="40ebe-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
