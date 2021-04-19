---
title: 'D2DSampleInput 函式 (D2d1effecthelpers) '
description: 在位置 uv 的輸入 N 範例。 僅適用于複雜的輸入。
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- D2DSampleInput 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983207"
---
# <a name="d2dsampleinput-function"></a>D2DSampleInput 函式

在位置 uv 的輸入 N 範例。 僅適用于複雜的輸入。

## <a name="syntax"></a>語法

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*N* \[ in\]
</dt> <dd>

輸入編號。

</dd> <dt>

*uv* \[在\]
</dt> <dd>

Uv 位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 **float4**，格式為 TEXCOORDN。

## <a name="remarks"></a>備註

下列範例顯示用來計算表面法線的函數。

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
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

 

 





