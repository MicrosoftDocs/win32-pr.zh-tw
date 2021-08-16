---
description: 計算平面和3D 向量的點乘積。 向量的 w 參數會假設為1。
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: 'D3DXPlaneDotCoord 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30f04ec310ce66dc43073e724b08c358cd8fc6f24f0b3840475a1abc61544503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524925"
---
# <a name="d3dxplanedotcoord-function"></a>D3DXPlaneDotCoord 函式

計算平面和3D 向量的點乘積。 向量的 w 參數會假設為1。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
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

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

平面和3D 向量的點乘積。

## <a name="remarks"></a>備註

給定平面 (a、b、c、d) 和3D 向量 (x、y、z) 此函式的傳回值為 \* x + b \* y + c \* z + d \* 1。 **D3DXPlaneDotCoord** 函數適合用來判斷平面在3d 空間中的座標關聯性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
