---
title: WaveGetLaneCount 函式
description: 傳回 wave 在此架構上的航道數目。
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- WaveGetLaneCount 函式 HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a177e50ee3c4c9c715ea109faaed72c24e174e4e942059a4dee0dcd0de91a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504736"
---
# <a name="wavegetlanecount-function"></a>WaveGetLaneCount 函式

傳回 wave 在此架構上的航道數目。

## <a name="syntax"></a>語法

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

結果會介於4到128之間，並且包含所有的波浪：作用中、非作用中和/或 helper 通道。 從這個函式傳回的結果可能會因為驅動程式的執行而有很大的差異。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="examples"></a>範例

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




