---
description: D3DXVec4Hermite 函式 (D3dx9math) -使用指定的4D 向量執行 Hermite 曲線插補。
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: 'D3DXVec4Hermite 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a62d96181b4242073b9e6a2176d841add86cbfeab4238bfb4cbb538bfd88e1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730726"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a>D3DXVec4Hermite 函式 (D3dx9math) 

使用指定的4D 向量執行 Hermite 曲線插補。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。

</dd> <dt>

*pT1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是正切向量。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是位置向量。

</dd> <dt>

*pT2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標，也就是正切向量。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是 Hermite 曲線插補的結果。

## <a name="remarks"></a>備註

**D3DXVec4Hermite** 函式會將 (PositionA、tangentA) 從 (PositionB、tangentB) （使用 Hermite 曲線插補）進行插補。

曲線插補是一種容易簡化的曲線一般化。 此曲線是 Q (s 的函式) 具有下列屬性。

Q (s) = ³ + Bs ² + Cs + D (因此，Q ' (s) = 3 ² + 2Bs + C) 

a) Q (0) = v1，所以 Q ' (0) = t1

b) Q (1) = v2，因此 Q ' (1) = t2

v1 是 pV1 的內容，v2 在 pV2 的內容中，t1 是 pT1 的內容，而 t2 是 pT2 的內容。

這些屬性是用來解決 A、B、C、D。

插入 A、B、C 和 D 的解決方案，以產生 Q (s) 。

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

這會產生：

Q (s) = (2v1-2v2 + t2 + t1) s ³ + (3v2-3v1-2t1-t2) s ² + t1s + v1

可以重新排列為：

Q (s) = (2 秒³-3 秒² + 1) v1 + (-2 ³ + 3 秒²) v2 + (s ³-2-2 ² + s) t1 + (s ³-s ²) t2

Hermite 曲線適合用來控制動畫，因為曲線會透過所有控制點來執行。 此外，因為位置和正切函數是在每個區段的結尾明確指定，所以只要您確定起始位置和正切值符合最後一個區段的結束值，就很容易建立 C2 連續曲線。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXVec4Hermite** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
