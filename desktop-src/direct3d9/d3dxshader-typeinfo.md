---
description: 包含成員類型資訊的 helper 結構。
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: 'D3DXSHADER_TYPEINFO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322863"
---
# <a name="d3dxshader_typeinfo-structure"></a><span data-ttu-id="8262f-103">D3DXSHADER \_ TYPEINFO 結構</span><span class="sxs-lookup"><span data-stu-id="8262f-103">D3DXSHADER\_TYPEINFO structure</span></span>

<span data-ttu-id="8262f-104">包含成員類型資訊的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="8262f-104">A helper structure containing member type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8262f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8262f-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="8262f-106">成員</span><span class="sxs-lookup"><span data-stu-id="8262f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8262f-107">**類別**</span><span class="sxs-lookup"><span data-stu-id="8262f-107">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="8262f-108">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8262f-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8262f-109">著色器物件類型。</span><span class="sxs-lookup"><span data-stu-id="8262f-109">Shader object type.</span></span> <span data-ttu-id="8262f-110">請參閱 [**D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)。</span><span class="sxs-lookup"><span data-stu-id="8262f-110">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="8262f-111">**型別**</span><span class="sxs-lookup"><span data-stu-id="8262f-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="8262f-112">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8262f-112">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8262f-113">資料類型。</span><span class="sxs-lookup"><span data-stu-id="8262f-113">Data type.</span></span> <span data-ttu-id="8262f-114">請參閱 [**D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)。</span><span class="sxs-lookup"><span data-stu-id="8262f-114">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="8262f-115">**資料列**</span><span class="sxs-lookup"><span data-stu-id="8262f-115">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="8262f-116">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8262f-116">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8262f-117"> (矩陣) 的矩陣資料列數目。</span><span class="sxs-lookup"><span data-stu-id="8262f-117">Number of matrix rows (matrices).</span></span>

</dd> <dt>

<span data-ttu-id="8262f-118">**資料行**</span><span class="sxs-lookup"><span data-stu-id="8262f-118">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="8262f-119">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8262f-119">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8262f-120"> (向量和矩陣) 的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="8262f-120">Number of columns (vectors and matrices).</span></span>

</dd> <dt>

<span data-ttu-id="8262f-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="8262f-121">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="8262f-122">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8262f-122">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8262f-123">陣列維度。</span><span class="sxs-lookup"><span data-stu-id="8262f-123">Array dimension.</span></span>

</dd> <dt>

<span data-ttu-id="8262f-124">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="8262f-124">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="8262f-125">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8262f-125">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8262f-126">結構成員的數目。</span><span class="sxs-lookup"><span data-stu-id="8262f-126">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="8262f-127">**StructMemberInfo**</span><span class="sxs-lookup"><span data-stu-id="8262f-127">**StructMemberInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8262f-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8262f-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8262f-129">結構成員資訊的陣列，D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] 。</span><span class="sxs-lookup"><span data-stu-id="8262f-129">Array of structure member information, D3DXSHADER\_STRUCTMEMBERINFO\[*StructMembers*\].</span></span> <span data-ttu-id="8262f-130">請參閱 [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="8262f-130">See [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8262f-131">備註</span><span class="sxs-lookup"><span data-stu-id="8262f-131">Remarks</span></span>

<span data-ttu-id="8262f-132">類型資訊是 [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md)的一部分。</span><span class="sxs-lookup"><span data-stu-id="8262f-132">The type information is part of [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8262f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="8262f-133">Requirements</span></span>



| <span data-ttu-id="8262f-134">需求</span><span class="sxs-lookup"><span data-stu-id="8262f-134">Requirement</span></span> | <span data-ttu-id="8262f-135">值</span><span class="sxs-lookup"><span data-stu-id="8262f-135">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8262f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="8262f-136">Header</span></span><br/> | <dl> <span data-ttu-id="8262f-137"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="8262f-137"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8262f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8262f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8262f-139">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="8262f-139">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="8262f-140">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="8262f-140">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
