---
title: WaveIsFirstLane 函式
description: 只針對目前 wave 中具有最小索引的使用中通道傳回 true。
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- WaveIsFirstLane 函式 HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316777"
---
# <a name="waveisfirstlane-function"></a>WaveIsFirstLane 函式

只針對目前 wave 中具有最小索引的使用中通道傳回 true。

## <a name="syntax"></a>語法


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

僅適用于目前 wave 中具有最小索引的現用通道。

## <a name="remarks"></a>備註

您可以使用此函式來識別每個 wave 只執行一次的作業。

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="examples"></a>範例

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




