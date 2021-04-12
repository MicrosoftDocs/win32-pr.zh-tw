---
description: 描述包含運算子多載和類型轉換的雙元件向量。 與 D3DXVECTOR2 相同，但它會使用 x、y 和 z 的16位浮點值。
ms.assetid: b410d2e1-a006-4563-928a-c9000f73c224
title: 'D3DXVECTOR2_16F 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 677f4f8c47cdc70791ad98e18582810bbff23920
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696584"
---
# <a name="d3dxvector2_16f-structure"></a><span data-ttu-id="9def2-104">D3DXVECTOR2 \_ 16F 結構</span><span class="sxs-lookup"><span data-stu-id="9def2-104">D3DXVECTOR2\_16F structure</span></span>

<span data-ttu-id="9def2-105">描述包含運算子多載和類型轉換的雙元件向量。</span><span class="sxs-lookup"><span data-stu-id="9def2-105">Describes a two-component vector including operator overloads and type casts.</span></span> <span data-ttu-id="9def2-106">與 [**D3DXVECTOR2**](d3d10-d3dxvector2.md)相同，但它會使用 x、y 和 z 的16位浮點值。</span><span class="sxs-lookup"><span data-stu-id="9def2-106">Same as a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="9def2-107">語法</span><span class="sxs-lookup"><span data-stu-id="9def2-107">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2_16F {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="members"></a><span data-ttu-id="9def2-108">成員</span><span class="sxs-lookup"><span data-stu-id="9def2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9def2-109">**x**</span><span class="sxs-lookup"><span data-stu-id="9def2-109">**x**</span></span>
</dt> <dd>

<span data-ttu-id="9def2-110">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9def2-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9def2-111">X 元件。</span><span class="sxs-lookup"><span data-stu-id="9def2-111">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="9def2-112">**y**</span><span class="sxs-lookup"><span data-stu-id="9def2-112">**y**</span></span>
</dt> <dd>

<span data-ttu-id="9def2-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9def2-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9def2-114">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="9def2-114">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9def2-115">備註</span><span class="sxs-lookup"><span data-stu-id="9def2-115">Remarks</span></span>

<span data-ttu-id="9def2-116">**D3DXVECTOR2 \_ 16F** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="9def2-116">**D3DXVECTOR2\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector2_16f-extensions"></a><span data-ttu-id="9def2-117">D3DXVECTOR2 \_ 16F 延伸模組</span><span class="sxs-lookup"><span data-stu-id="9def2-117">D3DXVECTOR2\_16F Extensions</span></span>


```

typedef struct D3DXVECTOR2_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR2_16F() {};
    D3DXVECTOR2_16F( CONST FLOAT * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR2_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR2_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y;

} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="requirements"></a><span data-ttu-id="9def2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9def2-118">Requirements</span></span>



| <span data-ttu-id="9def2-119">需求</span><span class="sxs-lookup"><span data-stu-id="9def2-119">Requirement</span></span> | <span data-ttu-id="9def2-120">值</span><span class="sxs-lookup"><span data-stu-id="9def2-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9def2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9def2-121">Header</span></span><br/> | <dl> <span data-ttu-id="9def2-122"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9def2-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9def2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9def2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9def2-124">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="9def2-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
