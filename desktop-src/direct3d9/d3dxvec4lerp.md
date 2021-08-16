---
description: 在兩個4D 向量之間執行線性插補。
ms.assetid: a068a626-17cd-4df9-8f41-9b417bfda1d1
title: 'D3DXVec4Lerp 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 726bd212947a37d69dd21e6003d550845799e4ac7aba237794d465ad3da5b509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856968"
---
# <a name="d3dxvec4lerp-function"></a>D3DXVec4Lerp 函式

在兩個4D 向量之間執行線性插補。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR4* D3DXVec4Lerp(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
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

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以線性方式在向量之間插補的參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是線性插補的結果。

## <a name="remarks"></a>備註

此函式會根據下列公式執行線性插補： V1 + s (V2-V1) 。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec4Lerp** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
