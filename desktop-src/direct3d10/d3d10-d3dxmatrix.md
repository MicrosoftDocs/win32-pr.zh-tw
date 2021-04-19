---
description: 4x4 矩陣，其中包含方法和運算子多載。
ms.assetid: c354d28b-bb08-41c5-bb59-90a912181f0f
title: 'D3DXMATRIX 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: cae887e2e9a8782cdc7ba159db203c929006c58a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974887"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a><span data-ttu-id="aff39-103">D3DXMATRIX 結構 (D3DX10Math .h) </span><span class="sxs-lookup"><span data-stu-id="aff39-103">D3DXMATRIX structure (D3DX10Math.h)</span></span>

<span data-ttu-id="aff39-104">4x4 矩陣，其中包含方法和運算子多載。</span><span class="sxs-lookup"><span data-stu-id="aff39-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff39-105">語法</span><span class="sxs-lookup"><span data-stu-id="aff39-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="aff39-106">成員</span><span class="sxs-lookup"><span data-stu-id="aff39-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aff39-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="aff39-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="aff39-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aff39-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aff39-109">矩陣的 (i，j) 元件，其中 i 是資料列編號，而 j 是資料行編號。</span><span class="sxs-lookup"><span data-stu-id="aff39-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="aff39-110">例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。</span><span class="sxs-lookup"><span data-stu-id="aff39-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aff39-111">備註</span><span class="sxs-lookup"><span data-stu-id="aff39-111">Remarks</span></span>

<span data-ttu-id="aff39-112">C 程式設計人員無法使用 D3DXMATRIX 結構，必須使用 D3DMATRIX 結構。</span><span class="sxs-lookup"><span data-stu-id="aff39-112">C programmers cannot use the D3DXMATRIX structure, they must use the D3DMATRIX structure.</span></span> <span data-ttu-id="aff39-113">C + + 程式設計人員可以利用多載的函式和指派、一元和二元 (包括相等) 運算子。</span><span class="sxs-lookup"><span data-stu-id="aff39-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="aff39-114">在 D3DX 中， \_ 投射矩陣的34元素不能是負數。</span><span class="sxs-lookup"><span data-stu-id="aff39-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="aff39-115">如果您的應用程式需要在這個位置使用負值，則應該改為將整個投射矩陣調整為-1。</span><span class="sxs-lookup"><span data-stu-id="aff39-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="aff39-116">D3DXMATRIX 延伸模組</span><span class="sxs-lookup"><span data-stu-id="aff39-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="aff39-117">**D3DXMATRIX** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="aff39-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
        
```



## <a name="requirements"></a><span data-ttu-id="aff39-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="aff39-118">Requirements</span></span>



| <span data-ttu-id="aff39-119">需求</span><span class="sxs-lookup"><span data-stu-id="aff39-119">Requirement</span></span> | <span data-ttu-id="aff39-120">值</span><span class="sxs-lookup"><span data-stu-id="aff39-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aff39-121">標頭</span><span class="sxs-lookup"><span data-stu-id="aff39-121">Header</span></span><br/> | <dl> <span data-ttu-id="aff39-122"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="aff39-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff39-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aff39-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff39-124">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="aff39-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
