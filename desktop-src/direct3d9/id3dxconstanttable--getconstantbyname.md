---
description: 藉由查詢名稱來取得常數。
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: 'ID3DXConstantTable：： GetConstantByName 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3df4fc2cf44e035daf208d5dd14602e89b528ed1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981834"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a><span data-ttu-id="b00ab-103">ID3DXConstantTable：： GetConstantByName 方法</span><span class="sxs-lookup"><span data-stu-id="b00ab-103">ID3DXConstantTable::GetConstantByName method</span></span>

<span data-ttu-id="b00ab-104">藉由查詢名稱來取得常數。</span><span class="sxs-lookup"><span data-stu-id="b00ab-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b00ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="b00ab-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="b00ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="b00ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b00ab-107">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b00ab-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b00ab-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b00ab-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b00ab-109">父資料結構的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b00ab-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="b00ab-110">如果常數是最上層參數 (沒有任何父資料結構) ，請使用 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b00ab-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b00ab-111">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b00ab-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b00ab-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b00ab-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b00ab-113">常數的名稱。</span><span class="sxs-lookup"><span data-stu-id="b00ab-113">Name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b00ab-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b00ab-114">Return value</span></span>

<span data-ttu-id="b00ab-115">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b00ab-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b00ab-116">傳回常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b00ab-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="b00ab-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b00ab-117">Requirements</span></span>



| <span data-ttu-id="b00ab-118">需求</span><span class="sxs-lookup"><span data-stu-id="b00ab-118">Requirement</span></span> | <span data-ttu-id="b00ab-119">值</span><span class="sxs-lookup"><span data-stu-id="b00ab-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b00ab-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b00ab-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b00ab-121"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="b00ab-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b00ab-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="b00ab-122">Library</span></span><br/> | <dl> <span data-ttu-id="b00ab-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b00ab-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b00ab-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b00ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b00ab-125">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b00ab-125">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
