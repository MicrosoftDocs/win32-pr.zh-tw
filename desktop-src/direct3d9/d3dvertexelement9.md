---
description: 定義頂點資料版面配置。 每個頂點都可以包含一或多個資料類型，而每個資料類型都是由頂點元素所描述。
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: 'D3DVERTEXELEMENT9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998367"
---
# <a name="d3dvertexelement9-structure"></a><span data-ttu-id="24412-104">D3DVERTEXELEMENT9 結構</span><span class="sxs-lookup"><span data-stu-id="24412-104">D3DVERTEXELEMENT9 structure</span></span>

<span data-ttu-id="24412-105">定義頂點資料版面配置。</span><span class="sxs-lookup"><span data-stu-id="24412-105">Defines the vertex data layout.</span></span> <span data-ttu-id="24412-106">每個頂點都可以包含一或多個資料類型，而每個資料類型都是由頂點元素所描述。</span><span class="sxs-lookup"><span data-stu-id="24412-106">Each vertex can contain one or more data types, and each data type is described by a vertex element.</span></span>

## <a name="syntax"></a><span data-ttu-id="24412-107">語法</span><span class="sxs-lookup"><span data-stu-id="24412-107">Syntax</span></span>


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a><span data-ttu-id="24412-108">成員</span><span class="sxs-lookup"><span data-stu-id="24412-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="24412-109">**串流**</span><span class="sxs-lookup"><span data-stu-id="24412-109">**Stream**</span></span>
</dt> <dd>

<span data-ttu-id="24412-110">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24412-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="24412-111">資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="24412-111">Stream number.</span></span>

</dd> <dt>

<span data-ttu-id="24412-112">**Offset**</span><span class="sxs-lookup"><span data-stu-id="24412-112">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="24412-113">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24412-113">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="24412-114">從頂點資料的開頭位移到與特定資料類型相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="24412-114">Offset from the beginning of the vertex data to the data associated with the particular data type.</span></span>

</dd> <dt>

<span data-ttu-id="24412-115">**型別**</span><span class="sxs-lookup"><span data-stu-id="24412-115">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="24412-116">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24412-116">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="24412-117">以 [**D3DDECLTYPE**](./d3ddecltype.md)指定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="24412-117">The data type, specified as a [**D3DDECLTYPE**](./d3ddecltype.md).</span></span> <span data-ttu-id="24412-118">定義資料大小的數個預先定義類型的其中一個。</span><span class="sxs-lookup"><span data-stu-id="24412-118">One of several predefined types that define the data size.</span></span> <span data-ttu-id="24412-119">某些方法具有隱含類型。</span><span class="sxs-lookup"><span data-stu-id="24412-119">Some methods have an implied type.</span></span>

</dd> <dt>

<span data-ttu-id="24412-120">**方法**</span><span class="sxs-lookup"><span data-stu-id="24412-120">**Method**</span></span>
</dt> <dd>

<span data-ttu-id="24412-121">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24412-121">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="24412-122">方法會指定鑲嵌處理，以決定鑲嵌如何解讀 (或) 頂點資料上運作。</span><span class="sxs-lookup"><span data-stu-id="24412-122">The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data.</span></span> <span data-ttu-id="24412-123">如需詳細資訊，請參閱 [**D3DDECLMETHOD**](./d3ddeclmethod.md)。</span><span class="sxs-lookup"><span data-stu-id="24412-123">For more information, see [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>

</dd> <dt>

<span data-ttu-id="24412-124">**使用量**</span><span class="sxs-lookup"><span data-stu-id="24412-124">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="24412-125">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24412-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="24412-126">定義將使用資料的目標;也就是說，頂點資料版面配置和頂點著色器之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="24412-126">Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders.</span></span> <span data-ttu-id="24412-127">每個使用方式都會將頂點宣告系結至頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="24412-127">Each usage acts to bind a vertex declaration to a vertex shader.</span></span> <span data-ttu-id="24412-128">在某些情況下，它們會有特殊的解讀。</span><span class="sxs-lookup"><span data-stu-id="24412-128">In some cases, they have a special interpretation.</span></span> <span data-ttu-id="24412-129">例如， \_ N patch 鑲嵌會使用指定 D3DDECLUSAGE NORMAL 或 D3DDECLUSAGE POSITION 的元素 \_ 來設定鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="24412-129">For example, an element that specifies D3DDECLUSAGE\_NORMAL or D3DDECLUSAGE\_POSITION is used by the N-patch tessellator to set up tessellation.</span></span> <span data-ttu-id="24412-130">如需可用的語法清單，請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md) 。</span><span class="sxs-lookup"><span data-stu-id="24412-130">See [**D3DDECLUSAGE**](./d3ddeclusage.md) for a list of the available semantics.</span></span> <span data-ttu-id="24412-131">D3DDECLUSAGE \_ TEXCOORD 可用於使用者定義的欄位， (沒有定義) 的現有用法。</span><span class="sxs-lookup"><span data-stu-id="24412-131">D3DDECLUSAGE\_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).</span></span>

</dd> <dt>

<span data-ttu-id="24412-132">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="24412-132">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="24412-133">類型： **[**位元組**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24412-133">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="24412-134">修改使用方式資料，以允許使用者指定多個使用類型。</span><span class="sxs-lookup"><span data-stu-id="24412-134">Modifies the usage data to allow the user to specify multiple usage types.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24412-135">備註</span><span class="sxs-lookup"><span data-stu-id="24412-135">Remarks</span></span>

<span data-ttu-id="24412-136">頂點資料是使用 **D3DVERTEXELEMENT9** 結構的陣列來定義。</span><span class="sxs-lookup"><span data-stu-id="24412-136">Vertex data is defined using an array of **D3DVERTEXELEMENT9** structures.</span></span> <span data-ttu-id="24412-137">使用 [**D3DDECL \_ END**](d3ddecl-end.md) 宣告宣告中的最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="24412-137">Use [**D3DDECL\_END**](d3ddecl-end.md) to declare the last element in the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="24412-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="24412-138">Requirements</span></span>



| <span data-ttu-id="24412-139">需求</span><span class="sxs-lookup"><span data-stu-id="24412-139">Requirement</span></span> | <span data-ttu-id="24412-140">值</span><span class="sxs-lookup"><span data-stu-id="24412-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24412-141">標頭</span><span class="sxs-lookup"><span data-stu-id="24412-141">Header</span></span><br/> | <dl> <span data-ttu-id="24412-142"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="24412-142"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24412-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24412-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24412-144">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="24412-144">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="24412-145"> (Direct3D 9) 的頂點宣告 </span><span class="sxs-lookup"><span data-stu-id="24412-145">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
