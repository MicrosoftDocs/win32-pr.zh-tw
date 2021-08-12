---
description: D3DXVec4BaryCentric 函式 (D3dx9math) -使用指定的4D 向量，傳回 Barycentric 座標中的點。
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: 'D3DXVec4BaryCentric 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28c8ffc80b908f1ea894a22581c72e4371f87e5f55def2bdb9a1a66cc255ba90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297637"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a>D3DXVec4BaryCentric 函式 (D3dx9math) 

使用指定的4D 向量，傳回 Barycentric 座標中的點。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[擴展\]
</dt> <dd>

類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。

</dd> <dt>

*pV3* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。

</dd> <dt>

*f* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> <dt>

*g* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Barycentric 座標中 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。

## <a name="remarks"></a>備註

**D3DXVec4BaryCentric** 函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。 此函式會使用下列方程式傳回結果點： V1 + f (V2-V1) + g (V3-V1) 。

平面 V1V2V3 中的任何點都可由 Barycentric 座標 (f，g) 表示。參數 *f* 控制要將多少 V2 加權至結果，而參數 *g* 控制在結果中加權多少 V3。 最後，1-f-g 控制 V1 在結果中的加權量。

請注意下列關聯性。

-   如果 (f>= 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於三角形 V1V2V3 內。
-   如果 (f = = 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於行 V1V3 上。
-   如果 (f>= 0 &，& g = = 0 &，& 1-f-g>= 0) ，則點位於行 V1V2 上。
-   如果 (f>= 0 &，& g>= 0 &，& 1-f-g = = 0) ，則點位於行 V2V3 上。

Barycentric 座標是一種一般座標形式。 在此內容中，使用 Barycentric 座標代表座標系統中的變更。 笛卡兒座標的 true 是 Barycentric 座標的 true。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec4BaryCentric** 函式就可以用來做為另一個函式的參數。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
