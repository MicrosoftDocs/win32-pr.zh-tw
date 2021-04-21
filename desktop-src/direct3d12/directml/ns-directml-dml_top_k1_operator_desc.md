---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: 選取每個序列中的最大或最小 *K* 元素，沿著 *InputTensor* 軸，然後分別傳回 *OutputValueTensor* 和 *OutputIndexTensor* 中這些元素的值和索引。
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803814"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>DML_TOP_K1_OPERATOR_DESC 結構 (directml .h) 
選取每個序列中的最大或最小 *K* 元素，沿著 *InputTensor* 軸，然後分別傳回 *OutputValueTensor* 和 *OutputIndexTensor* 中這些元素的值和索引。 *序列* 是指存在於 *InputTensor* 之 *軸* 維度中的其中一個專案集合。

選擇是否要選取最大的 K 元素或最小的 K 元素，都可以使用 *AxisDirection* 來控制。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含要選取之元素的輸入 tensor。

`OutputValueTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

用來將前 *K* 個元素的值寫入其中的輸出 tensor。 依據 *AxisDirection* 的值而定，會根據最大或最小的專案來選取前 *K* 個元素。 此 tensor 的大小必須等於 *InputTensor*，*但**軸* 參數所指定的維度必須等於 *K* 的大小。

如果 *AxisDirection* 是 [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)的，則在每個輸入序列中選取的 *K* 值保證會以遞減方式排序 (最大到最小的) 。 否則，相反的會是 true，而選取的值保證會以遞增方式排序 (最小到最大的) 。

`OutputIndexTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

輸出 tensor，用來將前 *K* 個元素的索引寫入至。 此 tensor 的大小必須等於 *InputTensor*，*但**軸* 參數所指定的維度必須等於 *K* 的大小。

在這個 tensor 中傳回的索引是相對於順序的開頭來測量 (而不是 tensor) 的開頭。 例如，索引0一律會參考軸中所有序列的第一個元素。

如果頂端的兩個或多個專案具有相同的值 (也就是說，當有系結) 時，會包含這兩個專案的索引，並保證會以遞增的元素索引來排序。 請注意，不論 *AxisDirection* 的值是什麼，都是如此。

`Axis`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

要在其中選取元素的維度索引。 這個值必須小於 *InputTensor* 的 *DimensionCount* 。

`K`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

要選取的元素數目。 *K* 必須大於0，但小於 *軸* 所指定之維度中 *InputTensor* 的元素數目。

`AxisDirection`

類型： **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)列舉中的值。 如果設定為 **DML_AXIS_DIRECTION_INCREASING**，則這個運算子會傳回 *最小* 的 *K* 元素（以遞增值的順序排列）。 否則，它會以遞減順序傳回 *最大* 的 *K* 元素。

## <a name="examples"></a>範例

### <a name="example-1"></a>範例 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a>範例 2. 使用不同的軸

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a>範例 3. 系結值

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a>範例4。 增加軸方向

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a>備註
當 *AxisDirection* 設定為 [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md)時，這個運算子相當於 [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc)。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束

* *InputTensor*、 *OutputIndexTensor* 和 *OutputValueTensor* 必須有相同的 *DimensionCount*。
* *InputTensor* 和 *OutputValueTensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 和更新版本

| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputValueTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputIndexTensor | 輸出 | 1至8 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 和更新版本

| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputValueTensor | 輸出 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputIndexTensor | 輸出 | 4 | UINT32 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |
