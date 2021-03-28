---
title: WaveActiveAnyTrue 函式
description: 如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- WaveActiveAnyTrue 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991030"
---
# <a name="waveactiveanytrue-function"></a>WaveActiveAnyTrue 函式

如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。

## <a name="syntax"></a>語法

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*expr* 
</dt> <dd>

要評估的布林運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果任何通道中的運算式為 true，則為 true。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




