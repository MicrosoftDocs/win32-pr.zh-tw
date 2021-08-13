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
ms.openlocfilehash: 63b3dfa3ae42ead2088193c42b2eef86c05ebb82c04d4a07162fb26970c5d29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526142"
---
# <a name="d3dxfloat16-extensions"></a>D3DXFLOAT16 延伸模組

提供 [**D3DXFLOAT16**](d3dxfloat16.md) 結構的運算子多載和類型轉換。

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

衍生類型： \* LPD3DXFLOAT16

## <a name="members"></a>成員

如需結構成員的詳細資訊，請參閱 D3DXFLOAT16。

## <a name="remarks"></a>備註

此結構的運算子多載和類型轉換會在 d3dx9math. .inl 中執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




