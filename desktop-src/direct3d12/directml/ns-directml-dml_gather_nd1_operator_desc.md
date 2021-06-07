---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: 使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。 |DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417271"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a>DML_GATHER_ND1_OPERATOR_DESC 結構 (directml .h) 

使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。 這個運算子會執行下列虛擬虛擬，其中 "..."代表一系列的座標，其行為取決於批次、輸入和索引維度計數。

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要從中讀取的 tensor。

`IndicesTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含索引的 tensor。 此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。 *IndicesTensor* 的最後一個維度實際上是每個索引元組的座標數目，不能超過 *InputTensor. DimensionCount*。 例如， *大小* `{1,4,5,2}` 為 *IndicesDimensionCount* = 3 的索引 Tensor，表示索引為 *InputTensor* 的2座標元組4x5 陣列。

從開始 `DML_FEATURE_LEVEL_3_0` ，當使用帶正負號的整數型別搭配這個 tensor 時，這個運算子支援負的索引值。 負索引會解讀為相對於個別維度的結尾。 例如，-1 的索引指的是該維度的最後一個元素。

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 此 tensor 的 *DimensionCount* 和 *資料類型* 必須符合 *InputTensor. DimensionCount*。 預期的 *OutputTensor。* 大小是 IndicesTensor 的串連 *。* 大小的尾端區段和 *InputTensor 的大小* 會產生下列各項。

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

這些維度會靠右對齊，並在必要時前置1值以滿足 *OutputTensor. DimensionCount*。

以下為範例。

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

略過任何不相關的開頭維度之後， *InputTensor* 內實際輸入維度的數目，範圍為 `[1, *InputTensor.DimensionCount*]` 。 例如，假設 *InputTensor 大小*  =  `{1,1,4,6}` 和 `InputDimensionCount` = 3，則實際有意義的索引為 `{1,4,6}` 。

`IndicesDimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

在忽略任何不相關的前置專案（範圍 [1， *IndicesTensor. DimensionCount*]）之後， *IndicesTensor* 中的實際索引維度數目。 例如，假設 *IndicesTensor 大小*  =  `{1,1,4,6}` 和 *IndicesDimensionCount* = 3，則實際有意義的索引為 `{1,4,6}` 。

`BatchDimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

每個 tensor 中的維度數目 (*InputTensor*、 *IndicesTensor*、 *OutputTensor*) 視為獨立的批次，範圍介於 [0， *InputTensor. DimensionCount*) 和 [0， *IndicesTensor. DimensionCount*) 中。 批次計數可以是0，這意味著單一批次。 例如，假設有 *IndicesTensor*，  =  `{1,3,4,5,6,7}` 而 *IndicesDimensionCount* = 5 和 `BatchDimensionCount` = 2，則有批次 `{3,4}` 和有意義的索引 `{5,6,7}` 。

## <a name="remarks"></a>備註
**DML_GATHER_ND1_OPERATOR_DESC** 會新增 *BatchDimensionCount*，且相當於 *BatchDimensionCount* = 0 時的 [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) 。

## <a name="examples"></a>範例

### <a name="example-1-1d-remapping"></a>範例 1. 1D 重新對應

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a>範例 2. 使用批次計數進行2D 重新對應

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *IndicesTensor*、 *InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。
* *InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| IndicesTensor | 輸入 | 1至8 | INT64、INT32、UINT64、UINT32 |
| OutputTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |
