---
title: WavePrefixSum 函式
description: 傳回使用中通道的所有值加上小於此值的總和。
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- WavePrefixSum 函式 HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbb9ced3fbf7e150cbe3b9bca7eb176e61cf6c8881def22a977ae37a2dbf4b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671088"
---
# <a name="waveprefixsum-function"></a>WavePrefixSum 函式

傳回使用中通道的所有值加上小於此值的總和。

## <a name="syntax"></a>語法

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>參數

*value* 

要加總的值。

## <a name="return-value"></a>傳回值

值的總和。

## <a name="remarks"></a>備註

無法保證此常式上的作業順序。 如此一來，就能有效地 \[ \] 在其中忽略精確的旗標。

您可以藉由將前置詞加總新增至目前通道的值來計算後置總和。

請注意，具有最低索引的使用中通道一律會收到0的前置詞總和。

所有著色器階段中的著色器模型6.0 都支援此函數。 

## <a name="examples"></a>範例

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

在 wave 大小為8的電腦上，如果通道0和4以外的所有通道都在作用中，則會從 WavePrefixSum 傳回下列值。

| 通道索引 | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | 非使用中 | n/a           |
| 1          | 作用中   | = 0           |
| 2          | 作用中   | = 0 + 2         |
| 3          | 作用中   | = 0 + 2 + 2       |
| 4          | 非使用中 | n/a           |
| 5          | 作用中   | = 0 + 2 + 2 + 2     |
| 6          | 作用中   | = 0 + 2 + 2 + 2 + 2   |
| 7          | 作用中   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>另請參閱

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[著色器模型6](shader-model-6-0.md)
