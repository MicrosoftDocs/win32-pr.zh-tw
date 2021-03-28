---
title: AllMemoryBarrierWithGroupSync 函式
description: 封鎖群組中所有線程的執行，直到所有記憶體存取都已完成，且群組中的所有線程都已達到此呼叫。
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- AllMemoryBarrierWithGroupSync 函式 HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022628"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>AllMemoryBarrierWithGroupSync 函式

封鎖群組中所有線程的執行，直到所有記憶體存取都已完成，且群組中的所有線程都已達到此呼叫。

## <a name="syntax"></a>語法

``` syntax
void AllMemoryBarrierWithGroupSync(void);
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




