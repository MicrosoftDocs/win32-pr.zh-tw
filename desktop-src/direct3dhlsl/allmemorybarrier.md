---
title: AllMemoryBarrier 函式
description: 封鎖群組中所有線程的執行，直到所有記憶體存取都完成為止。
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- AllMemoryBarrier 函式 HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fc5d22c36d67aa0e8df8352ba8fa6f2d579ddabd4825e6508499420a56bd0ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626748"
---
# <a name="allmemorybarrier-function"></a>AllMemoryBarrier 函式

封鎖群組中所有線程的執行，直到所有記憶體存取都完成為止。

## <a name="syntax"></a>語法

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

記憶體關卡可保證未完成的記憶體作業已完成。 執行緒會在 GroupSync 關卡進行同步處理。 如果記憶體作業正在進行中，這可能會導致執行緒或執行緒停止運作。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




