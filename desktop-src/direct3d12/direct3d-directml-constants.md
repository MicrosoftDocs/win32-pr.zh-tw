---
title: DirectML 常數
description: 下列常數是在中宣告 `DirectML.h` 。
keywords:
- 常數
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5f2d95d0eef67309ef1e5902ed6b968616b38bc081bd259d77418e950e4e028f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989598"
---
# <a name="directml-constants"></a>DirectML 常數

下列常數是在中宣告 `DirectML.h` 。

| 常數 | 值 | 描述 |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | 針對 DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0，DirectML 張量支援最多5個維度。 |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | DirectML 張量支援最多8個 DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0 的維度。 |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | 暫存和持續性緩衝區必須有對齊256個位元組的基底位址。 |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | 暫存和持續性緩衝區必須有對齊256個位元組的基底位址。 |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | 緩衝區張量的基本位址對齊需求下限為16個位元組。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | DirectML。h |

## <a name="see-also"></a>另請參閱

* [DirectML 參考](direct3d-directml-reference.md)
* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
