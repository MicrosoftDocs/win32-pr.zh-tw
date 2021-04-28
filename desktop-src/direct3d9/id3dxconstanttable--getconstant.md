---
description: ID3DXConstantTable：： GetConstant 方法-藉由查閱索引來取得常數。
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'ID3DXConstantTable：： GetConstant 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 664a1b1a214b49eb731a3a0766a255e5f5acadd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115266"
---
# <a name="id3dxconstanttablegetconstant-method"></a><span data-ttu-id="c56c9-103">ID3DXConstantTable：： GetConstant 方法</span><span class="sxs-lookup"><span data-stu-id="c56c9-103">ID3DXConstantTable::GetConstant method</span></span>

<span data-ttu-id="c56c9-104">藉由查閱索引來取得常數。</span><span class="sxs-lookup"><span data-stu-id="c56c9-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="c56c9-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="c56c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="c56c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c56c9-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c56c9-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56c9-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c56c9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c56c9-109">父資料結構的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c56c9-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="c56c9-110">如果常數是最上層參數 (沒有任何父資料結構) ，請使用 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c56c9-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c56c9-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c56c9-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56c9-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c56c9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c56c9-113">常數以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="c56c9-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c56c9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c56c9-114">Return value</span></span>

<span data-ttu-id="c56c9-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c56c9-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c56c9-116">傳回常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c56c9-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="c56c9-117">備註</span><span class="sxs-lookup"><span data-stu-id="c56c9-117">Remarks</span></span>

<span data-ttu-id="c56c9-118">若要從常數陣列取得常數，請使用 [**ID3DXConstantTable：： GetConstantElement**](id3dxconstanttable--getconstantelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c56c9-118">To get a constant from an array of constants, use [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c56c9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c56c9-119">Requirements</span></span>



| <span data-ttu-id="c56c9-120">需求</span><span class="sxs-lookup"><span data-stu-id="c56c9-120">Requirement</span></span> | <span data-ttu-id="c56c9-121">值</span><span class="sxs-lookup"><span data-stu-id="c56c9-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56c9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c56c9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c56c9-123"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="c56c9-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c56c9-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="c56c9-124">Library</span></span><br/> | <dl> <span data-ttu-id="c56c9-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c56c9-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c56c9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c56c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56c9-127">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="c56c9-127">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
