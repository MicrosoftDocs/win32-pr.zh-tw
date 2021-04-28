---
description: D3DXSHEvalDirection 函式 (D3dx9math) -從輸入方向向量評估球面調和 (SH) 基礎函數。
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: 'D3DXSHEvalDirection 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e02f0f3d8770b4b703f275de3225eacb301a7843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093957"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a>D3DXSHEvalDirection 函式 (D3dx9math) 

從輸入方向向量評估球面調和 (SH) 基礎函數。

## <a name="syntax"></a>語法


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

球面調和 (SH) 輸出係數的指標。 評估會產生順序²係數。 請參閱＜備註＞。

</dd> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*pDir* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

 (x，y，z) 方向向量，用來評估 SH 基礎函數。 必須正規化。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

SH 輸出係數的指標。 請參閱＜備註＞。

## <a name="remarks"></a>備註

基礎函數 Ylm 的每個係數都會儲存在記憶體位置 l ² + m + l，其中：

-   l 是基礎函數的程度。
-   m 是指定 l 值的基礎函數索引，範圍從-l 到 l （含）。

如下圖所示，在具有單位半徑的球體上，可以只使用 theta、 [右邊](coordinate-systems.md)的 Z 軸角度和 phi （z 的角度）來指定方向。

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。 角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[預先計算 Radiance Transfer (Direct3D 9) ](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
