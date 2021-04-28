---
description: D3DXSHEvalSphericalLight 函式 (D3DX10) -評估球面燈，並傳回光譜的球面調和 (SH) 資料。
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: 'D3DXSHEvalSphericalLight 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1e509ea4695f143bd5399cbda004bcba53f514c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108556"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a>D3DXSHEvalSphericalLight 函式 (D3DX10) 

評估球面燈，並傳回光譜的球面調和 (SH) 資料。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
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

*pPos* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

光線位置的指標。

</dd> <dt>

*Radius* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

球形燈光來源的半徑。

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

評估球面燈並傳回光譜 SH 資料。 這種光線的亮度沒有正規化，就像方向燈一樣，所以在指定濃度時必須小心。 這會計算三個光譜範例;將會傳回 pROut，同時會傳回 pGOut 和 pBOut。

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

 

 
