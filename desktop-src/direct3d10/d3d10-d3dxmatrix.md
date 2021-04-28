---
description: D3DXMATRIX 結構 (D3DX10Math .h) -包含方法和運算子多載的4x4 矩陣。
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
ms.openlocfilehash: ba1b9533fe5dfa2cfd163a1f92b34a43d7dbd741
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113226"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a>D3DXMATRIX 結構 (D3DX10Math .h) 

4x4 矩陣，其中包含方法和運算子多載。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a>成員

<dl> <dt>

**\_Ij**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

矩陣的 (i，j) 元件，其中 i 是資料列編號，而 j 是資料行編號。 例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。

</dd> </dl>

## <a name="remarks"></a>備註

C 程式設計人員無法使用 D3DXMATRIX 結構，必須使用 D3DMATRIX 結構。 C + + 程式設計人員可以利用多載的函式和指派、一元和二元 (包括相等) 運算子。

在 D3DX 中， \_ 投射矩陣的34元素不能是負數。 如果您的應用程式需要在這個位置使用負值，則應該改為將整個投射矩陣調整為-1。

### <a name="d3dxmatrix-extensions"></a>D3DXMATRIX 延伸模組

**D3DXMATRIX** 具有下列 c + + 擴充功能。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
