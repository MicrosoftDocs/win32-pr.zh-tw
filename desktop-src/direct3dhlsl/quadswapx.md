---
title: QuadReadAcrossX 函式
description: 傳回指定的區域值，此值會從這個四的 X 方向中的另一個通道讀取。
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- QuadReadAcrossX 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86a2f525a79fa2458e4f7e0ef44379053e03128782d2625e1bdceb23ec518b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672438"
---
# <a name="quadreadacrossx-function"></a>QuadReadAcrossX 函式

傳回指定的區域值，此值會從這個四的 X 方向中的另一個通道讀取。

## <a name="syntax"></a>語法

``` syntax
<type> QuadReadAcrossX(
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

指定的區域值。 如果來源通道為非使用中，則結果為未定義。

## <a name="remarks"></a>備註

如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。

只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




