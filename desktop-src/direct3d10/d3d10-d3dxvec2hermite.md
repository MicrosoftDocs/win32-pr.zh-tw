---
description: D3DXVec2Hermite 函式 (D3DX10Math) -使用指定的2D 向量執行 Hermite 曲線插補。
ms.assetid: 2d6ff836-a1a7-4cd0-aea3-4fe344f4e211
title: 'D3DXVec2Hermite 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 60e4aef5183e7c107b0853794b9e63c288916763daa4784e21241d55c1bfec89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990708"
---
# <a name="d3dxvec2hermite-function-d3dx10mathh"></a>D3DXVec2Hermite 函式 (D3DX10Math) 

使用指定的2D 向量執行 Hermite 曲線插補。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

來源 D3DXVECTOR2 結構的指標，也就是位置向量。

</dd> <dt>

*pT1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

來源 D3DXVECTOR2 結構的指標，也就是正切向量。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

來源 D3DXVECTOR2 結構的指標，也就是位置向量。

</dd> <dt>

*pT2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

來源 D3DXVECTOR2 結構的指標，也就是正切向量。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

D3DXVECTOR2 結構的指標，此結構是 Hermite 曲線插補的結果。

## <a name="remarks"></a>備註

**D3DXVec2Hermite** 函式會將 (PositionA、tangentA) 從 (PositionB、tangentB) （使用 Hermite 曲線插補）進行插補。

曲線插補是一種容易簡化的曲線一般化。 此曲線是 Q (s 的函式) 具有下列屬性。

Q (s) = ³ + Bs ² + Cs + D (因此，Q ' (s) = 3 ² + 2Bs + C) 

a) Q (0) = v1，所以 Q ' (0) = t1

b) Q (1) = v2，因此 Q ' (1) = t2

v1 是 pV1 的內容，v2 在 pV2 的內容中，t1 是 pT1 的內容，而 t2 是 pT2 的內容。

這些屬性是用來解決 A、B、C、D。


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



插入 A、B、C 和 D 的解決方案，以產生 Q (s) 。


```
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

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXVec2Hermite** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
