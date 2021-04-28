---
description: ID3DXTextureShader：： GetConstant 方法-藉由查閱索引來取得常數。
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: 'ID3DXTextureShader：： GetConstant 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117666"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="78782-103">ID3DXTextureShader：： GetConstant 方法</span><span class="sxs-lookup"><span data-stu-id="78782-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="78782-104">藉由查閱索引來取得常數。</span><span class="sxs-lookup"><span data-stu-id="78782-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="78782-105">語法</span><span class="sxs-lookup"><span data-stu-id="78782-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="78782-106">參數</span><span class="sxs-lookup"><span data-stu-id="78782-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78782-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78782-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78782-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="78782-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="78782-109">父資料結構的 [控制碼](handles.md) 。</span><span class="sxs-lookup"><span data-stu-id="78782-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="78782-110">如果常數是最上層參數 (沒有任何父資料結構) ，請使用 **Null**。</span><span class="sxs-lookup"><span data-stu-id="78782-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="78782-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78782-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78782-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78782-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78782-113">常數以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="78782-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78782-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="78782-114">Return value</span></span>

<span data-ttu-id="78782-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="78782-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="78782-116">傳回常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="78782-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="78782-117">備註</span><span class="sxs-lookup"><span data-stu-id="78782-117">Remarks</span></span>

<span data-ttu-id="78782-118">若要從常數陣列取得常數，請使用 [**ID3DXTextureShader：： GetConstantElement**](id3dxtextureshader--getconstantelement.md)。</span><span class="sxs-lookup"><span data-stu-id="78782-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78782-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="78782-119">Requirements</span></span>



| <span data-ttu-id="78782-120">需求</span><span class="sxs-lookup"><span data-stu-id="78782-120">Requirement</span></span> | <span data-ttu-id="78782-121">值</span><span class="sxs-lookup"><span data-stu-id="78782-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="78782-122">標頭</span><span class="sxs-lookup"><span data-stu-id="78782-122">Header</span></span><br/>  | <dl> <span data-ttu-id="78782-123"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="78782-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="78782-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="78782-124">Library</span></span><br/> | <dl> <span data-ttu-id="78782-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="78782-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="78782-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78782-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78782-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="78782-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
