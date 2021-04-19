---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: 定義常數，以指定運算子的指定軸的方向 (例如，加總，選取最小的專案，然後選取) 的最小元素。
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_AXIS_DIRECTION
ms.openlocfilehash: 18cd2189f88378245be0824e0a68e5f618008bc7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106985794"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a>DML_AXIS_DIRECTION 列舉 (directml .h) 

定義常數，以指定運算子的指定軸的方向 (例如，加總，選取最小的專案，然後選取) 的最小元素。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>Syntax
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a>常數

| Name | 描述 |
| ---- |:---- |
| DML_AXIS_DIRECTION_INCREASING | 指定從低索引到高索引) 的遞增順序 (。 |
| DML_AXIS_DIRECTION_DECREASING | 指定從高索引到低索引) 的遞減順序 (。 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |