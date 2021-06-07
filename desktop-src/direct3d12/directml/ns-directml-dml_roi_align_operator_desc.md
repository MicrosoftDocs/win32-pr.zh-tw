---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870). 總而言之，此作業會解壓縮來自輸入影像 tensor 的裁剪，並使用指定的 *InterpolationMode*，將其調整為 *OutputTensor* 最後2個維度所指定的一般輸出大小。
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417222"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>DML_ROI_ALIGN_OPERATOR_DESC 結構 (directml .h) 

Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870). 總而言之，此作業會解壓縮來自輸入影像 tensor 的裁剪，並使用指定的 *InterpolationMode*，將其調整為 *OutputTensor* 最後2個維度所指定的一般輸出大小。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor，其中包含具有維度的輸入資料 `{ BatchCount, ChannelCount, InputHeight, InputWidth }` 。

`ROITensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor，其中包含感興趣的區域 (ROI) 資料。 允許的維度 `ROITensor` 為 `{ NumROIs, 4 }` 、 `{ 1, NumROIs, 4 }` 或 `{ 1, 1, NumROIs, 4 }` 。 針對每個投資報酬率，值會是其左上角和右下角的座標（依序排列） `[x1, y1, x2, y2]` 。

`BatchIndicesTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含要從中解壓縮 ROIs 之批次索引的 tensor。 允許的維度 `BatchIndicesTensor` 為 `{ NumROIs }` 、 `{ 1, NumROIs }` 、 `{ 1, 1, NumROIs }` 或 `{ 1, 1, 1, NumROIs }` 。 每個值都是來自 *InputTensor* 之批次的索引。 如果值不在範圍 [0，BatchCount) 中，則行為會是未定義的。

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸出資料的 tensor。 *OutputTensor* 的預期維度是 `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` 。

`ReductionFunction`

類型： **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

要在對輸出專案產生的所有輸入樣本之間進行縮減時所要使用的縮減函數 ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) 或 **DML_REDUCE_FUNCTION_MAX**) 。 要減少的輸入樣本數會受到 *MinimumSamplesPerOutput* 和 *MaximumSamplesPerOutput* 的限制。

`InterpolationMode`

類型： **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

調整區域大小時要使用的插補模式。

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)。 使用 *最接近的鄰近* 演算法，為每個輸出元素選擇最接近對應圖元中心的輸入元素。
- **DML_INTERPOLATION_MODE_LINEAR**。 使用 *雙線性* 演算法，它會針對每個維度執行2個最接近相鄰輸入元素的加權平均值，以計算輸出元素。 由於只有2個維度會調整大小，因此每個輸出元素總共會計算4個輸入元素的加權平均值。

`SpatialScaleX`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

縮放係數的 X (或寬度) 元件，用以乘以 *ROITensor* 座標，以便讓它們與 *InputHeight* 和 *InputWidth* 成正比。 例如，如果 *ROITensor* 包含正規化座標 (範圍 [0 ..1] ) 中的值，則 *SpatialScaleX* 通常會具有與 *InputWidth* 相同的值。

`SpatialScaleY`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

縮放係數的 Y (或高度) 元件，用來乘以 *ROITensor* 座標，以便讓它們與 *InputHeight* 和 *InputWidth* 成正比。 例如，如果 *ROITensor* 包含正規化座標 (範圍 [0 ..1] ) 中的值，則 *SpatialScaleY* 通常會具有與 *InputHeight* 相同的值。

`OutOfBoundsInputValue`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

當 ROIs 超出 *InputTensor* 的界限時，從 *InputTensor* 讀取的值。 當在 *SpatialScaleX* 和 *SpatialScaleY* 的調整 *ROITensor* 之後取得的值大於 *InputWidth* 和 *InputHeight* 時，就會發生這種情況。

`MinimumSamplesPerOutput`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

每個輸出元素要使用的輸入樣本數目下限。 運算子會計算輸入樣本的數目 `ScaledCropSize / OutputSize` ，然後將其設為 *MinimumSamplesPerOutput* 和 *MaximumSamplesPerOutput*。

`MaximumSamplesPerOutput`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

每個輸出元素要使用的輸入樣本數上限。 運算子會計算輸入樣本的數目 `ScaledCropSize / OutputSize` ，然後將其設為 *MinimumSamplesPerOutput* 和 *MaximumSamplesPerOutput*。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor*、 *OutputTensor* 和 *ROITensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16 |
| ROITensor | 輸入 | 2到4 | FLOAT32、FLOAT16 |
| BatchIndicesTensor | 輸入 | 1到4 | UINT32 |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |