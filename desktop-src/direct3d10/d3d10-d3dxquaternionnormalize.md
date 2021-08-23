---
description: D3DXQuaternionNormalize 函數 (D3DX10Math) -計算單位長度四元數。
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: 'D3DXQuaternionNormalize 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b6664c6f5149066822197dd8ac2f76918c204ec5cb9e479b21c9793c885aeff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991098"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a>D3DXQuaternionNormalize 函式 (D3DX10Math) 

計算單位長度四元數。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
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

D3DXQUATERNION 結構的指標，此結構是四元數的標準。

## <a name="remarks"></a>備註

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXQuaternionNormalize 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
