---
description: 描述包含運算子多載和類型轉換的雙元件向量。 與 D3DXVECTOR2 相同，但它會使用 x、y 和 z 的16位浮點值。
ms.assetid: b410d2e1-a006-4563-928a-c9000f73c224
title: 'D3DXVECTOR2_16F 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e7d1c24b40674fe2df202a0cdea42dc7ad96728a8710c21e443642c8b6152cea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120258"
---
# <a name="d3dxvector2_16f-structure"></a>D3DXVECTOR2 \_ 16F 結構

描述包含運算子多載和類型轉換的雙元件向量。 與 [**D3DXVECTOR2**](d3d10-d3dxvector2.md)相同，但它會使用 x、y 和 z 的16位浮點值。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXVECTOR2_16F {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="members"></a>成員

<dl> <dt>

**x**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

X 元件。

</dd> <dt>

**y**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Y 元件。

</dd> </dl>

## <a name="remarks"></a>備註

**D3DXVECTOR2 \_ 16F** 具有下列 c + + 擴充功能。

### <a name="d3dxvector2_16f-extensions"></a>D3DXVECTOR2 \_ 16F 延伸模組


```

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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
