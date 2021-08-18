---
title: ddx_fine 函式
description: 計算相對於螢幕空間 x 座標的高精確度部分衍生。 |ddx_fine 函式
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- ddx_fine 函式 HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5735d0e2f13a150b730855bc1308cba6e9f2dac795f6c5fc09000e42a607bec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986668"
---
# <a name="ddx_fine-function"></a>ddx \_ 精細函數

計算相對於螢幕空間 x 座標的高精確度部分衍生。

## <a name="syntax"></a>語法

``` syntax
float ddx_fine(
  in float value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **float**

輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **float**

*值* 的高精確度部分衍生。

## <a name="remarks"></a>備註

您也可以使用下列多載版本：

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




