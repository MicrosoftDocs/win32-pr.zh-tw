---
title: EvaluateAttributeSnapped 函式
description: 以位移的圖元距心進行評估。
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- EvaluateAttributeSnapped 函式 HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990671"
---
# <a name="evaluateattributesnapped-function"></a>EvaluateAttributeSnapped 函式

以位移的圖元距心進行評估。

## <a name="syntax"></a>語法

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **attrib 數值**

輸入值。

</dd> <dt>

*位移* \[在\]
</dt> <dd>

類型： **int2**

使用16x16 方格的圖元中心2D 位移。

</dd> </dl>

## <a name="remarks"></a>備註

*Offset* 參數的範圍必須由下列位元組碼定義。

系統只會使用前兩個元件中最少的4個位 (U，V) 的圖元位移。 從4位固定點到 float 的轉換如下 (MSB .。。LSB) ，其中 MSB 是分數的一部分，並決定正負號：

-   1000 =-0.5 f (-8/16) 
-   1001 =-0.4375 f (-7/16) 
-   1010 =-0.375 f (-6/16) 
-   1011 =-0.3125 f (-5/16) 
-   1100 =-0.25 f (-4/16) 
-   1101 =-0.1875 f (-3/16) 
-   1110 =-0.125 f (-2/16) 
-   1111 =-0.0625 f (-1/16) 
-   0000 = 0.0 f ( 0/16) 
-   0001 = 0.0625 f ( 1/16) 
-   0010 = 0.125 f ( 2/16) 
-   0011 = 0.1875 f ( 3/16) 
-   0100 = 0.25 f ( 4/16) 
-   0101 = 0.3125 f ( 5/16) 
-   0110 = 0.375 f ( 6/16) 
-   0111 = 0.4375 f ( 7/16) 

> [!Note]  
> 圖元的左邊和上邊緣包含在位移中;但是，不包含底部和右邊的邊緣。 32位整數中的所有其他位都會被忽略。

 

實值可以採用著色器所提供的位移，並透過執行下列計算，取得完整的32位固定點值 (28.4) （橫跨有效範圍）：


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



如果實作為必須將位移對應至浮點數位移，則會執行下列計算：


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




