---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: 計算輸入 tensor 的所有非零元素的 N 維座標。
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417237"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>DML_NONZERO_COORDINATES_OPERATOR_DESC 結構 (directml .h) 

計算輸入 tensor 的所有非零元素的 N 維座標。

這個運算子會產生值的 MxN 矩陣，其中每個資料列 M 包含輸入中非零值的 N 維座標。 使用 **FLOAT32** 或 **FLOAT16** 輸入時，負號和正 0 (0.0 f 和-0.0 f) 會視為零，以供此運算子的用途使用。

運算子要求 *OutputCoordinatesTensor* 的大小必須夠大，才能容納最糟的情況，其中輸入的每個元素都不是零。 這個運算子會透過 *OutputCountTensor* 傳回非零元素的計數，而呼叫端可以檢查以判斷寫入 *OutputCoordinatesTensor* 的座標數目。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

輸入 tensor。

`OutputCountTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

在輸入 tensor 中保存非零元素計數的輸出 tensor。 這個 tensor 必須是純量， &mdash; 也就是這個 tensor 的大小必須全部為1。 這個 tensor 的型別必須是 **UINT32**。

`OutputCoordinatesTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

輸出 tensor，其中保存非零之輸入元素的 N 維座標。 

如果 DimensionCount 為 4) ，則此 tensor 的 *大小* 必須是 (，如果 `{1,1,M,N}`  `{1,1,1,M,N}` *DimensionCount* 為 5) ，則為 (，其中 M 是 *InputTensor* 中的專案總數，而 N 大於或等於有效的 *InputTensor**次序*，最多可達輸入的 *DimensionCount* 。

Tensor 的有效順位是由該 tensor 的 *DimensionCount* 所決定，而不是大小為1的開頭維度。 例如，大小為的 tensor `{1,2,3,4}` 具有有效的順位3，與大小的 tensor 相同 `{1,1,5,5,5}` 。 具有大小的 tensor `{1,1,1,1}` 具有有效的順位0。

考慮使用 *大小* 為的 *InputTensor* `{1,1,12,5}` 。 此輸入 tensor 包含60個元素，且具有有效的順位2。 在此範例中，所有有效的 *OutputCoordinatesTensor* 大小都屬於表單 `{1,1,60,N}` ，其中 N >= 2，但在此範例) 中不大於 *DimensionCount* (4。

寫入此 tensor 的座標保證會以遞增的元素索引來排序。 例如，如果輸入 tensor 在座標、和上有3個非零值， {1,0} {1,2} {0,5} 則寫入 *OutputCoordinatesTensor* 的值將會是 `[[0,5], [1,0], [1,2]]` 。

雖然此 tensor 需要其維度 M 等於輸入 tensor 中的元素數目，但這個運算子只會將 OutputCount 元素最多寫入此 tensor。 OutputCount 會透過純量 *OutputCountTensor* 傳回。

> [!NOTE]
> 當這個運算子完成之後，此 tensor 的其餘元素就不會定義。 您不應該依賴這些元素的值。

## <a name="example"></a>範例

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor*、 *OutputCoordinatesTensor* 和 `OutputCountTensor` 必須有相同的 *DimensionCount*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 維度 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | 輸入 | {[D0]、D1、D2、D3、D4} | 4到5 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputCountTensor | 輸出 | {[1]，1，1，1，1} | 4到5 | UINT32 |
| OutputCoordinatesTensor | 輸出 | {[1]，1，1，M，N} | 4到5 | UINT32 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |