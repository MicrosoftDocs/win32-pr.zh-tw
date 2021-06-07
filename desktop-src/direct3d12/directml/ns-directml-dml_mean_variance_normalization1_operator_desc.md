---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: 在輸入 tensor 上執行 mean 變異數正規化函數。 這個運算子會計算輸入 tensor 的平均數和變異數，以執行正規化。
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
f1_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417240"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC 結構 (directml .h) 

在輸入 tensor 上執行 mean 變異數正規化函數。 這個運算子會計算輸入 tensor 的平均數和變異數，以執行正規化。 這個運算子會執行下列計算。

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入資料的 tensor。 此 tensor 的維度應該是 `{ BatchCount, ChannelCount, Height, Width }` 。

`ScaleTensor`

類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含調整資料的選擇性 tensor。

如果 **DML_FEATURE_LEVEL** 小於 **DML_FEATURE_LEVEL_4_0**，則此 tensor 的維度應該是 `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` 。 ScaleBatchCount、ScaleHeight 和 ScaleWidth 的維度應該符合 *InputTensor*，或設定為1，以自動在輸入之間廣播這些維度。

如果 **DML_FEATURE_LEVEL** 大於或等於 **DML_FEATURE_LEVEL_4_0**，則任何維度都可以設定為1，並自動廣播以符合 *InputTensor*。

如果使用 *BiasTensor* ，則需要此 tensor。

`BiasTensor`

類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***


包含偏差資料的選擇性 tensor。

如果 **DML_FEATURE_LEVEL** 小於 **DML_FEATURE_LEVEL_4_0**，則此 tensor 的維度應該是 `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` 。 BiasBatchCount、BiasHeight 和 BiasWidth 的維度應該符合 *InputTensor*，或設定為1，以自動在輸入之間廣播這些維度。

如果 **DML_FEATURE_LEVEL** 大於或等於 **DML_FEATURE_LEVEL_4_0**，則任何維度都可以設定為1，並自動廣播以符合 *InputTensor*。

如果使用 *ScaleTensor* ，則需要此 tensor。

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 這個 tensor 的維度是 `{ BatchCount, ChannelCount, Height, Width }` 。

`AxisCount`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

軸的數目。 此欄位會決定 *軸* 陣列的大小。

`Axes`

類型： \_ 欄位 \_ 大小 \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \*** 

要計算平均值和變異數的座標軸。

`NormalizeVariance`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

如果正規化層包含正規化計算中的變異數，**則為 TRUE** 。 否則 **為 FALSE**。 如果 **為 FALSE**，則正規化方程式為 `Output = FusedActivation(Scale * (Input - Mean) + Bias)` 。

`Epsilon`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

用來避免除以零的 epsilon 值。 預設值為0.00001 的建議值。

`FusedActivation`

類型： \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

要在正規化之後套用的選擇性融合啟用層。

## <a name="remarks"></a>備註
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** 是 [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc)功能的超集合。 在這裡，將 **座標軸** 陣列設定為 `{ 0, 2, 3 }` 相當於 **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC** 中將 *CrossChannel* 設定為 **FALSE** ，而將 **座標軸** 陣列設定為 `{ 1, 2, 3 }` 相當於將 *CrossChannel* 設定為 **TRUE**。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束

*BiasTensor*、 *InputTensor*、 *OutputTensor* 和 *ScaleTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。

## <a name="tensor-support"></a>Tensor 支援

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 和更新版本

| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16 |
| ScaleTensor | 選擇性輸入 | 1至8 | FLOAT32、FLOAT16 |
| BiasTensor | 選擇性輸入 | 1至8 | FLOAT32、FLOAT16 |
| OutputTensor | 輸出 | 1至8 | FLOAT32、FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 和更新版本

| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16 |
| ScaleTensor | 選擇性輸入 | 4 | FLOAT32、FLOAT16 |
| BiasTensor | 選擇性輸入 | 4 | FLOAT32、FLOAT16 |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |

## <a name="see-also"></a>另請參閱

[使用融合的運算子改善效能](../dml-fused-activations.md)