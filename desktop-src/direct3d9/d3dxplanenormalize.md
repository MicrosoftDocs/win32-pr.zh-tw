---
description: 正規化平面係數，讓平面法線具有單位長度。
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: 'D3DXPlaneNormalize 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986073"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>D3DXPlaneNormalize 函式 (D3dx9math) 

正規化平面係數，讓平面法線具有單位長度。

## <a name="syntax"></a>語法


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXPLANE**](d3dxplane.md)\***

[**D3DXPLANE**](d3dxplane.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pP* \[在\]
</dt> <dd>

Type： **Const [**D3DXPLANE**](d3dxplane.md) \***

來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXPLANE**](d3dxplane.md)\***

[**D3DXPLANE**](d3dxplane.md)結構的指標，代表平面的一般。

## <a name="remarks"></a>備註

此函式會將平面正規化，使 \| a、b、c \| = = 1。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來，此函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




