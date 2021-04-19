---
description: 使用指定的3D 向量，傳回 Barycentric 座標中的點。
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: 'D3DXVec3BaryCentric 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3c14d01acc71a13cabb810d5b26d0afaf7f67f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989198"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a>D3DXVec3BaryCentric 函式 (D3DX10Math) 

使用指定的3D 向量，傳回 Barycentric 座標中的點。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _In_       D3DXVECTOR3 *pOut,
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2,
  _In_ const D3DXVECTOR3 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 結構的指標。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 結構的指標。

</dd> <dt>

*pV3* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 結構的指標。

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

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Barycentric 座標中 D3DXVECTOR3 結構的指標。

## <a name="remarks"></a>備註

D3DXVec3BaryCentric 函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。 此函式會使用下列方程式傳回結果點： V1 + f (V2-V1) + g (V3-V1) 。

平面 V1V2V3 中的任何點都可由 Barycentric 座標 (f，g) 表示。參數 f 控制要將多少 V2 加權至結果，而參數 g 控制在結果中加權多少 V3。 最後，1-f-g 控制 V1 在結果中的加權量。

請注意下列關聯性。

-   如果 (f>= 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於三角形 V1V2V3 內。
-   如果 (f = = 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於行 V1V3 上。
-   如果 (f>= 0 &，& g = = 0 &，& 1-f-g>= 0) ，則點位於行 V1V2 上。
-   如果 (f>= 0 &，& g>= 0 &，& 1-f-g = = 0) ，則點位於行 V2V3 上。

Barycentric 座標是一種一般座標形式。 在此內容中，使用 Barycentric 座標代表座標系統中的變更。 笛卡兒座標的 true 是 Barycentric 座標的 true。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXVec3BaryCentric 函式就可以用來做為另一個函式的參數。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
