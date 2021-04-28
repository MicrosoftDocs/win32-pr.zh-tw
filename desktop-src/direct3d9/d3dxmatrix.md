---
description: D3DXMATRIX 結構 (D3dx9math .h) -包含方法和運算子多載的4x4 矩陣。
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: 'D3DXMATRIX 結構 (D3dx9math .h) '
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
- d3dx9math.h
ms.openlocfilehash: fad44c13f7b856270fe6475f9e099f6e1714e064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094216"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a><span data-ttu-id="a2038-103">D3DXMATRIX 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="a2038-103">D3DXMATRIX structure (D3dx9math.h)</span></span>

<span data-ttu-id="a2038-104">4x4 矩陣，其中包含方法和運算子多載。</span><span class="sxs-lookup"><span data-stu-id="a2038-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2038-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2038-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="a2038-106">成員</span><span class="sxs-lookup"><span data-stu-id="a2038-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2038-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="a2038-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="a2038-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2038-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a2038-109">矩陣的 (i，j) 元件，其中 i 是資料列編號，而 j 是資料行編號。</span><span class="sxs-lookup"><span data-stu-id="a2038-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="a2038-110">例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。</span><span class="sxs-lookup"><span data-stu-id="a2038-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2038-111">備註</span><span class="sxs-lookup"><span data-stu-id="a2038-111">Remarks</span></span>

<span data-ttu-id="a2038-112">C 程式設計人員無法使用 D3DXMATRIX 結構，必須使用 [**D3DMATRIX**](d3dmatrix.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="a2038-112">C programmers cannot use the D3DXMATRIX structure, they must use the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="a2038-113">C + + 程式設計人員可以利用多載的函式和指派、一元和二元 (包括相等) 運算子。</span><span class="sxs-lookup"><span data-stu-id="a2038-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="a2038-114">在 D3DX 中， \_ 投射矩陣的34元素不能是負數。</span><span class="sxs-lookup"><span data-stu-id="a2038-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="a2038-115">如果您的應用程式需要在這個位置使用負值，則應該改為將整個投射矩陣調整為-1。</span><span class="sxs-lookup"><span data-stu-id="a2038-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="a2038-116">D3DXMATRIX 延伸模組</span><span class="sxs-lookup"><span data-stu-id="a2038-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="a2038-117">**D3DXMATRIX** 具有下列 c + + 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="a2038-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a2038-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2038-118">Requirements</span></span>



| <span data-ttu-id="a2038-119">需求</span><span class="sxs-lookup"><span data-stu-id="a2038-119">Requirement</span></span> | <span data-ttu-id="a2038-120">值</span><span class="sxs-lookup"><span data-stu-id="a2038-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2038-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a2038-121">Header</span></span><br/> | <dl> <span data-ttu-id="a2038-122"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2038-122"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2038-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2038-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2038-124">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="a2038-124">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a2038-125">**D3DMATRIX**</span><span class="sxs-lookup"><span data-stu-id="a2038-125">**D3DMATRIX**</span></span>](d3dmatrix.md)
</dt> </dl>

 

 
