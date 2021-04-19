---
title: 'D2DSampleInputAtOffset 函式 (D2d1effecthelpers) '
description: 在輸入座標的位移位移上取樣輸入 N。 僅適用于複雜的輸入。
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- D2DSampleInputAtOffset 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993240"
---
# <a name="d2dsampleinputatoffset-function"></a>D2DSampleInputAtOffset 函式

在輸入座標的位移位移上取樣輸入 N。 僅適用于複雜的輸入。

## <a name="syntax"></a>語法

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*N* \[ in\]
</dt> <dd>

輸入編號。

</dd> <dt>

*位移* \[在\]
</dt> <dd>

Uv 位移。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 **float4**，格式為 TEXCOORDN。

## <a name="remarks"></a>備註

下列範例顯示在反白顯示和遮蔽漸層遮罩中使用的函式。

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
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

 

 





