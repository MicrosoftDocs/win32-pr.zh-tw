---
title: 'D2DGetInput 函式 (D2d1effecthelpers) '
description: 傳回輸入座標的輸入 N 的色彩。 僅適用于簡單的輸入。
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- D2DGetInput 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37de536eb6ac36af3e8aa1ffca61c3840cf6c84e585466a56a447522c4d628d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075312"
---
# <a name="d2dgetinput-function"></a>D2DGetInput 函式

傳回輸入座標的輸入 N 的色彩。 僅適用于簡單的輸入。

## <a name="syntax"></a>語法

``` syntax
float4 WINAPI D2DGetInput(
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

函數會傳回 **float4**，其中包含 INPUTN 格式的 RGBA 色彩。

## <a name="remarks"></a>備註

下列範例顯示在算術複合效果中使用的函數。

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

此外，如需使用此函數的另一個範例，請參閱 [D2D \_ PS \_ 專案](d2d-ps-entry.md) 的備註。

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

 

 





