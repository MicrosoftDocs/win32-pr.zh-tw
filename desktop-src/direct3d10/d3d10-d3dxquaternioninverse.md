---
description: D3DXQuaternionInverse 函數 (D3DX10Math) -Conjugates 和 renormalizes 四元數。
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: 'D3DXQuaternionInverse 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 84816ac72841dcda0aef726535b7f5219d5467e4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103196"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a>D3DXQuaternionInverse 函式 (D3DX10Math) 

Conjugates 和 renormalizes 四元數。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。

</dd> <dt>

*pQ* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

來源 D3DXQUATERNION 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

D3DXQUATERNION 結構的指標，此結構是四元數的反向四元數。

## <a name="remarks"></a>備註


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXQuaternionInverse 函式就可以用來做為另一個函式的參數。

針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
