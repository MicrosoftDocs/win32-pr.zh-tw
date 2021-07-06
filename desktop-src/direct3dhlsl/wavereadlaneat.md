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
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316480"
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

此函式實際上是 *laneIndex* 的第一個通道中的值廣播。

所有著色器階段中的著色器模型6.0 都支援此函數。

## <a name="see-also"></a>另請參閱

* [著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [著色器模型6](shader-model-6-0.md)
