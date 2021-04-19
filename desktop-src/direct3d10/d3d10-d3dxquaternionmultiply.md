---
description: 將兩個四元數相乘。
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: 'D3DXQuaternionMultiply 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 74e10117bf27d922480418e5aa0b8ea60a13528c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974881"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>D3DXQuaternionMultiply 函式 (D3DX10Math) 

將兩個四元數相乘。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。

</dd> <dt>

*pQ1* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 結構的指標。

</dd> <dt>

*pQ2* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)結構的指標，這是兩個四元數的乘積。

## <a name="remarks"></a>備註

結果代表旋轉 Q1，後面接著旋轉 Q2 (Out = Q2 \* q1) 。 這樣做的目的是為了讓 **D3DXQuaternionMultiply** 維持與 [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) 相同的語義，因為可以將單元四元數視為另一種表示旋轉矩陣的方式。

**D3DXQuaternionMultiply** 和 [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md)函數的轉換會以相同順序串連。 例如，假設 mX 和 mY 表示與 qX 和 qY 相同的旋轉，則 m 和 q 都代表相同的旋轉。


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



四元數的乘法不是可交換的。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXQuaternionMultiply** 函式就可以用來做為另一個函式的參數。

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

 

 
