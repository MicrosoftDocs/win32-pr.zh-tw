---
description: 針對 D3DXPLANE 結構提供下列運算子多載和類型轉換。
ms.assetid: 05f80b68-fb2b-4fd7-94e9-e5b40968c4aa
title: 'D3DXPLANE Extensions (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3ff8f68283cd81e6647fcdea480ac19b48547cab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993854"
---
# <a name="d3dxplane-extensions"></a><span data-ttu-id="86e2d-103">D3DXPLANE 延伸模組</span><span class="sxs-lookup"><span data-stu-id="86e2d-103">D3DXPLANE Extensions</span></span>

<span data-ttu-id="86e2d-104">針對 [**D3DXPLANE**](d3dxplane.md) 結構提供下列運算子多載和類型轉換。</span><span class="sxs-lookup"><span data-stu-id="86e2d-104">Supplies the following operator overloads and type casts for [**D3DXPLANE**](d3dxplane.md) structures.</span></span>

``` syntax
typedef struct D3DXPLANE
{
#ifdef __cplusplus
public:
    D3DXPLANE() {}
    D3DXPLANE( CONST FLOAT* );
    D3DXPLANE( CONST D3DXFLOAT16* );
    D3DXPLANE( FLOAT a, FLOAT b, FLOAT c, FLOAT d );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXPLANE& operator *= ( FLOAT );
    D3DXPLANE& operator /= ( FLOAT );

    // unary operators
    D3DXPLANE operator + () const;
    D3DXPLANE operator - () const;

    // binary operators
    D3DXPLANE operator * ( FLOAT ) const;
    D3DXPLANE operator / ( FLOAT ) const;

    friend D3DXPLANE operator * ( FLOAT, CONST D3DXPLANE& );

    BOOL operator == ( CONST D3DXPLANE& ) const;
    BOOL operator != ( CONST D3DXPLANE& ) const;

#endif //__cplusplus
    FLOAT a, b, c, d;
} D3DXPLANE, *LPD3DXPLANE;
```

<span data-ttu-id="86e2d-105">衍生類型： \* LPD3DXPLANE</span><span class="sxs-lookup"><span data-stu-id="86e2d-105">Derived types: \*LPD3DXPLANE</span></span>

## <a name="remarks"></a><span data-ttu-id="86e2d-106">備註</span><span class="sxs-lookup"><span data-stu-id="86e2d-106">Remarks</span></span>

<span data-ttu-id="86e2d-107">如需結構成員的詳細資訊，請參閱 [**D3DXPLANE**](d3dxplane.md)。</span><span class="sxs-lookup"><span data-stu-id="86e2d-107">For more information about structure members, refer to [**D3DXPLANE**](d3dxplane.md).</span></span>

<span data-ttu-id="86e2d-108">此結構的運算子多載和類型轉換會在 d3dx9math. .inl 中執行。</span><span class="sxs-lookup"><span data-stu-id="86e2d-108">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e2d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="86e2d-109">Requirements</span></span>



| <span data-ttu-id="86e2d-110">需求</span><span class="sxs-lookup"><span data-stu-id="86e2d-110">Requirement</span></span> | <span data-ttu-id="86e2d-111">值</span><span class="sxs-lookup"><span data-stu-id="86e2d-111">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86e2d-112">標頭</span><span class="sxs-lookup"><span data-stu-id="86e2d-112">Header</span></span><br/> | <dl> <span data-ttu-id="86e2d-113"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="86e2d-113"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e2d-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86e2d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e2d-115">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="86e2d-115">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




