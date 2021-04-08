---
description: 計算指數。
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: 'D3DXQuaternionExp 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d00292cc073679e3e90c2470630ba1851d0d3cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696727"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a>D3DXQuaternionExp 函式 (D3DX10Math) 

計算指數。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionExp(
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

D3DXQUATERNION 結構的指標，其為指數。

## <a name="remarks"></a>備註

這個方法會將純四元數轉換成單位四元數。 D3DXQuaternionExp 需要純四元數，其中 w 會忽略計算 (w = = 0) 。


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



其中 v 是四元數的向量部分。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXQuaternionExp 函式就可以用來做為另一個函式的參數。

[**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md)方法也可以用來設定四元數的控制點。

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

 

 
