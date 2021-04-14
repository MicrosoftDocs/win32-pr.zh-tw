---
description: 與 D3DXVECTOR4 相同，但它會使用 x、y 和 z 的16位浮點值。
ms.assetid: 2db5fb3e-ffe0-4bcf-8894-a8bc7eefaf82
title: 'D3DXVECTOR4_16F 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: d3d46e6bc5423260e550fd026ca52420b1c392ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322756"
---
# <a name="d3dxvector4_16f-structure"></a><span data-ttu-id="cb46c-103">D3DXVECTOR4 \_ 16F 結構</span><span class="sxs-lookup"><span data-stu-id="cb46c-103">D3DXVECTOR4\_16F structure</span></span>

<span data-ttu-id="cb46c-104">與 [**D3DXVECTOR4**](d3d10-d3dxvector4.md)相同，但它會使用 x、y 和 z 的16位浮點值。</span><span class="sxs-lookup"><span data-stu-id="cb46c-104">Same as a [**D3DXVECTOR4**](d3d10-d3dxvector4.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb46c-105">語法</span><span class="sxs-lookup"><span data-stu-id="cb46c-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="members"></a><span data-ttu-id="cb46c-106">成員</span><span class="sxs-lookup"><span data-stu-id="cb46c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb46c-107">**x**</span><span class="sxs-lookup"><span data-stu-id="cb46c-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="cb46c-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb46c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cb46c-109">X 元件。</span><span class="sxs-lookup"><span data-stu-id="cb46c-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="cb46c-110">**y**</span><span class="sxs-lookup"><span data-stu-id="cb46c-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="cb46c-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb46c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cb46c-112">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="cb46c-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="cb46c-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="cb46c-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="cb46c-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb46c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cb46c-115">Z 元件。</span><span class="sxs-lookup"><span data-stu-id="cb46c-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="cb46c-116">**w**</span><span class="sxs-lookup"><span data-stu-id="cb46c-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="cb46c-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb46c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cb46c-118">W 元件。</span><span class="sxs-lookup"><span data-stu-id="cb46c-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb46c-119">備註</span><span class="sxs-lookup"><span data-stu-id="cb46c-119">Remarks</span></span>

<span data-ttu-id="cb46c-120">**D3DXVECTOR4 \_ 16F** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="cb46c-120">**D3DXVECTOR4\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector4_16f-extensions"></a><span data-ttu-id="cb46c-121">D3DXVECTOR4 \_ 16F 延伸模組</span><span class="sxs-lookup"><span data-stu-id="cb46c-121">D3DXVECTOR4\_16F Extensions</span></span>


```
typedef struct D3DXVECTOR4_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR4_16F() {};
    D3DXVECTOR4_16F( CONST FLOAT * );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR4_16F( CONST D3DXVECTOR3_16F& xyz, CONST D3DXFLOAT16& w );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16& x, CONST D3DXFLOAT16& y, CONST D3DXFLOAT16& z, CONST D3DXFLOAT16& w );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR4_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR4_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z, w;

} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="requirements"></a><span data-ttu-id="cb46c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb46c-122">Requirements</span></span>



| <span data-ttu-id="cb46c-123">需求</span><span class="sxs-lookup"><span data-stu-id="cb46c-123">Requirement</span></span> | <span data-ttu-id="cb46c-124">值</span><span class="sxs-lookup"><span data-stu-id="cb46c-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb46c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cb46c-125">Header</span></span><br/> | <dl> <span data-ttu-id="cb46c-126"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb46c-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb46c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb46c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb46c-128">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="cb46c-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
