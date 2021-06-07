---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: 使用縮放因數來計算目的地 tensor 大小，以將來源中的專案 Resamples 至目的地 tensor。 您可以使用線性或最接近的相鄰插補模式。
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417358"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>DML_RESAMPLE1_OPERATOR_DESC 結構 (directml .h) 
使用縮放因數來計算目的地 tensor 大小，以將來源中的專案 Resamples 至目的地 tensor。 您可以使用線性或最接近的相鄰插補模式。 運算子支援跨多個維度（而不只是2D）的插補。 因此，您可以保留相同的空間大小，但會在通道之間或在批次之間進行插補。 輸入和輸出座標之間的關聯性如下所示。

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入資料的 tensor。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入輸出資料的 tensor。


`InterpolationMode`

類型： [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

此欄位會決定用來選擇輸出圖元的插補種類。

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**。 使用 *最接近的鄰近* 演算法，為每個輸出元素選擇最接近對應圖元中心的輸入元素。

- **DML_INTERPOLATION_MODE_LINEAR**。 使用 *Quadrilinear* 演算法，其會針對每個維度執行2個最接近相鄰輸入元素的加權平均值，以計算輸出元素。 由於所有4個維度都可以重新取樣，因此每個輸出元素總共會計算16個輸入元素的加權平均值。


`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

陣列中的值數目，這些值會 *調整*、 *InputPixelOffsets* 和 *OutputPixelOffsets* 點。 此值必須符合 *InputTensor* 和 *OutputTensor* 的維度計數，其必須是4。


`Scales`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

重新取樣輸入時要套用的比例，其中尺規 > 1 會向上延展影像，並將 < 1 縮小該維度的影像。 請注意，調整不需要完全相同 `OutputSize / InputSize` 。 如果在調整之後的輸入大於輸出系結，則會將其裁剪為輸出大小。 另一方面，如果在調整之後的輸入小於輸出系結，則會壓制輸出邊緣。


`InputPixelOffsets`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

要在重新取樣之前套用至輸入圖元的位移。 當此值為時 `0` ，就會使用圖元的左上角，而不是其中心，這通常不會提供預期的結果。 若要使用圖元的中心來重新取樣影像，並取得與 [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)相同的行為，此值必須是 `0.5` 。


`OutputPixelOffsets`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

重新取樣後要套用至輸出圖元的位移。 當此值為時 `0` ，就會使用圖元的左上角，而不是其中心，這通常不會提供預期的結果。 若要使用圖元的中心來重新取樣影像，並取得與 [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)相同的行為，此值必須是 `-0.5` 。


## <a name="remarks"></a>備註
當 *InputPixelOffsets* 設定為0.5，而 *OutputPixelOffsets* 設定為-0.5 時，此運算子相當於 [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor* 和 *OutputTensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16 |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |