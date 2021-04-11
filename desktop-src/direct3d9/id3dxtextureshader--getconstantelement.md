---
description: 從常數資料表取得常數。
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'ID3DXTextureShader：： GetConstantElement 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196285"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a><span data-ttu-id="a5a78-103">ID3DXTextureShader：： GetConstantElement 方法</span><span class="sxs-lookup"><span data-stu-id="a5a78-103">ID3DXTextureShader::GetConstantElement method</span></span>

<span data-ttu-id="a5a78-104">從常數資料表取得常數。</span><span class="sxs-lookup"><span data-stu-id="a5a78-104">Get a constant from the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a78-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5a78-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="a5a78-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5a78-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5a78-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a78-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a5a78-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a5a78-109">常數陣列的 [控制碼](handles.md) 。</span><span class="sxs-lookup"><span data-stu-id="a5a78-109">A [handle](handles.md) to the array of constants.</span></span> <span data-ttu-id="a5a78-110">此值不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a5a78-110">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a5a78-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5a78-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a78-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5a78-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5a78-113">常數資料表中專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="a5a78-113">Zero-based index of the element in the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5a78-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5a78-114">Return value</span></span>

<span data-ttu-id="a5a78-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a5a78-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a5a78-116">傳回常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5a78-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5a78-117">備註</span><span class="sxs-lookup"><span data-stu-id="a5a78-117">Remarks</span></span>

<span data-ttu-id="a5a78-118">若要取得不屬於陣列的常數，請使用 [**ID3DXTextureShader：： GetConstant**](id3dxtextureshader--getconstant.md) 或 [**ID3DXTextureShader：： GetConstantByName**](id3dxtextureshader--getconstantbyname.md)。</span><span class="sxs-lookup"><span data-stu-id="a5a78-118">To get a constant that is not part of an array, use [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) or [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a78-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5a78-119">Requirements</span></span>



| <span data-ttu-id="a5a78-120">需求</span><span class="sxs-lookup"><span data-stu-id="a5a78-120">Requirement</span></span> | <span data-ttu-id="a5a78-121">值</span><span class="sxs-lookup"><span data-stu-id="a5a78-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a78-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a5a78-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a5a78-123"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5a78-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a5a78-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5a78-124">Library</span></span><br/> | <dl> <span data-ttu-id="a5a78-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5a78-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a5a78-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5a78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a78-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a5a78-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
