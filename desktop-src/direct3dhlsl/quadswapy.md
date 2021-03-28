---
title: QuadReadAcrossY 函式
description: 傳回從這個四個 Y 方向的其他通道讀取的指定來源值。
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- QuadReadAcrossY 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971812"
---
# <a name="quadreadacrossy-function"></a>QuadReadAcrossY 函式

傳回從這個四個 Y 方向的其他通道讀取的指定來源值。

## <a name="syntax"></a>語法

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*localValue* 
</dt> <dd>

要求的類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

指定的來源值。 如果來源通道為非使用中，則結果為未定義。

## <a name="remarks"></a>備註

如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。

只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




