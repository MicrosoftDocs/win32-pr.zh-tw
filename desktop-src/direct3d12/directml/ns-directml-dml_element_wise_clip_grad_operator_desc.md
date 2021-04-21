---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: 計算 [元素取向剪輯](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)的反向傳播漸層。
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 224fbacdb8816a6aed6a7779c5c8ff991736ee6c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804447"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a>DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml) 

計算 [元素取向剪輯](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)的反向傳播漸層。

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

這個運算子支援就地執行，這表示在系結 `OutputTensor` 期間允許別名 *InputTensor* 。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

輸入功能 tensor。 這通常是在轉寄行程中提供作為 *InputTensor* [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) 的相同 tensor。

`InputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

傳入的漸層 tensor。 這通常是從上一層的反向傳播輸出中取得。 一般來說，這個 tensor 的大小會和向前傳遞中對應 **DML_OPERATOR_ELEMENT_WISE_CLIP** 的 *輸出* 相同。

`OutputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 backpropagated 漸層的輸出 tensor。 一般來說，這個 tensor 的大小會和向前傳遞中對應 **DML_OPERATOR_ELEMENT_WISE_CLIP** 的 *輸入* 相同。

`Min`

類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**

最小值。 如果 x 位於或低於此值，則漸層結果為0。

`Max`

類型： **[FLOAT](/windows/win32/winprog/windows-data-types)**

最大值。 如果 x 等於或高於此值，則漸層結果為0。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputGradientTensor*、 *InputTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| InputGradientTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputGradientTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |
