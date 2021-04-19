---
description: 管理著色器常數資料表的協助程式結構。 這也可以使用 ID3DXConstantTable 來完成。
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: 'D3DXSHADER_CONSTANTTABLE 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986736"
---
# <a name="d3dxshader_constanttable-structure"></a><span data-ttu-id="03b2c-104">D3DXSHADER \_ CONSTANTTABLE 結構</span><span class="sxs-lookup"><span data-stu-id="03b2c-104">D3DXSHADER\_CONSTANTTABLE structure</span></span>

<span data-ttu-id="03b2c-105">管理著色器常數資料表的協助程式結構。</span><span class="sxs-lookup"><span data-stu-id="03b2c-105">Helper structure for managing a shader constant table.</span></span> <span data-ttu-id="03b2c-106">這也可以使用 [**ID3DXConstantTable**](id3dxconstanttable.md)來完成。</span><span class="sxs-lookup"><span data-stu-id="03b2c-106">This can also be done using [**ID3DXConstantTable**](id3dxconstanttable.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03b2c-107">語法</span><span class="sxs-lookup"><span data-stu-id="03b2c-107">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a><span data-ttu-id="03b2c-108">成員</span><span class="sxs-lookup"><span data-stu-id="03b2c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="03b2c-109">**大小**</span><span class="sxs-lookup"><span data-stu-id="03b2c-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="03b2c-110">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03b2c-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03b2c-111">結構的大小。</span><span class="sxs-lookup"><span data-stu-id="03b2c-111">Size of the structure.</span></span> <span data-ttu-id="03b2c-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="03b2c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="03b2c-113">**建立者**</span><span class="sxs-lookup"><span data-stu-id="03b2c-113">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="03b2c-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03b2c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03b2c-115">從這個結構開頭算起的位移（以位元組為單位），指向包含建立者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="03b2c-115">Offset from the beginning of this structure, in bytes, to the string that contains the name of the creator.</span></span>

</dd> <dt>

<span data-ttu-id="03b2c-116">**版本**</span><span class="sxs-lookup"><span data-stu-id="03b2c-116">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="03b2c-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03b2c-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03b2c-118">著色器版本。</span><span class="sxs-lookup"><span data-stu-id="03b2c-118">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="03b2c-119">**常數**</span><span class="sxs-lookup"><span data-stu-id="03b2c-119">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="03b2c-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03b2c-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03b2c-121">常數的數目。</span><span class="sxs-lookup"><span data-stu-id="03b2c-121">Number of constants.</span></span>

</dd> <dt>

<span data-ttu-id="03b2c-122">**ConstantInfo**</span><span class="sxs-lookup"><span data-stu-id="03b2c-122">**ConstantInfo**</span></span>
</dt> <dd>

<span data-ttu-id="03b2c-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03b2c-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03b2c-124">常數資訊的陣列，D3DXSHADER \_ CONSTANTINFO \[ *常數* \] 。</span><span class="sxs-lookup"><span data-stu-id="03b2c-124">Array of constant information, D3DXSHADER\_CONSTANTINFO\[*Constants*\].</span></span> <span data-ttu-id="03b2c-125">請參閱 [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="03b2c-125">See [**D3DXSHADER\_CONSTANTINFO**](d3dxshader-constantinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="03b2c-126">**旗標**</span><span class="sxs-lookup"><span data-stu-id="03b2c-126">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="03b2c-127">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03b2c-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03b2c-128">用來編譯著色器的 [D3DXSHADER 旗](d3dxshader-flags.md) 標旗標。</span><span class="sxs-lookup"><span data-stu-id="03b2c-128">The [D3DXSHADER Flags](d3dxshader-flags.md) flags used to compile the shader.</span></span>

</dd> <dt>

<span data-ttu-id="03b2c-129">**Target**</span><span class="sxs-lookup"><span data-stu-id="03b2c-129">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="03b2c-130">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03b2c-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03b2c-131">包含目標之字串的位移。</span><span class="sxs-lookup"><span data-stu-id="03b2c-131">Offset into the string that contains the target.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03b2c-132">備註</span><span class="sxs-lookup"><span data-stu-id="03b2c-132">Remarks</span></span>

<span data-ttu-id="03b2c-133">著色器常數資訊會包含在以 tab 分隔的批註資料表中。</span><span class="sxs-lookup"><span data-stu-id="03b2c-133">Shader constant information is included in a tab-delimited table of comments.</span></span> <span data-ttu-id="03b2c-134">所有位移都會以位元組為單位，從結構的開頭算起。</span><span class="sxs-lookup"><span data-stu-id="03b2c-134">All offsets are measured in bytes from the beginning of the structure.</span></span> <span data-ttu-id="03b2c-135">常數資料表中的專案會依建立者的遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="03b2c-135">Entries in the constant table are sorted by Creator in ascending order.</span></span>

<span data-ttu-id="03b2c-136">您可以使用 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面來管理著色器常數資料表。</span><span class="sxs-lookup"><span data-stu-id="03b2c-136">A shader constant table can be managed with the [**ID3DXConstantTable**](id3dxconstanttable.md) interfaces.</span></span> <span data-ttu-id="03b2c-137">或者，您也可以使用 **D3DXSHADER \_ CONSTANTTABLE** 來管理常數資料表。</span><span class="sxs-lookup"><span data-stu-id="03b2c-137">Alternatively, you can manage the constant table with **D3DXSHADER\_CONSTANTTABLE**.</span></span>

<span data-ttu-id="03b2c-138">此大小成員通常會使用下列程式初始化：</span><span class="sxs-lookup"><span data-stu-id="03b2c-138">This size member is often initialized using the following:</span></span>


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a><span data-ttu-id="03b2c-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="03b2c-139">Requirements</span></span>



| <span data-ttu-id="03b2c-140">需求</span><span class="sxs-lookup"><span data-stu-id="03b2c-140">Requirement</span></span> | <span data-ttu-id="03b2c-141">值</span><span class="sxs-lookup"><span data-stu-id="03b2c-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b2c-142">標頭</span><span class="sxs-lookup"><span data-stu-id="03b2c-142">Header</span></span><br/> | <dl> <span data-ttu-id="03b2c-143"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="03b2c-143"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03b2c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03b2c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b2c-145">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="03b2c-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="03b2c-146">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="03b2c-146">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
