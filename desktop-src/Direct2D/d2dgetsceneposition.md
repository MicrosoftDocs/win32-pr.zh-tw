---
title: 'D2DGetScenePosition 函式 (D2d1effecthelpers) '
description: 傳回輸入場景位置的值 \_ 。 只有當 D2D \_ 需要 \_ 場景 \_ 位置在原始程式檔中宣告時，才可使用。
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- D2DGetScenePosition 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995060"
---
# <a name="d2dgetsceneposition-function"></a>D2DGetScenePosition 函式

傳回輸入場景位置的值 \_ 。 只有當 D2D \_ 需要 \_ 場景 \_ 位置在原始程式檔中宣告時，才可使用。

## <a name="syntax"></a>語法

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

函數會傳回格式場景位置的 **float4** \_ 。

## <a name="remarks"></a>備註

下列範例示範如何在產生溶解模式時使用函數。

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
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

 

 





