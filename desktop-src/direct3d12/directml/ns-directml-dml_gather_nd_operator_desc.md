---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: 使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。 |DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802901"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>DML_GATHER_ND_OPERATOR_DESC 結構 (directml .h) 

使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。 這個運算子會執行下列虛擬虛擬，其中 "..."代表一系列的座標，其行為取決於輸入和索引維度計數。

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
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

包含索引的 tensor。 此 tensor 的 *DimensionCount* 必須符合 *InputTensor. DimensionCount*。 *IndicesTensor* 的最後一個維度實際上是每個索引元組的座標數目，不能超過 *InputTensor. DimensionCount*。 例如， *大小* `{1,4,5,2}` 為 *IndicesDimensionCount* = 3 的索引 Tensor，表示索引為 *InputTensor* 的2座標元組4x5 陣列。

從開始 `DML_FEATURE_LEVEL_3_0` ，當使用帶正負號的整數型別搭配這個 tensor 時，這個運算子支援負的索引值。 負索引會解讀為相對於個別維度的結尾。 例如，-1 的索引指的是該維度的最後一個元素。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 此 tensor 的 *DimensionCount* 和 *資料類型* 必須符合 *InputTensor. DimensionCount*。 預期的 *OutputTensor。* 大小是 IndicesTensor 的串連 *。* 大小的開頭區段和 *InputTensor。大小* 的尾端區段會產生：

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

輸出維度會靠右對齊，並在必要時前置1值，以滿足最多 *OutputTensor DimensionCount*。

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

## <a name="examples"></a>範例

### <a name="example-1-1d-remapping"></a>範例 1. 1D 重新對應

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a>範例 2. 2D 重新對應

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a>備註
在中引進了這個運算子的較新版本 `DML_OPERATOR_GATHER_ND1` `DML_FEATURE_LEVEL_3_0` 。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *IndicesTensor*、 *InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。
* *InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 和更新版本
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| IndicesTensor | 輸入 | 1至8 | INT64、INT32、UINT64、UINT32 |
| OutputTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 和更新版本
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| IndicesTensor | 輸入 | 4 | UINT32 |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |
