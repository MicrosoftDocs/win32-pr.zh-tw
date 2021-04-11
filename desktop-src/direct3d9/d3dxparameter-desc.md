---
description: 描述用於效果物件的參數。
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: 'D3DXPARAMETER_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196181"
---
# <a name="d3dxparameter_desc-structure"></a><span data-ttu-id="41b82-103">D3DXPARAMETER \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="41b82-103">D3DXPARAMETER\_DESC structure</span></span>

<span data-ttu-id="41b82-104">描述用於效果物件的參數。</span><span class="sxs-lookup"><span data-stu-id="41b82-104">Describes a parameter used for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b82-105">語法</span><span class="sxs-lookup"><span data-stu-id="41b82-105">Syntax</span></span>


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a><span data-ttu-id="41b82-106">成員</span><span class="sxs-lookup"><span data-stu-id="41b82-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41b82-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="41b82-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-109">參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="41b82-109">Name of the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="41b82-110">**語義**</span><span class="sxs-lookup"><span data-stu-id="41b82-110">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-112">語義意義，也稱為使用方式。</span><span class="sxs-lookup"><span data-stu-id="41b82-112">Semantic meaning, also called the usage.</span></span>

</dd> <dt>

<span data-ttu-id="41b82-113">**類別**</span><span class="sxs-lookup"><span data-stu-id="41b82-113">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-114">Type： **[ **D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-114">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-115">Parameter 類別。</span><span class="sxs-lookup"><span data-stu-id="41b82-115">Parameter class.</span></span> <span data-ttu-id="41b82-116">將此值設定為 [**D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="41b82-116">Set this to one of the values in [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="41b82-117">**型別**</span><span class="sxs-lookup"><span data-stu-id="41b82-117">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-118">類型： **[ **D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-118">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-119">參數類型。</span><span class="sxs-lookup"><span data-stu-id="41b82-119">Parameter type.</span></span> <span data-ttu-id="41b82-120">將此值設定為 [ [**D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)] 中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="41b82-120">Set this to one of the values in [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="41b82-121">**資料列**</span><span class="sxs-lookup"><span data-stu-id="41b82-121">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-123">陣列中的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="41b82-123">Number of rows in the array.</span></span>

</dd> <dt>

<span data-ttu-id="41b82-124">**資料行**</span><span class="sxs-lookup"><span data-stu-id="41b82-124">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-125">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-126">陣列中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="41b82-126">Number of columns in the array.</span></span>

</dd> <dt>

<span data-ttu-id="41b82-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="41b82-127">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-128">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-129">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="41b82-129">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="41b82-130">**註解**</span><span class="sxs-lookup"><span data-stu-id="41b82-130">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-131">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-132">注釋的數目。</span><span class="sxs-lookup"><span data-stu-id="41b82-132">Number of annotations.</span></span>

</dd> <dt>

<span data-ttu-id="41b82-133">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="41b82-133">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-134">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-135">結構成員的數目。</span><span class="sxs-lookup"><span data-stu-id="41b82-135">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="41b82-136">**旗標**</span><span class="sxs-lookup"><span data-stu-id="41b82-136">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-137">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-138">參數屬性。</span><span class="sxs-lookup"><span data-stu-id="41b82-138">Parameter attributes.</span></span> <span data-ttu-id="41b82-139">請參閱 [效果常數](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="41b82-139">See [Effect Constants](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="41b82-140">**Bytes**</span><span class="sxs-lookup"><span data-stu-id="41b82-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="41b82-141">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41b82-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="41b82-142">參數的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="41b82-142">The size of the parameter, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41b82-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="41b82-143">Requirements</span></span>



| <span data-ttu-id="41b82-144">需求</span><span class="sxs-lookup"><span data-stu-id="41b82-144">Requirement</span></span> | <span data-ttu-id="41b82-145">值</span><span class="sxs-lookup"><span data-stu-id="41b82-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b82-146">標頭</span><span class="sxs-lookup"><span data-stu-id="41b82-146">Header</span></span><br/> | <dl> <span data-ttu-id="41b82-147"><dt>D3dx9effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="41b82-147"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b82-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41b82-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b82-149">效果結構</span><span class="sxs-lookup"><span data-stu-id="41b82-149">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
