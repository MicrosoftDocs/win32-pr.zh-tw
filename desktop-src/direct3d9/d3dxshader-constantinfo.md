---
description: D3DXSHADER \_ CONSTANTINFO 結構
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: 'D3DXSHADER_CONSTANTINFO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196240"
---
# <a name="d3dxshader_constantinfo-structure"></a><span data-ttu-id="8b454-103">D3DXSHADER \_ CONSTANTINFO 結構</span><span class="sxs-lookup"><span data-stu-id="8b454-103">D3DXSHADER\_CONSTANTINFO structure</span></span>

## <a name="syntax"></a><span data-ttu-id="8b454-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b454-104">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a><span data-ttu-id="8b454-105">成員</span><span class="sxs-lookup"><span data-stu-id="8b454-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b454-106">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8b454-106">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="8b454-107">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b454-107">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8b454-108">從這個結構開頭算起的位移（以位元組為單位），指向包含常數資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="8b454-108">Offset from the beginning of this structure, in bytes, to the string that contains the constant information.</span></span>

</dd> <dt>

<span data-ttu-id="8b454-109">**RegisterSet**</span><span class="sxs-lookup"><span data-stu-id="8b454-109">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="8b454-110">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b454-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8b454-111">註冊集。</span><span class="sxs-lookup"><span data-stu-id="8b454-111">Register set.</span></span> <span data-ttu-id="8b454-112">請參閱 [**D3DXREGISTER \_ SET**](./d3dxregister-set.md)。</span><span class="sxs-lookup"><span data-stu-id="8b454-112">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b454-113">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="8b454-113">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="8b454-114">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b454-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8b454-115">註冊索引。</span><span class="sxs-lookup"><span data-stu-id="8b454-115">The register index.</span></span>

</dd> <dt>

<span data-ttu-id="8b454-116">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="8b454-116">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="8b454-117">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b454-117">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8b454-118">註冊數目。</span><span class="sxs-lookup"><span data-stu-id="8b454-118">Number of registers.</span></span>

</dd> <dt>

<span data-ttu-id="8b454-119">**已保留**</span><span class="sxs-lookup"><span data-stu-id="8b454-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="8b454-120">類型： **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b454-120">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8b454-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="8b454-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8b454-122">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="8b454-122">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8b454-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b454-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8b454-124">從這個結構開頭算起的位移（以位元組為單位），指向包含 [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md) 資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="8b454-124">Offset from the beginning of this structure, in bytes, to the string that contains the [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md) information.</span></span>

</dd> <dt>

<span data-ttu-id="8b454-125">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="8b454-125">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="8b454-126">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b454-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8b454-127">從這個結構開頭算起的位移（以位元組為單位），指向包含預設值的字串。</span><span class="sxs-lookup"><span data-stu-id="8b454-127">Offset from the beginning of this structure, in bytes, to the string that contains the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b454-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b454-128">Requirements</span></span>



| <span data-ttu-id="8b454-129">需求</span><span class="sxs-lookup"><span data-stu-id="8b454-129">Requirement</span></span> | <span data-ttu-id="8b454-130">值</span><span class="sxs-lookup"><span data-stu-id="8b454-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b454-131">標頭</span><span class="sxs-lookup"><span data-stu-id="8b454-131">Header</span></span><br/> | <dl> <span data-ttu-id="8b454-132"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b454-132"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b454-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b454-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b454-134">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="8b454-134">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
