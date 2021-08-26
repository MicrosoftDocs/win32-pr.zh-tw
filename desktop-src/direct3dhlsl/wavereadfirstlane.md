---
title: WaveReadLaneFirst 函式
description: 傳回目前 wave （具有最小索引）之使用中通道的運算式值。
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- WaveReadLaneFirst 函式 HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b7b8e22cb17db4bdb2d692dc003baf63a6c6836c7d1a05a67444d254940e342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948908"
---
# <a name="wavereadlanefirst-function"></a>WaveReadLaneFirst 函式

傳回目前 wave （具有最小索引）之使用中通道的運算式值。

## <a name="syntax"></a>語法

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*expr* 
</dt> <dd>

要評估的運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

產生的值會在 wave 之間保持一致。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




