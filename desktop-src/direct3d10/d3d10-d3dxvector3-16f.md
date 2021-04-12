---
description: 與 D3DXVECTOR3 相同，但它會使用 x、y 和 z 的16位浮點值。
ms.assetid: b21676f1-5cff-4eef-bd60-5c09882283dc
title: 'D3DXVECTOR3_16F 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b7143e864eddf37842e19d7554150beaf50c0b53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946070"
---
# <a name="d3dxvector3_16f-structure"></a><span data-ttu-id="1f9ee-103">D3DXVECTOR3 \_ 16F 結構</span><span class="sxs-lookup"><span data-stu-id="1f9ee-103">D3DXVECTOR3\_16F structure</span></span>

<span data-ttu-id="1f9ee-104">與 [**D3DXVECTOR3**](d3d10-d3dxvector3.md)相同，但它會使用 x、y 和 z 的16位浮點值。</span><span class="sxs-lookup"><span data-stu-id="1f9ee-104">Same as a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9ee-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f9ee-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="members"></a><span data-ttu-id="1f9ee-106">成員</span><span class="sxs-lookup"><span data-stu-id="1f9ee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f9ee-107">**x**</span><span class="sxs-lookup"><span data-stu-id="1f9ee-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="1f9ee-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f9ee-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f9ee-109">X 元件。</span><span class="sxs-lookup"><span data-stu-id="1f9ee-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="1f9ee-110">**y**</span><span class="sxs-lookup"><span data-stu-id="1f9ee-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="1f9ee-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f9ee-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f9ee-112">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="1f9ee-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="1f9ee-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="1f9ee-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="1f9ee-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f9ee-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1f9ee-115">Z 元件。</span><span class="sxs-lookup"><span data-stu-id="1f9ee-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f9ee-116">備註</span><span class="sxs-lookup"><span data-stu-id="1f9ee-116">Remarks</span></span>

<span data-ttu-id="1f9ee-117">**D3DXVECTOR3 \_ 16F** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1f9ee-117">**D3DXVECTOR3\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector3_16f-extensions"></a><span data-ttu-id="1f9ee-118">D3DXVECTOR3 \_ 16F 延伸模組</span><span class="sxs-lookup"><span data-stu-id="1f9ee-118">D3DXVECTOR3\_16F Extensions</span></span>


```

typedef struct D3DXVECTOR3_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR3_16F() {};
    D3DXVECTOR3_16F( CONST FLOAT * );
    D3DXVECTOR3_16F( CONST D3DVECTOR& );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y, CONST D3DXFLOAT16 &z );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR3_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR3_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z;

} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="requirements"></a><span data-ttu-id="1f9ee-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f9ee-119">Requirements</span></span>



| <span data-ttu-id="1f9ee-120">需求</span><span class="sxs-lookup"><span data-stu-id="1f9ee-120">Requirement</span></span> | <span data-ttu-id="1f9ee-121">值</span><span class="sxs-lookup"><span data-stu-id="1f9ee-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9ee-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1f9ee-122">Header</span></span><br/> | <dl> <span data-ttu-id="1f9ee-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9ee-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9ee-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f9ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9ee-125">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="1f9ee-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
