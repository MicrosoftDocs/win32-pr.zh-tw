---
description: D3DXVECTOR4 結構 (D3DX10Math) -描述四個元件的向量，包括運算子多載和類型轉換。
ms.assetid: c6348346-f317-48ed-a369-e39fdb4dc1d6
title: 'D3DXVECTOR4 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 2e3af4c11922d7433c56b9353482eba8d374d5a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102826"
---
# <a name="d3dxvector4-structure-d3dx10mathh"></a><span data-ttu-id="4f0b0-103">D3DXVECTOR4 結構 (D3DX10Math .h) </span><span class="sxs-lookup"><span data-stu-id="4f0b0-103">D3DXVECTOR4 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="4f0b0-104">描述四個元件的向量，包括運算子多載和類型轉換。</span><span class="sxs-lookup"><span data-stu-id="4f0b0-104">Describes a four-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="4f0b0-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
```



## <a name="members"></a><span data-ttu-id="4f0b0-106">成員</span><span class="sxs-lookup"><span data-stu-id="4f0b0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f0b0-107">**x**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="4f0b0-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0b0-109">X 元件。</span><span class="sxs-lookup"><span data-stu-id="4f0b0-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="4f0b0-110">**y**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="4f0b0-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0b0-112">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="4f0b0-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="4f0b0-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="4f0b0-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0b0-115">Z 元件。</span><span class="sxs-lookup"><span data-stu-id="4f0b0-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="4f0b0-116">**w**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="4f0b0-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0b0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0b0-118">W 元件。</span><span class="sxs-lookup"><span data-stu-id="4f0b0-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f0b0-119">備註</span><span class="sxs-lookup"><span data-stu-id="4f0b0-119">Remarks</span></span>

<span data-ttu-id="4f0b0-120">**D3DXVECTOR4** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="4f0b0-120">**D3DXVECTOR4** has the following C++ extensions.</span></span>

### <a name="d3dxvector4-extensions"></a><span data-ttu-id="4f0b0-121">D3DXVECTOR4 延伸模組</span><span class="sxs-lookup"><span data-stu-id="4f0b0-121">D3DXVECTOR4 Extensions</span></span>


```
typedef struct D3DXVECTOR4
{
#ifdef __cplusplus
public:
    D3DXVECTOR4() {};
    D3DXVECTOR4( CONST FLOAT* );
    D3DXVECTOR4( CONST D3DXFLOAT16 * );
    D3DXVECTOR4( CONST D3DVECTOR& xyz, FLOAT w );
    D3DXVECTOR4( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR4& operator += ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator -= ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator *= ( FLOAT );
    D3DXVECTOR4& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR4 operator + () const;
    D3DXVECTOR4 operator - () const;

    // binary operators
    D3DXVECTOR4 operator + ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator - ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator * ( FLOAT ) const;
    D3DXVECTOR4 operator / ( FLOAT ) const;

    friend D3DXVECTOR4 operator * ( FLOAT, CONST D3DXVECTOR4& );

    BOOL operator == ( CONST D3DXVECTOR4& ) const;
    BOOL operator != ( CONST D3DXVECTOR4& ) const;

public:
#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
        
```



## <a name="requirements"></a><span data-ttu-id="4f0b0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f0b0-122">Requirements</span></span>



| <span data-ttu-id="4f0b0-123">需求</span><span class="sxs-lookup"><span data-stu-id="4f0b0-123">Requirement</span></span> | <span data-ttu-id="4f0b0-124">值</span><span class="sxs-lookup"><span data-stu-id="4f0b0-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0b0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4f0b0-125">Header</span></span><br/> | <dl> <span data-ttu-id="4f0b0-126"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f0b0-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0b0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f0b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0b0-128">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="4f0b0-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
