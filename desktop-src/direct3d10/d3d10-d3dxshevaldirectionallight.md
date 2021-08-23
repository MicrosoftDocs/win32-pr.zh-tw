---
description: D3DXSHEvalDirectionalLight 函式 (D3DX10) -評估方向輕量，並傳回光譜的球面調和 (SH) 資料。
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: 'D3DXSHEvalDirectionalLight 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fb50ac274455c67da00d73f91319c0fa17ae85c46f74f4ef605af33e0085ddd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990888"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a>D3DXSHEvalDirectionalLight 函式 (D3DX10) 

評估方向輕量，並傳回光譜的球面調和 (SH) 資料。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
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

SH 評估的順序。 必須在 D3DXSH \_ MINORDER 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*pDir* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

要在其中評估 SH 基礎函數的 (x，y，z) 半球軸方向向量的指標。 請參閱＜備註＞。

</dd> <dt>

*RIntensity* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

光線的紅色濃度。

</dd> <dt>

*GIntensity* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

光線的綠色濃度。

</dd> <dt>

*BIntensity* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

光線的藍色濃度。

</dd> <dt>

*pROut* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

紅色元件的輸出 SH 向量指標。

</dd> <dt>

*pGOut* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

綠色元件之輸出 SH 向量的選擇性指標。

</dd> <dt>

*pBOut* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

藍色元件之輸出 SH 向量的選擇性指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

輸出向量會進行計算，如此一來，如果濃度比率 R/G/B 等於1，則在 >albedo 為1的擴散物件上，點正下方的結果結束 radiance 會是1.0。 這會計算三個光譜範例;將會傳回 pROut，同時會傳回 pGOut 和 pBOut。

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

 

 
