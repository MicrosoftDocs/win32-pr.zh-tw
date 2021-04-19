---
description: 從常數的陣列取得常數。 陣列是由元素所組成。
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'ID3DXConstantTable：： GetConstantElement 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991471"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a><span data-ttu-id="60550-104">ID3DXConstantTable：： GetConstantElement 方法</span><span class="sxs-lookup"><span data-stu-id="60550-104">ID3DXConstantTable::GetConstantElement method</span></span>

<span data-ttu-id="60550-105">從常數的陣列取得常數。</span><span class="sxs-lookup"><span data-stu-id="60550-105">Gets a constant from an array of constants.</span></span> <span data-ttu-id="60550-106">陣列是由元素所組成。</span><span class="sxs-lookup"><span data-stu-id="60550-106">An array is made up of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="60550-107">語法</span><span class="sxs-lookup"><span data-stu-id="60550-107">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="60550-108">參數</span><span class="sxs-lookup"><span data-stu-id="60550-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60550-109">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60550-109">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60550-110">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="60550-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="60550-111">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="60550-111">Unique identifier to the array of constants.</span></span> <span data-ttu-id="60550-112">此值不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="60550-112">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="60550-113">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60550-113">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60550-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60550-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60550-115">陣列中元素之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="60550-115">Zero-based index of the element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60550-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="60550-116">Return value</span></span>

<span data-ttu-id="60550-117">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="60550-117">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="60550-118">傳回元素常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="60550-118">Returns a unique identifier to the element constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="60550-119">備註</span><span class="sxs-lookup"><span data-stu-id="60550-119">Remarks</span></span>

<span data-ttu-id="60550-120">若要取得不屬於陣列的常數，請使用 [**ID3DXConstantTable：： GetConstant**](id3dxconstanttable--getconstant.md) 或 [**ID3DXConstantTable：： GetConstantByName**](id3dxconstanttable--getconstantbyname.md)。</span><span class="sxs-lookup"><span data-stu-id="60550-120">To get a constant that is not part of an array, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) or [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60550-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="60550-121">Requirements</span></span>



| <span data-ttu-id="60550-122">需求</span><span class="sxs-lookup"><span data-stu-id="60550-122">Requirement</span></span> | <span data-ttu-id="60550-123">值</span><span class="sxs-lookup"><span data-stu-id="60550-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60550-124">標頭</span><span class="sxs-lookup"><span data-stu-id="60550-124">Header</span></span><br/>  | <dl> <span data-ttu-id="60550-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="60550-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="60550-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="60550-126">Library</span></span><br/> | <dl> <span data-ttu-id="60550-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="60550-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="60550-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60550-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60550-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="60550-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
