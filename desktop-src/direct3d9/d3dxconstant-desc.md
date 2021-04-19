---
description: 常數資料表中常數的描述。
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: 'D3DXCONSTANT_DESC 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990024"
---
# <a name="d3dxconstant_desc-structure"></a><span data-ttu-id="97b6b-103">D3DXCONSTANT \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="97b6b-103">D3DXCONSTANT\_DESC structure</span></span>

<span data-ttu-id="97b6b-104">常數資料表中常數的描述。</span><span class="sxs-lookup"><span data-stu-id="97b6b-104">A description of a constant in a constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b6b-105">語法</span><span class="sxs-lookup"><span data-stu-id="97b6b-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a><span data-ttu-id="97b6b-106">成員</span><span class="sxs-lookup"><span data-stu-id="97b6b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="97b6b-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="97b6b-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-109">常數的名稱。</span><span class="sxs-lookup"><span data-stu-id="97b6b-109">Name of the constant.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-110">**RegisterSet**</span><span class="sxs-lookup"><span data-stu-id="97b6b-110">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-111">類型： **[ **D3DXREGISTER \_ 集**](./d3dxregister-set.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-111">Type: **[**D3DXREGISTER\_SET**](./d3dxregister-set.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-112">常數資料類型。</span><span class="sxs-lookup"><span data-stu-id="97b6b-112">Constant data type.</span></span> <span data-ttu-id="97b6b-113">請參閱 [**D3DXREGISTER \_ SET**](./d3dxregister-set.md)。</span><span class="sxs-lookup"><span data-stu-id="97b6b-113">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-114">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="97b6b-114">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-116">資料表中常數的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="97b6b-116">Zero-based index of the constant in the table.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-117">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="97b6b-117">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-119">包含資料的暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="97b6b-119">Number of registers that contain data.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-120">**類別**</span><span class="sxs-lookup"><span data-stu-id="97b6b-120">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-121">Type： **[ **D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-121">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-122">Parameter 類別。</span><span class="sxs-lookup"><span data-stu-id="97b6b-122">Parameter class.</span></span> <span data-ttu-id="97b6b-123">請參閱 [**D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)。</span><span class="sxs-lookup"><span data-stu-id="97b6b-123">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-124">**型別**</span><span class="sxs-lookup"><span data-stu-id="97b6b-124">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-125">類型： **[ **D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-125">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-126">參數類型。</span><span class="sxs-lookup"><span data-stu-id="97b6b-126">Parameter type.</span></span> <span data-ttu-id="97b6b-127">請參閱 [**D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)。</span><span class="sxs-lookup"><span data-stu-id="97b6b-127">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-128">**資料列**</span><span class="sxs-lookup"><span data-stu-id="97b6b-128">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-129">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-130">資料列數目。</span><span class="sxs-lookup"><span data-stu-id="97b6b-130">Number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-131">**資料行**</span><span class="sxs-lookup"><span data-stu-id="97b6b-131">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-132">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-133">資料行數目。</span><span class="sxs-lookup"><span data-stu-id="97b6b-133">Number of columns.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="97b6b-134">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-135">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-136">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="97b6b-136">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-137">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="97b6b-137">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-138">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-139">結構成員子參數的數目。</span><span class="sxs-lookup"><span data-stu-id="97b6b-139">Number of structure member sub-parameters.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-140">**Bytes**</span><span class="sxs-lookup"><span data-stu-id="97b6b-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-141">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-142">資料大小（位元組數）。</span><span class="sxs-lookup"><span data-stu-id="97b6b-142">Data size in number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="97b6b-143">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="97b6b-143">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="97b6b-144">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97b6b-144">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97b6b-145">預設值的指標。</span><span class="sxs-lookup"><span data-stu-id="97b6b-145">Pointer to the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97b6b-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="97b6b-146">Requirements</span></span>



| <span data-ttu-id="97b6b-147">需求</span><span class="sxs-lookup"><span data-stu-id="97b6b-147">Requirement</span></span> | <span data-ttu-id="97b6b-148">值</span><span class="sxs-lookup"><span data-stu-id="97b6b-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97b6b-149">標頭</span><span class="sxs-lookup"><span data-stu-id="97b6b-149">Header</span></span><br/> | <dl> <span data-ttu-id="97b6b-150"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="97b6b-150"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b6b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97b6b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b6b-152">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="97b6b-152">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="97b6b-153">**D3DXCONSTANTTABLE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="97b6b-153">**D3DXCONSTANTTABLE\_DESC**</span></span>](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
