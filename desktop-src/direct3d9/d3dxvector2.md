---
description: 描述包含運算子多載和類型轉換的雙元件向量。
ms.assetid: e61ec1c8-00b5-491f-8fb1-be97218f6c68
title: 'D3DXVECTOR2 結構 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7f54dc67c038d7c22929b67c59e6b0331a5e545
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106977141"
---
# <a name="d3dxvector2-structure-d3dx9mathh"></a><span data-ttu-id="c4079-103">D3DXVECTOR2 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="c4079-103">D3DXVECTOR2 structure (D3dx9math.h)</span></span>

<span data-ttu-id="c4079-104">描述包含運算子多載和類型轉換的雙元件向量。</span><span class="sxs-lookup"><span data-stu-id="c4079-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4079-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4079-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="c4079-106">成員</span><span class="sxs-lookup"><span data-stu-id="c4079-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4079-107">**x**</span><span class="sxs-lookup"><span data-stu-id="c4079-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="c4079-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4079-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c4079-109">X 元件。</span><span class="sxs-lookup"><span data-stu-id="c4079-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="c4079-110">**y**</span><span class="sxs-lookup"><span data-stu-id="c4079-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="c4079-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4079-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c4079-112">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="c4079-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4079-113">備註</span><span class="sxs-lookup"><span data-stu-id="c4079-113">Remarks</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="c4079-114">D3DXVECTOR2 延伸模組</span><span class="sxs-lookup"><span data-stu-id="c4079-114">D3DXVECTOR2 Extensions</span></span>

<span data-ttu-id="c4079-115">D3DXVECTOR2 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="c4079-115">D3DXVECTOR2 has the following C++ extensions.</span></span>


```
typedef struct D3DXVECTOR2
{
#ifdef __cplusplus
public:
    D3DXVECTOR2() {};
    D3DXVECTOR2( CONST FLOAT * );
    D3DXVECTOR2( CONST D3DXFLOAT16 * );
    D3DXVECTOR2( FLOAT x, FLOAT y );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR2& operator += ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator -= ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator *= ( FLOAT );
    D3DXVECTOR2& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR2 operator + () const;
    D3DXVECTOR2 operator - () const;

    // binary operators
    D3DXVECTOR2 operator + ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator - ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator * ( FLOAT ) const;
    D3DXVECTOR2 operator / ( FLOAT ) const;

    friend D3DXVECTOR2 operator * ( FLOAT, CONST D3DXVECTOR2& );

    BOOL operator == ( CONST D3DXVECTOR2& ) const;
    BOOL operator != ( CONST D3DXVECTOR2& ) const;


public:
#endif //__cplusplus
    FLOAT x, y;
} D3DXVECTOR2, *LPD3DXVECTOR2;

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



## <a name="requirements"></a><span data-ttu-id="c4079-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4079-116">Requirements</span></span>



| <span data-ttu-id="c4079-117">需求</span><span class="sxs-lookup"><span data-stu-id="c4079-117">Requirement</span></span> | <span data-ttu-id="c4079-118">值</span><span class="sxs-lookup"><span data-stu-id="c4079-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4079-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c4079-119">Header</span></span><br/> | <dl> <span data-ttu-id="c4079-120"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4079-120"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4079-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4079-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4079-122">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="c4079-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
