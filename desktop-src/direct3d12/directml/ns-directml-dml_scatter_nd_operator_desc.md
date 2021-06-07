---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: 'DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC) '
description: 將整個輸入 tensor 複製到輸出，然後使用 [更新] tensor 中的對應值來覆寫選取的索引。
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417314"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>DML_SCATTER_ND_OPERATOR_DESC 結構 (directml .h) 
將整個輸入 tensor 複製到輸出，然後使用 [更新] tensor 中的對應值來覆寫選取的索引。 這個運算子會執行下列虛擬虛擬，其中 "..."代表一系列的座標，其確切行為取決於軸和索引的大小。

```
output = input
output[indices[...]] = updates[...]
```

如果有兩個輸出元素索引 () 無效，則無法保證最後寫入的最後一個。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要從中讀取的 tensor。


`IndicesTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含索引的 tensor。 此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。 *IndicesTensor* 的最後一個維度實際上是每個索引元組的座標數目，而不得超過 *InputTensor. DimensionCount*。 例如，大小 `{1,4,5,2}` 為 *IndicesDimensionCount* = 3 的索引 tensor，表示索引為 *InputTensor* 的2值座標元組4x5 陣列。

從開始 `DML_FEATURE_LEVEL_3_0` ，當使用帶正負號的整數型別搭配這個 tensor 時，這個運算子支援負的索引值。 負索引會解讀為相對於個別維度的結尾。 例如，-1 的索引指的是該維度的最後一個元素。


`UpdatesTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含新值的 tensor，用來取代對應索引的現有輸入值。 此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。 預期的 *UpdatesTensor 大小* 為 IndicesTensor 的串連 *。* 大小的前置區段和 *InputTensor。大小* 尾端區段可產生下列各項。

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

這些維度會靠右對齊，並在必要時前置1值以滿足 *UpdatesTensor. DimensionCount*。

以下為範例。

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 這個 tensor 的 *大小* 和 *資料類型* 必須符合 *InputTensor 的大小*。


`InputDimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

*InputTensor* 中的實際輸入維度數目，在略過任何不相關的前置專案之後（範圍 [1， *InputTensor. DimensionCount*) ）。 例如，假設 *InputTensor 的大小* = {1,1,4,6} 和 *InputDimensionCount* = 3，則實際有意義的索引為 {1,4,6} 。


`IndicesDimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

在忽略任何不相關的前置專案（範圍 [1， *IndicesTensor. DimensionCount*) ）後， *IndicesTensor* 內實際的索引維度數目。 例如，假設 *IndicesTensor 的大小* = {1,1,4,6} 和 *IndicesDimensionCount* = 3，則實際有意義的索引為 {1,4,6} 。

## <a name="examples"></a>範例

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *IndicesTensor*、 *InputTensor*、 *OutputTensor* 和 `UpdatesTensor` 必須有相同的 *DimensionCount*。
* *InputTensor*、 *OutputTensor* 和 `UpdatesTensor` 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 和更新版本
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| IndicesTensor | 輸入 | 1至8 | INT64、INT32、UINT64、UINT32 |
| UpdatesTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 和更新版本
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| IndicesTensor | 輸入 | 4 | UINT32 |
| UpdatesTensor | 輸入 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |