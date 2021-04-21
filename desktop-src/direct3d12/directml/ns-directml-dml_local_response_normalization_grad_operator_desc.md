---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: 計算 [本機回應](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)正規化的反向傳播漸層。
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804422"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a>DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml) 

計算 [本機回應](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)正規化的反向傳播漸層。

所有張量的資料類型和大小都必須相同。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入資料的 tensor。 此 tensor 的 *大小* 應該是 `{ BatchCount, ChannelCount, Height, Width }` 。

`InputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

傳入的漸層 tensor。 這通常是從上一層的反向傳播輸出中取得。

`OutputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 backpropagated 漸層的輸出 tensor。

`CrossChannel`

類型： **[BOOL](/windows/win32/winprog/windows-data-types)**

如果 LRN 圖層在各通道之間加總，則 **為 TRUE** ;如果 LRN 圖層加總空間維度，則 **為 FALSE** 。

`LocalSize`

類型： **[UINT](/windows/win32/winprog/windows-data-types)**

要在每個維度加總的元素數目上限 (本地區域會遭到裁剪，讓所有專案都在界限) 內。 如果 *CrossChannel* 為 **TRUE**，則這是本機區域的寬度和高度。 如果 *CrossChannel* 為 **FALSE**，則這是本機區域中的元素數目。 此值必須至少為 1。

`Alpha`

類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**

調整參數的值。 我們建議預設值為0.0001。

`Beta`

類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**

指數值。 我們建議預設值為0.75。

`Bias`

類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**

偏差的值。 我們建議預設值為1。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputGradientTensor*、 *InputTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型* 和 *大小*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16 |
| InputGradientTensor | 輸入 | 4 | FLOAT32、FLOAT16 |
| OutputGradientTensor | 輸出 | 4 | FLOAT32、FLOAT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |
