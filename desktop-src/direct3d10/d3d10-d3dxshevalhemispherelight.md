---
description: 評估在球體上兩個色彩之間的線性插補之間的光線。
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: 'D3DXSHEvalHemisphereLight 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323107"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a>D3DXSHEvalHemisphereLight 函式 (D3DX10) 

評估在球體上兩個色彩之間的線性插補之間的光線。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

球形調和 (SH) 評估的順序。 必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*pDir* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

要在其中評估 SH 基礎函數的 (x，y，z) 半球軸方向向量的指標。 請參閱＜備註＞。

</dd> <dt>

*頂端* \[在\]
</dt> <dd>

類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

天空色彩。

</dd> <dt>

*底部* \[在\]
</dt> <dd>

類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

地面色彩。

</dd> <dt>

*pROut* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

紅色元件的輸出 SH 向量指標。

</dd> <dt>

*pGOut* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

綠色元件的輸出 SH 向量指標。

</dd> <dt>

*pBOut* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

藍色元件的輸出 SH 向量指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

插補會在兩個點之間以線性方式完成，而不是在球體的表面上 (也就是，如果軸是 (0，0，1) 它是 Z 中的線性，而不是 azimuthal 角度) 。 產生的球形光源函式會正規化，如此一來，完全擴散表面上的點不會有遮蔽，而且方向 pDir 的一般指示會導致結束 radiance 值為 1 (如果最上層色彩為白色，而底部的色彩為黑色) 。 這是非常簡單的模型，其中 Top 代表「天空」的濃度，而底部代表「地面」的強度。

如下圖所示，在具有單位半徑的球體上，可以只使用 theta、右邊的 Z 軸角度和 phi （z 的角度）來指定方向。

![具有單位半徑之球體的圖例](images/spherical-coordinates.png)

下列方會顯示笛卡兒 (x、y、z) 和球面 (theta 之間的關聯性，以及單位球體上的 phi) 座標。 角度 theta 會因0到 2 pi 的範圍而異，而 phi 則是從0到 pi 的變化。

![笛卡兒和球面座標之間關聯性的方程式](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
