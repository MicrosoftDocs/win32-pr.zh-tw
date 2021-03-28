---
title: WavePrefixProduct 函式
description: 使用小於此通道的索引，傳回這個波中使用中通道內所有值的乘積。
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- WavePrefixProduct 函式 HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383282"
---
# <a name="waveprefixproduct-function"></a>WavePrefixProduct 函式

使用小於此通道的索引，傳回這個波中使用中通道內所有值的乘積。

## <a name="syntax"></a>語法

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>參數

*value* 

要相乘的值。

## <a name="return-value"></a>傳回值

所有值的乘積。

## <a name="remarks"></a>備註

無法保證此常式上的作業順序。 如此一來，就能有效地 \[ \] 在其中忽略精確的旗標。

您可以藉由將前置乘積乘以目前通道的值來計算後置產品。

請注意，具有最低索引的使用中通道一律會收到其前置產品的1。

所有著色器階段中的著色器模型6.0 都支援此函數。 

## <a name="examples"></a>範例

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

在 wave 大小為8的電腦上，如果通道0和4以外的所有通道都在作用中，則會從 WavePrefixProduct 傳回下列值。

| 通道索引 | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | 非使用中 | n/a           |
| 1          | 作用中   |  = 1           |
| 2          | 作用中   | = 1 \* 2        |
| 3          | 作用中   | = 1 \* 2 \* 2     |
| 4          | 非使用中 | n/a           |
| 5          | 作用中   | = 1 \* 2 \* 2 2 \*       |
| 6          | 作用中   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | 作用中   | = 1 2 2 2 2 2 2 \* \* \* \* \* |

## <a name="see-also"></a>另請參閱

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[著色器模型6](shader-model-6-0.md)
