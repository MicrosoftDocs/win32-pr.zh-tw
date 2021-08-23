---
description: 計算平面和4D 向量的點乘積。
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: 'D3DXPlaneDot 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4895a94ad50171682a8bd5247694c3b35a56d174b5477f5bbb2a621c1e74fa96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564628"
---
# <a name="d3dxplanedot-function"></a>D3DXPlaneDot 函式

計算平面和4D 向量的點乘積。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pP* \[在\]
</dt> <dd>

Type： **Const [**D3DXPLANE**](d3dxplane.md) \***

來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

平面和4D 向量的點乘積。

## <a name="remarks"></a>備註

給定平面 (a、b、c、d) 和4D 向量 (x、y、z、w) 此函式的傳回值為 \* x + b \* y + c \* z + d \* w。 **D3DXPlaneDot** 函數適合用來判斷平面與同質座標之間的關聯性。 例如，您可以使用這個函式來判斷特定的座標是否在特定的平面上，或特定平面的哪一端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
