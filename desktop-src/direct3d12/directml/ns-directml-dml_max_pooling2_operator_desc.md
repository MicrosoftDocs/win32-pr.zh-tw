---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: 在 [輸入] tensor 上，計算滑動視窗內各元素的最大值，並選擇性地傳回所選最大值的索引。
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417263"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>DML_MAX_POOLING2_OPERATOR_DESC 結構 (directml .h) 
在 [輸入] tensor 上，計算滑動視窗內各元素的最大值，並選擇性地傳回所選最大值的索引。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

 `{ BatchCount, ChannelCount, Height, Width }` 如果 *InputTensor. DimensionCount* 是4，則為大小的輸入 Tensor， `{ BatchCount, ChannelCount, Depth, Height, Weight } ` 如果 *InputTensor. DimensionCount* 為5。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的輸出 tensor。 輸出 tensor 的大小可以計算如下。

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

針對輸入 tensor *InputTensor* 所產生並儲存在 *OutputTensor* 中的最大值之索引的選擇性輸出 tensor。 這些索引值是以零為基底，並將輸入 tensor 視為連續的一維陣列。 當滑動視窗中的多個專案具有相同值時，會忽略較晚的相等值，且索引會指向第一個遇到的值。 *OutputTensor* 和 *OutputIndicesTensor* 都有相同的 tensor 大小。


`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

輸入 tensor *InputTensor* 的空間維度數目，也會對應至滑動視窗 *WindowSize* 的維度數目。 此值也會決定進展、 *StartPadding* 和 *EndPadding* *陣列的大小*。 當 *InputTensor* 為4d 時，應設定為2，而當它是 5d tensor 時，則應設為3。


`Strides`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

`{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，滑動視窗大小的進展。


`WindowSize`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

`{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設定為3時，滑動視窗的維度。


`StartPadding`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

要套用至輸入 tensor *InputTensor* 中每個空間維度開頭的填補元素數目。 `{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，這些值就會在中。


`EndPadding`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

要套用至輸入 tensor *InputTensor* 中每個空間維度結尾的填補元素數目。 `{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，這些值就會在中。


`Dilations`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

輸入 tensor *InputTensor* 的每個空間維度的值，會根據該值的每個專案選取滑動視窗內的元素。 `{ Height, Width }`當 *DimensionCount* 設定為2或 `{ Depth, Height, Width }` 設為3時，這些值就會在中。


## <a name="remarks"></a>備註
**DML_MAX_POOLING2_OPERATOR_DESC** 會以額外的常數陣列 *Dilations* 取代舊版 [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) 。 當 *Dilations* 設定為 `{ 1,1 }` 4D 輸入或5d 個輸入功能時，這兩個版本是相等的 `{ 1,1,1 }` 。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *InputTensor*、 *OutputIndicesTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount*。
* *InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 和更新版本
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4到5 | FLOAT32、FLOAT16、INT8、UINT8 |
| OutputTensor | 輸出 | 4到5 | FLOAT32、FLOAT16、INT8、UINT8 |
| OutputIndicesTensor | 選用輸出 | 4到5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 和更新版本
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4到5 | FLOAT32、FLOAT16 |
| OutputTensor | 輸出 | 4到5 | FLOAT32、FLOAT16 |
| OutputIndicesTensor | 選用輸出 | 4到5 | UINT32 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10，版本 2004 (10.0;組建 19041)  |
| **最低支援的伺服器** | Windows Server，版本 2004 (10.0;組建 19041)  |
| **標頭** | directml。h |