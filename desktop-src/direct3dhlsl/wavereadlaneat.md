---
title: WaveReadLaneAt 函式
description: 傳回指定 wave 內給定通道索引的運算式值。
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt 函式 HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2020
ms.locfileid: "104374896"
---
# <a name="wavereadlaneat-function"></a>WaveReadLaneAt 函式

傳回指定 wave 內給定通道索引的運算式值。

## <a name="syntax"></a>語法

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*expr* 
</dt> <dd>

要評估的運算式。

</dd> <dt>

*laneIndex* 
</dt> <dd>

將傳回其 *expr* 結果之通道的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

產生的值是 *expr* 的結果。 如果 *laneIndex* 是統一的，則會是統一的。

## <a name="remarks"></a>備註

此函數實際上是 laneIndex'th 通道中的值廣播。

著色器模型6.0 支援下列著色器類型中的函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




