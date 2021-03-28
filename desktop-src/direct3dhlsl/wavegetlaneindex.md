---
title: WaveGetLaneIndex 函式
description: 傳回目前 wave 內目前通道的索引。
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- WaveGetLaneIndex 函式 HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991031"
---
# <a name="wavegetlaneindex-function"></a>WaveGetLaneIndex 函式

傳回目前 wave 內目前通道的索引。

## <a name="syntax"></a>語法

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

目前的航道索引。 結果會介於0和從 [**WaveGetLaneCount**](wavegetlanecount.md)傳回的結果之間。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




