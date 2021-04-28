---
description: D3DXVec4Normalize 函式 (D3DX10Math) -傳回4D 向量的正規化版本。
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: 'D3DXVec4Normalize 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102906"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a>D3DXVec4Normalize 函式 (D3DX10Math) 

傳回4D 向量的正規化版本。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

作業結果之 [**D3DXVECTOR4**](d3d10-d3dxvector4.md) 的指標。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

來源 D3DXVECTOR4 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

D3DXVECTOR4 結構的指標，此結構是向量的正規化版本。

## <a name="remarks"></a>備註

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXVec4Normalize 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
