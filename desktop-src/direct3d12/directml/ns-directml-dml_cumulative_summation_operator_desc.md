---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: 將 tensor 的專案加總在軸上，將總和的執行總和寫入輸出 tensor 中。
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106989106"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a>DML_CUMULATIVE_SUMMATION_OPERATOR_DESC 結構 (directml .h) 

將 tensor 的專案加總在軸上，將總和的執行總和寫入輸出 tensor 中。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含要加總之元素的輸入 tensor。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入所產生累計總和的輸出 tensor。 這個 tensor 的大小和資料類型必須與 *InputTensor* 相同。


`Axis`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

要加總元素之維度的索引。 這個值必須小於 *InputTensor* 的 *DimensionCount* 。


`AxisDirection`

類型： **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)列舉的其中一個值。 如果設定為 **DML_AXIS_DIRECTION_INCREASING**，則會以遞增的元素索引沿著指定的軸沿著 tensor 來進行總和。 如果設定為 **DML_AXIS_DIRECTION_DECREASING**，則反轉為 true，而且會藉由遞減索引來進行專案的總和。


`HasExclusiveSum`




## <a name="remarks"></a>備註
這個運算子支援就地執行，這表示允許 *OutputTensor* 在系結期間為 *InputTensor* 加上別名。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型* 和 *大小*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16、UINT32、UINT16 |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16、UINT32、UINT16 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |