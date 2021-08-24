---
title: GroupMemoryBarrierWithGroupSync 函式
description: 封鎖群組中所有線程的執行，直到完成所有群組共用存取，而且群組中的所有線程都已達到此呼叫。
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- GroupMemoryBarrierWithGroupSync 函式 HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbcfdea451c0cb7ad2b84297c422fa6865b1f45d757612a7b5d220a8829a99b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854448"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a>GroupMemoryBarrierWithGroupSync 函式

封鎖群組中所有線程的執行，直到完成所有群組共用存取，而且群組中的所有線程都已達到此呼叫。

## <a name="syntax"></a>語法

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

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

 

 




