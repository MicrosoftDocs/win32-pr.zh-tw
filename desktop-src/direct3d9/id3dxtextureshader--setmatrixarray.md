---
description: 設定非轉換矩陣的陣列。
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: 'ID3DXTextureShader：： SetMatrixArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b0545d48e16698f44cc48ad467f9454ac94db030
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997400"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a><span data-ttu-id="72c27-103">ID3DXTextureShader：： SetMatrixArray 方法</span><span class="sxs-lookup"><span data-stu-id="72c27-103">ID3DXTextureShader::SetMatrixArray method</span></span>

<span data-ttu-id="72c27-104">設定非轉換矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="72c27-104">Sets an array of non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="72c27-105">語法</span><span class="sxs-lookup"><span data-stu-id="72c27-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="72c27-106">參數</span><span class="sxs-lookup"><span data-stu-id="72c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72c27-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72c27-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72c27-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="72c27-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="72c27-109">常數矩陣陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="72c27-109">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="72c27-110">請參閱 [D3DXHANDLE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="72c27-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="72c27-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72c27-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72c27-112">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="72c27-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="72c27-113">非轉換矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="72c27-113">Array of non-transposed matrices.</span></span> <span data-ttu-id="72c27-114">請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="72c27-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="72c27-115">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72c27-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72c27-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72c27-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72c27-117">陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="72c27-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72c27-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="72c27-118">Return value</span></span>

<span data-ttu-id="72c27-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72c27-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72c27-120">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="72c27-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="72c27-121">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="72c27-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="72c27-122">備註</span><span class="sxs-lookup"><span data-stu-id="72c27-122">Remarks</span></span>

<span data-ttu-id="72c27-123">未轉換的矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。</span><span class="sxs-lookup"><span data-stu-id="72c27-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="72c27-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="72c27-124">Requirements</span></span>



| <span data-ttu-id="72c27-125">需求</span><span class="sxs-lookup"><span data-stu-id="72c27-125">Requirement</span></span> | <span data-ttu-id="72c27-126">值</span><span class="sxs-lookup"><span data-stu-id="72c27-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72c27-127">標頭</span><span class="sxs-lookup"><span data-stu-id="72c27-127">Header</span></span><br/>  | <dl> <span data-ttu-id="72c27-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="72c27-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="72c27-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="72c27-129">Library</span></span><br/> | <dl> <span data-ttu-id="72c27-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="72c27-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="72c27-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72c27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c27-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="72c27-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
