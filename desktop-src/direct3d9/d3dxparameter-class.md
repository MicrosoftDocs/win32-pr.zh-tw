---
description: 物件的型別。
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: 'D3DXPARAMETER_CLASS 列舉 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853967"
---
# <a name="d3dxparameter_class-enumeration"></a><span data-ttu-id="a5617-103">D3DXPARAMETER \_ 類別列舉</span><span class="sxs-lookup"><span data-stu-id="a5617-103">D3DXPARAMETER\_CLASS enumeration</span></span>

<span data-ttu-id="a5617-104">物件的型別。</span><span class="sxs-lookup"><span data-stu-id="a5617-104">The type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5617-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5617-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a><span data-ttu-id="a5617-106">常數</span><span class="sxs-lookup"><span data-stu-id="a5617-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a5617-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC \_ 純量**</span><span class="sxs-lookup"><span data-stu-id="a5617-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC\_SCALAR**</span></span>
</dt> <dd>

<span data-ttu-id="a5617-108">常數是純量。</span><span class="sxs-lookup"><span data-stu-id="a5617-108">Constant is a scalar.</span></span>

</dd> <dt>

<span data-ttu-id="a5617-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC \_ 向量**</span><span class="sxs-lookup"><span data-stu-id="a5617-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC\_VECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a5617-110">常數是向量。</span><span class="sxs-lookup"><span data-stu-id="a5617-110">Constant is a vector.</span></span>

</dd> <dt>

<span data-ttu-id="a5617-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC \_ 矩陣資料 \_ 列**</span><span class="sxs-lookup"><span data-stu-id="a5617-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC\_MATRIX\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="a5617-112">常數是資料列的主要矩陣。</span><span class="sxs-lookup"><span data-stu-id="a5617-112">Constant is a row major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a5617-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC \_ 矩陣資料 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="a5617-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC\_MATRIX\_COLUMNS**</span></span>
</dt> <dd>

<span data-ttu-id="a5617-114">常數是資料行主要矩陣。</span><span class="sxs-lookup"><span data-stu-id="a5617-114">Constant is a column major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a5617-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="a5617-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="a5617-116">常數可以是材質、著色器或字串。</span><span class="sxs-lookup"><span data-stu-id="a5617-116">Constant is either a texture, shader, or a string.</span></span>

</dd> <dt>

<span data-ttu-id="a5617-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="a5617-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC\_STRUCT**</span></span>
</dt> <dd>

<span data-ttu-id="a5617-118">常數是一種結構。</span><span class="sxs-lookup"><span data-stu-id="a5617-118">Constant is a structure.</span></span>

</dd> <dt>

<span data-ttu-id="a5617-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a5617-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a5617-120">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="a5617-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a5617-121">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="a5617-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a5617-122">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="a5617-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5617-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5617-123">Requirements</span></span>



| <span data-ttu-id="a5617-124">需求</span><span class="sxs-lookup"><span data-stu-id="a5617-124">Requirement</span></span> | <span data-ttu-id="a5617-125">值</span><span class="sxs-lookup"><span data-stu-id="a5617-125">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5617-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a5617-126">Header</span></span><br/> | <dl> <span data-ttu-id="a5617-127"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5617-127"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5617-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5617-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5617-129">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="a5617-129">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="a5617-130">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="a5617-130">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a5617-131">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a5617-131">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




