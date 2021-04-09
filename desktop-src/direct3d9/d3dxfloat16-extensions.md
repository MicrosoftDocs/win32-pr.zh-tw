---
description: 提供 D3DXFLOAT16 結構的運算子多載和類型轉換。
ms.assetid: d287efb5-d15e-46dc-924d-012e1a108efc
title: 'D3DXFLOAT16 Extensions (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f97e8917f453e7c2c2db99b8f894d557d7b7909f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035348"
---
# <a name="d3dxfloat16-extensions"></a><span data-ttu-id="dbe1c-103">D3DXFLOAT16 延伸模組</span><span class="sxs-lookup"><span data-stu-id="dbe1c-103">D3DXFLOAT16 Extensions</span></span>

<span data-ttu-id="dbe1c-104">提供 [**D3DXFLOAT16**](d3dxfloat16.md) 結構的運算子多載和類型轉換。</span><span class="sxs-lookup"><span data-stu-id="dbe1c-104">Supplies operator overloads and type casts for [**D3DXFLOAT16**](d3dxfloat16.md) structures.</span></span>

``` syntax
typedef struct D3DXFLOAT16
{
#ifdef __cplusplus
public:
    D3DXFLOAT16() {};
    D3DXFLOAT16( FLOAT );
    D3DXFLOAT16( CONST D3DXFLOAT16& );

    // casting
    operator FLOAT ();

    // binary operators
    BOOL operator == ( CONST D3DXFLOAT16& ) const;
    BOOL operator != ( CONST D3DXFLOAT16& ) const;

protected:
#endif //__cplusplus
    WORD value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```

<span data-ttu-id="dbe1c-105">衍生類型： \* LPD3DXFLOAT16</span><span class="sxs-lookup"><span data-stu-id="dbe1c-105">Derived types: \*LPD3DXFLOAT16</span></span>

## <a name="members"></a><span data-ttu-id="dbe1c-106">成員</span><span class="sxs-lookup"><span data-stu-id="dbe1c-106">Members</span></span>

<span data-ttu-id="dbe1c-107">如需結構成員的詳細資訊，請參閱 D3DXFLOAT16。</span><span class="sxs-lookup"><span data-stu-id="dbe1c-107">For more information about structure members, refer to D3DXFLOAT16.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe1c-108">備註</span><span class="sxs-lookup"><span data-stu-id="dbe1c-108">Remarks</span></span>

<span data-ttu-id="dbe1c-109">此結構的運算子多載和類型轉換會在 d3dx9math. .inl 中執行。</span><span class="sxs-lookup"><span data-stu-id="dbe1c-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe1c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbe1c-110">Requirements</span></span>



| <span data-ttu-id="dbe1c-111">需求</span><span class="sxs-lookup"><span data-stu-id="dbe1c-111">Requirement</span></span> | <span data-ttu-id="dbe1c-112">值</span><span class="sxs-lookup"><span data-stu-id="dbe1c-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe1c-113">標頭</span><span class="sxs-lookup"><span data-stu-id="dbe1c-113">Header</span></span><br/> | <dl> <span data-ttu-id="dbe1c-114"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe1c-114"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe1c-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbe1c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe1c-116">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="dbe1c-116">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




