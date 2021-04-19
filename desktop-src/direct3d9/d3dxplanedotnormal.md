---
description: 計算平面和3D 向量的點乘積。 向量的 w 參數會假設為0。
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: 'D3DXPlaneDotNormal 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985529"
---
# <a name="d3dxplanedotnormal-function"></a>D3DXPlaneDotNormal 函式

計算平面和3D 向量的點乘積。 向量的 w 參數會假設為0。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXPlaneDotNormal(
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

給定平面 (a、b、c、d) 和3D 向量 (x、y、z) 此函式的傳回值為 \* x + b \* y + c \* z + d \* 0。 **D3DXPlaneDotNormal** 函式可用來計算平面法線之間的角度，另一個則是正常的。

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

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> </dl>

 

 
