---
description: D3DXVECTOR3 結構 (D3dx9math) -描述包含運算子多載和類型轉換的三個元件向量。
ms.assetid: 4d73de4b-82fe-452a-8a1e-17208f172a03
title: 'D3DXVECTOR3 結構 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 29d6743f0c0c365911ebbbba66cb4d44f10792e7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097576"
---
# <a name="d3dxvector3-structure-d3dx9mathh"></a><span data-ttu-id="b9780-103">D3DXVECTOR3 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="b9780-103">D3DXVECTOR3 structure (D3dx9math.h)</span></span>

<span data-ttu-id="b9780-104">描述包含運算子多載和類型轉換的三個元件向量。</span><span class="sxs-lookup"><span data-stu-id="b9780-104">Describes a three-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9780-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9780-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
```



## <a name="members"></a><span data-ttu-id="b9780-106">成員</span><span class="sxs-lookup"><span data-stu-id="b9780-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9780-107">**x**</span><span class="sxs-lookup"><span data-stu-id="b9780-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="b9780-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9780-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9780-109">X 元件。</span><span class="sxs-lookup"><span data-stu-id="b9780-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="b9780-110">**y**</span><span class="sxs-lookup"><span data-stu-id="b9780-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="b9780-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9780-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9780-112">Y 元件。</span><span class="sxs-lookup"><span data-stu-id="b9780-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="b9780-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="b9780-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="b9780-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9780-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9780-115">Z 元件。</span><span class="sxs-lookup"><span data-stu-id="b9780-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9780-116">備註</span><span class="sxs-lookup"><span data-stu-id="b9780-116">Remarks</span></span>

### <a name="d3dxvector3-extensions"></a><span data-ttu-id="b9780-117">D3DXVECTOR3 延伸模組</span><span class="sxs-lookup"><span data-stu-id="b9780-117">D3DXVECTOR3 Extensions</span></span>

<span data-ttu-id="b9780-118">D3DXVECTOR3 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b9780-118">D3DXVECTOR3 has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXVECTOR3 : public D3DVECTOR
{
public:
    D3DXVECTOR3() {};
    D3DXVECTOR3( CONST FLOAT * );
    D3DXVECTOR3( CONST D3DVECTOR& );
    D3DXVECTOR3( CONST D3DXFLOAT16 * );
    D3DXVECTOR3( FLOAT x, FLOAT y, FLOAT z );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR3& operator += ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator -= ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator *= ( FLOAT );
    D3DXVECTOR3& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR3 operator + () const;
    D3DXVECTOR3 operator - () const;

    // binary operators
    D3DXVECTOR3 operator + ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator - ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator * ( FLOAT ) const;
    D3DXVECTOR3 operator / ( FLOAT ) const;

    friend D3DXVECTOR3 operator * ( FLOAT, CONST struct D3DXVECTOR3& );

    BOOL operator == ( CONST D3DXVECTOR3& ) const;
    BOOL operator != ( CONST D3DXVECTOR3& ) const;

} D3DXVECTOR3, *LPD3DXVECTOR3;

#else //!__cplusplus
typedef struct _D3DVECTOR D3DXVECTOR3, *LPD3DXVECTOR3;
#endif //!__cplusplus

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



## <a name="requirements"></a><span data-ttu-id="b9780-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9780-119">Requirements</span></span>



| <span data-ttu-id="b9780-120">需求</span><span class="sxs-lookup"><span data-stu-id="b9780-120">Requirement</span></span> | <span data-ttu-id="b9780-121">值</span><span class="sxs-lookup"><span data-stu-id="b9780-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9780-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b9780-122">Header</span></span><br/> | <dl> <span data-ttu-id="b9780-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9780-123"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9780-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9780-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9780-125">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="b9780-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
