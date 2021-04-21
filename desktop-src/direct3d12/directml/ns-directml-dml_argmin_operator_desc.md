---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: 輸出一或多個輸入 tensor 維度內最小值元素的索引。
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: 2e12a81593504a4eb7a0917e545bfa20c70647ff
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804074"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a>DML_ARGMIN_OPERATOR_DESC 結構 (directml .h) 

輸出一或多個輸入 tensor 維度內最小值元素的索引。

每個輸出元素都是在輸入 tensor 的子集上套用 *argmin* 減少的結果。 *Argmin* 函式會輸出一組輸入元素中最小值元素的索引。 每個減少所涉及的輸入元素是由提供的輸入軸所決定。 同樣地，每個輸出索引都與提供的輸入軸有關。 如果指定了所有的輸入軸，則運算子會套用單一 *argmin* 減少，並產生單一的輸出元素。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要從中讀取的 tensor。

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 每個輸出元素都是從 *InputTensor* 的元素子集 *argmin* 減少的結果。

- *DimensionCount* 必須符合 *InputTensor。 DimensionCount* (保留) 的輸入 tensor 的次序。
- *大小* 必須符合 *InputTensor 的大小*，但縮減 *軸* 中包含的維度除外，其大小必須為1。

`AxisCount`

類型： **[UINT](/windows/win32/winprog/windows-data-types)**

要減少的軸數目。 此欄位會決定 *軸* 陣列的大小。

`Axes`

類型： \_ Field_size \_ (AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

要減少的軸。 值必須在範圍內 `[0, InputTensor.DimensionCount - 1]` 。

`AxisDirection`

DML_AXIS_DIRECTION AxisDirection;

類型： **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

決定當多個輸入專案具有相同值時要選取的索引。
- **DML_AXIS_DIRECTION_INCREASING** 會傳回第一個最小值元素的索引 (例如， `argmin({1,2,3,2,1}) = 0`) 
- **DML_AXIS_DIRECTION_DECREASING** 會傳回最後一個最小值元素的索引 (例如， `argmin({1,2,3,2,1}) = 4`) 

## <a name="examples"></a>範例

本節中的範例都使用相同的二維輸入 tensor。

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a>範例 1. 將 *argmin* 套用至資料行

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a>範例 2. 將 *argmin* 套用至資料列

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a>範例 3. 將 *argmin* 套用至所有座標軸 (整個 tensor) 

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>備註
輸出 tensor 的大小必須與輸入 tensor 大小相同，但減少的軸必須是1。

當 [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) *AxisDirection* 時，此 API 相當於 [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc)與 [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function)。

這項功能的子集是透過 [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) 運算子公開，並且在先前的 DirectML 功能層級上受到支援。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputTensor | 輸出 | 1至8 | INT64、INT32、UINT64、UINT32 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |