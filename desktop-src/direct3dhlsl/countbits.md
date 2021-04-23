---
title: countbits 函式
description: 計算輸入整數中的每個元件) 設定 (位數。
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- countbits 函式 HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925621"
---
# <a name="countbits-function"></a>countbits 函式

計算輸入整數中的每個元件) 設定 (位數。

## <a name="syntax"></a>語法

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **uint**

輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint**

位數。

## <a name="remarks"></a>備註

您也可以使用下列多載版本：

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




