---
description: 針對 D3DXQUATERNION 結構提供下列運算子多載和類型轉換。
ms.assetid: a49975a4-a9a7-4183-91b3-3d56f70747ef
title: 'D3DXQUATERNION Extensions (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: a937dcf23f894d094fb5f6cc75a765b1d563a1b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991453"
---
# <a name="d3dxquaternion-extensions"></a><span data-ttu-id="90c46-103">D3DXQUATERNION 延伸模組</span><span class="sxs-lookup"><span data-stu-id="90c46-103">D3DXQUATERNION Extensions</span></span>

<span data-ttu-id="90c46-104">針對 [**D3DXQUATERNION**](d3dxquaternion.md) 結構提供下列運算子多載和類型轉換。</span><span class="sxs-lookup"><span data-stu-id="90c46-104">Supplies the following operator overloads and type casts for [**D3DXQUATERNION**](d3dxquaternion.md) structures.</span></span>

``` syntax
typedef struct D3DXQUATERNION
{
#ifdef __cplusplus
public:
    D3DXQUATERNION() {}
    D3DXQUATERNION( CONST FLOAT * );
    D3DXQUATERNION( CONST D3DXFLOAT16 * );
    D3DXQUATERNION( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXQUATERNION& operator += ( CONST D3DXQUATERNION& );
    D3DXQUATERNION& operator -= ( CONST D3DXQUATERNION& );
    D3DXQUATERNION& operator *= ( CONST D3DXQUATERNION& );
    D3DXQUATERNION& operator *= ( FLOAT );
    D3DXQUATERNION& operator /= ( FLOAT );

    // unary operators
    D3DXQUATERNION  operator + () const;
    D3DXQUATERNION  operator - () const;

    // binary operators
    D3DXQUATERNION operator + ( CONST D3DXQUATERNION& ) const;
    D3DXQUATERNION operator - ( CONST D3DXQUATERNION& ) const;
    D3DXQUATERNION operator * ( CONST D3DXQUATERNION& ) const;
    D3DXQUATERNION operator * ( FLOAT ) const;
    D3DXQUATERNION operator / ( FLOAT ) const;

    friend D3DXQUATERNION operator * (FLOAT, CONST D3DXQUATERNION& );

    BOOL operator == ( CONST D3DXQUATERNION& ) const;
    BOOL operator != ( CONST D3DXQUATERNION& ) const;

#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXQUATERNION, *LPD3DXQUATERNION;

```

<span data-ttu-id="90c46-105">衍生類型： \* LPD3DXQUATERNION</span><span class="sxs-lookup"><span data-stu-id="90c46-105">Derived types: \*LPD3DXQUATERNION</span></span>

## <a name="remarks"></a><span data-ttu-id="90c46-106">備註</span><span class="sxs-lookup"><span data-stu-id="90c46-106">Remarks</span></span>

<span data-ttu-id="90c46-107">如需結構成員的詳細資訊，請參閱 [**D3DXQUATERNION**](d3dxquaternion.md)。</span><span class="sxs-lookup"><span data-stu-id="90c46-107">For more information about structure members, refer to [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

<span data-ttu-id="90c46-108">此結構的運算子多載和類型轉換會在 d3dx9math. .inl 中執行。</span><span class="sxs-lookup"><span data-stu-id="90c46-108">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c46-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="90c46-109">Requirements</span></span>



| <span data-ttu-id="90c46-110">需求</span><span class="sxs-lookup"><span data-stu-id="90c46-110">Requirement</span></span> | <span data-ttu-id="90c46-111">值</span><span class="sxs-lookup"><span data-stu-id="90c46-111">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90c46-112">標頭</span><span class="sxs-lookup"><span data-stu-id="90c46-112">Header</span></span><br/> | <dl> <span data-ttu-id="90c46-113"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="90c46-113"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90c46-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90c46-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c46-115">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="90c46-115">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




