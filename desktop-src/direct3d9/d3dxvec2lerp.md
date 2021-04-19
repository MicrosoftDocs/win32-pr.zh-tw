---
description: 在兩個2D 向量之間執行線性插補。
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: 'D3DXVec2Lerp 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08b767993143db3057985140b97854b9203d2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982874"
---
# <a name="d3dxvec2lerp-function"></a>D3DXVec2Lerp 函式

在兩個2D 向量之間執行線性插補。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以線性方式在向量之間插補的參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是線性插補的結果。

## <a name="remarks"></a>備註

此函式會根據下列公式執行線性插補： V1 + s (V2-V1) 。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec2Lerp** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
