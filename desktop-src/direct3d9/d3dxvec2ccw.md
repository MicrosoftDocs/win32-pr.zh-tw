---
description: 採用兩個2D 向量的交叉乘積來傳回 z 元件。
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: 'D3DXVec2CCW 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982878"
---
# <a name="d3dxvec2ccw-function"></a>D3DXVec2CCW 函式

採用兩個2D 向量的交叉乘積來傳回 z 元件。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

Z 元件。

## <a name="remarks"></a>備註

此函式會根據下列公式來判斷交叉乘積，以決定 z 元件： ( (x1、y1、0) cross (x2、y2、0) ) 。 或者，如下列範例所示。


```
pV1->x * pV2->y - pV1->y * pV2->x
```



如果 z 元件的值是正數，則向量 V2 會從向量 V1 中逆時針。 這項資訊適用于背面的挑選。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
