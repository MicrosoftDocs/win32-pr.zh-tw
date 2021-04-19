---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: " (輸入 tensor 的「配量」 ) 解壓縮單一子領域。"
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: 06721a7484426eb293494156a2ec23db6fbf0a6b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981916"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>DML_SLICE1_OPERATOR_DESC 結構 (directml .h) 
 (輸入 tensor 的「配量」 ) 解壓縮單一子領域。

[ *輸入] 視窗* 描述配量中要考慮的輸入 tensor 範圍。 此視窗會使用每個維度的三個值來定義。

- *位移* 會將 *視窗的開頭* 標示為維度。
- *大小* 會在維度中標示視窗的範圍。 維度中 *視窗的結尾* 是 `offset + size - 1` 。
- *Stride* 表示如何遍歷維度中的元素。
  - Stride 的大小表示在視窗中複製時要前進的元素數目。
  - 如果 stride 是正數，則會從維度中視窗的 *開頭* 開始複製元素。
  - 如果跨距是負數，則會從維度中視窗的 *結尾* 開始複製專案。

下列虛擬程式碼說明如何使用 [輸入] 視窗複製元素。 請注意，維度中的元素如何從開頭到結尾以正面的跨距複製，並從結尾複製到以負的 stride 開始。

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

輸入視窗不得在任何維度中都是空的，而且視窗不得延伸到超出輸入 (tensor 的維度，) 不允許超出範圍的讀取。 視窗的大小和進展實際上會限制可從輸入 tensor 的每個維度複製的元素數目 `i` 。

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

輸出 tensor 不需要複製視窗內所有可連接的元素。 配量有效，只要 `1 <= OutputSizes[i] <= MaxCopiedElements[i]` 。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要從中解壓縮配量的 tensor。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

寫入切割資料結果的 tensor。


`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

維度的數目。 此欄位會決定 *InputWindowOffsets*、 *InputWindowSizes* 和 *InputWindowStrides* 陣列的大小。 此值必須與輸入和輸出張量的 *DimensionCount* 相符。 此值必須介於1和8之間，其開頭 `DML_FEATURE_LEVEL_3_0` 為; 較早的功能層級需要值為4或5。


`InputWindowOffsets`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

陣列，其中包含每個維度之輸入視窗的元素) 中的開始 (。 陣列中的值必須滿足條件約束 `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

陣列，其中包含每個維度之輸入視窗) 專案中的範圍 (。 陣列中的值必須滿足條件約束 `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

陣列，其中包含在專案中每個輸入 tensor 維度的配量跨距。 Stride 的大小表示在輸入視窗內複製時要前進的元素數目。 Stride 的正負號可決定是否要從視窗的開頭開始複製專案 (正跨距) 或視窗結尾 (負 stride) 。 進步可能不是0。

## <a name="examples"></a>範例

下列範例會使用相同的輸入 tensor。

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>範例 1. 具有正面進步的 Strided 配量

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

複製的元素的計算方式如下。 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>範例 2. 具有負面進步的 Strided 配量

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

回想一下，具有負面視窗進展的維度會在該維度的輸入視窗結束時開始複製;這是藉由加入 `InputWindowSize[i] - 1` 至視窗位移來完成。 具有正面 stride 的維度只會從開始 `InputWindowOffset[i]` 。
- 軸 0 (`+1` 視窗 stride) 開始複製的時間 `InputWindowOffsets[0] = 0` 。 
- 軸 1 (`+1` 視窗 stride) 開始複製 `InputWindowOffsets[1] = 0` 。 
- 軸 2 (`-2` 視窗 stride) 開始複製的時間 `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` 。 
- 軸 3 (`+2` 視窗 stride) 開始複製 `InputWindowOffsets[3] = 1` 。 

複製的元素的計算方式如下。 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>備註
這個運算子類似于 [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc)，但它有兩種重要的差異。

- 配量的進展可能是負數，可讓維度的值反轉。
- 輸入視窗大小與輸出 tensor 大小不一定相同。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。

## <a name="tensor-support"></a>Tensor 支援
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 和更新版本
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 和更新版本
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4到5 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputTensor | 輸出 | 4到5 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |