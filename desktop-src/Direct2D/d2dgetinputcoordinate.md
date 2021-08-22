---
title: 'D2DGetInputCoordinate 函式 (D2d1effecthelpers) '
description: 傳回輸入 TEXCOORDN 的值。 僅適用于複雜的輸入。
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- D2DGetInputCoordinate 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3fe0d825dea70c8e5211b8c13f1e850fa513670bbc93de98f1f8e2b87ef046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075292"
---
# <a name="d2dgetinputcoordinate-function"></a>D2DGetInputCoordinate 函式

傳回輸入 TEXCOORDN 的值。 僅適用于複雜的輸入。

## <a name="syntax"></a>語法

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*N* \[ in\]
</dt> <dd>

輸入編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 **float4**，格式為 TEXCOORDN。

## <a name="remarks"></a>備註

此函式所傳回的座標在材質空間中。 著色器不應該依賴此值的計算方式。 它只能用來取樣圖元著色器的輸入。 如需詳細資訊，請參閱 [將圖元著色器加入至自訂轉換](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform)。

下列範例顯示用於置換地圖效果的函式。

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果著色器連結](effect-shader-linking.md)
</dt> <dt>

[HLSL 協助程式](hlsl-helpers.md)
</dt> </dl>

 

