---
description: 針對 D3DXCOLOR 結構提供下列運算子多載和類型轉換。
ms.assetid: 89780c6f-c78b-4ebe-876a-6dbc37b598ef
title: 'D3DXCOLOR Extensions (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7f457332f371b2c452a465c5b831774488301c6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854031"
---
# <a name="d3dxcolor-extensions"></a><span data-ttu-id="78c5c-103">D3DXCOLOR 延伸模組</span><span class="sxs-lookup"><span data-stu-id="78c5c-103">D3DXCOLOR Extensions</span></span>

<span data-ttu-id="78c5c-104">針對 [**D3DXCOLOR**](d3dxcolor.md) 結構提供下列運算子多載和類型轉換。</span><span class="sxs-lookup"><span data-stu-id="78c5c-104">Supplies the following operator overloads and type casts for [**D3DXCOLOR**](d3dxcolor.md) structures.</span></span>

``` syntax
typedef struct D3DXCOLOR
{
#ifdef __cplusplus
public:
    D3DXCOLOR() {}
    D3DXCOLOR( DWORD argb );
    D3DXCOLOR( CONST FLOAT * );
    D3DXCOLOR( CONST D3DXFLOAT16 * );
    D3DXCOLOR( CONST D3DCOLORVALUE& );
    D3DXCOLOR( FLOAT r, FLOAT g, FLOAT b, FLOAT a );

    // casting
    operator DWORD () const;

    operator FLOAT* ();
    operator CONST FLOAT* () const;

    operator D3DCOLORVALUE* ();
    operator CONST D3DCOLORVALUE* () const;

    operator D3DCOLORVALUE& ();
    operator CONST D3DCOLORVALUE& () const;

    // assignment operators
    D3DXCOLOR& operator += ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator -= ( CONST D3DXCOLOR& );
    D3DXCOLOR& operator *= ( FLOAT );
    D3DXCOLOR& operator /= ( FLOAT );

    // unary operators
    D3DXCOLOR operator + () const;
    D3DXCOLOR operator - () const;

    // binary operators
    D3DXCOLOR operator + ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator - ( CONST D3DXCOLOR& ) const;
    D3DXCOLOR operator * ( FLOAT ) const;
    D3DXCOLOR operator / ( FLOAT ) const;

    friend D3DXCOLOR operator * ( FLOAT, CONST D3DXCOLOR& );

    BOOL operator == ( CONST D3DXCOLOR& ) const;
    BOOL operator != ( CONST D3DXCOLOR& ) const;

#endif //__cplusplus
    FLOAT r, g, b, a;
} D3DXCOLOR, *LPD3DXCOLOR;
```

<span data-ttu-id="78c5c-105">衍生類型： \* LPD3DXCOLOR</span><span class="sxs-lookup"><span data-stu-id="78c5c-105">Derived types: \*LPD3DXCOLOR</span></span>

## <a name="members"></a><span data-ttu-id="78c5c-106">成員</span><span class="sxs-lookup"><span data-stu-id="78c5c-106">Members</span></span>

<span data-ttu-id="78c5c-107">如需結構成員的詳細資訊，請參閱 [**D3DXCOLOR**](d3dxcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="78c5c-107">For more information about structure members, refer to [**D3DXCOLOR**](d3dxcolor.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78c5c-108">備註</span><span class="sxs-lookup"><span data-stu-id="78c5c-108">Remarks</span></span>

<span data-ttu-id="78c5c-109">此結構的運算子多載和類型轉換會在 d3dx9math. .inl 中執行。</span><span class="sxs-lookup"><span data-stu-id="78c5c-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

> [!Note]  
> <span data-ttu-id="78c5c-110">當您在 Microsoft Visual Studio 2010 的偵測模式中執行 D3DXCOLOR () 函式時，會在運行 [時間錯誤檢查 (/RTCc) ](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) 編譯器選項時當機。</span><span class="sxs-lookup"><span data-stu-id="78c5c-110">The D3DXCOLOR() constructor crashes at runtime when you run it in debug mode in Microsoft Visual Studio 2010 with the [Run-Time Error Checks (/RTCc)](/previous-versions/visualstudio/visual-studio-2010/8wtf2dfz(v=vs.100)) compiler option.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78c5c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="78c5c-111">Requirements</span></span>



| <span data-ttu-id="78c5c-112">需求</span><span class="sxs-lookup"><span data-stu-id="78c5c-112">Requirement</span></span> | <span data-ttu-id="78c5c-113">值</span><span class="sxs-lookup"><span data-stu-id="78c5c-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78c5c-114">標頭</span><span class="sxs-lookup"><span data-stu-id="78c5c-114">Header</span></span><br/> | <dl> <span data-ttu-id="78c5c-115"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="78c5c-115"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c5c-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78c5c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c5c-117">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="78c5c-117">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
