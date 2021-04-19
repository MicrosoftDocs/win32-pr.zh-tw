---
description: 藉由查閱索引來取得常數。
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
ms.openlocfilehash: 24f3f78d5970d5e3beda119ca40a565f45d0d950
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992740"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="af67e-103">ID3DXTextureShader：： GetConstant 方法</span><span class="sxs-lookup"><span data-stu-id="af67e-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="af67e-104">藉由查閱索引來取得常數。</span><span class="sxs-lookup"><span data-stu-id="af67e-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="af67e-105">語法</span><span class="sxs-lookup"><span data-stu-id="af67e-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="af67e-106">參數</span><span class="sxs-lookup"><span data-stu-id="af67e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af67e-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af67e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af67e-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="af67e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="af67e-109">父資料結構的 [控制碼](handles.md) 。</span><span class="sxs-lookup"><span data-stu-id="af67e-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="af67e-110">如果常數是最上層參數 (沒有任何父資料結構) ，請使用 **Null**。</span><span class="sxs-lookup"><span data-stu-id="af67e-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="af67e-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af67e-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af67e-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af67e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af67e-113">常數以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="af67e-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af67e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="af67e-114">Return value</span></span>

<span data-ttu-id="af67e-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="af67e-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="af67e-116">傳回常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="af67e-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="af67e-117">備註</span><span class="sxs-lookup"><span data-stu-id="af67e-117">Remarks</span></span>

<span data-ttu-id="af67e-118">若要從常數陣列取得常數，請使用 [**ID3DXTextureShader：： GetConstantElement**](id3dxtextureshader--getconstantelement.md)。</span><span class="sxs-lookup"><span data-stu-id="af67e-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af67e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="af67e-119">Requirements</span></span>



| <span data-ttu-id="af67e-120">需求</span><span class="sxs-lookup"><span data-stu-id="af67e-120">Requirement</span></span> | <span data-ttu-id="af67e-121">值</span><span class="sxs-lookup"><span data-stu-id="af67e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af67e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="af67e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="af67e-123"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="af67e-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="af67e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="af67e-124">Library</span></span><br/> | <dl> <span data-ttu-id="af67e-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="af67e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="af67e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af67e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af67e-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="af67e-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
