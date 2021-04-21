---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: 根據 Adam (**ADA** ptive **M** oment 估計) 演算法，使用提供的漸層來計算更新的加權 (參數) 。 這個運算子是優化工具，通常用於定型迴圈的加權更新步驟，以執行梯度下降。
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803528"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>DML_ADAM_OPTIMIZER_OPERATOR_DESC 結構 (directml .h) 

根據 Adam (**ADA** ptive **M** oment 估計) 演算法，使用提供的漸層來計算更新的加權 (參數) 。 這個運算子是優化工具，通常用於定型迴圈的加權更新步驟，以執行梯度下降。

這個運算子會執行下列計算：

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

除了計算 (在 *OutputParametersTensor*) 中傳回的更新權數參數之外，此運算子也會分別傳回 *OutputFirstMomentTensor* 和 *OutputSecondMomentTensor* 中更新的第一次和第二次預估值。 一般而言，您應該儲存這些第一次和第二次的估計值，並在後續定型步驟中提供它們作為輸入。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a>成員

`InputParametersTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor，其中包含要套用此優化工具)  (權數的參數。 這個運算子會使用漸層、第一個和第二個時間估計、目前的定型步驟，以及超參數 *LearningRate*、 *Beta1* 和 *Beta2*，來對此 tensor 中提供的加權值執行梯度下降。

`InputFirstMomentTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor，其中包含每個加權值之漸層的第一次估計。 這些值通常是透過 *OutputFirstMomentTensor* 上一次執行這個運算子的結果來取得的。

當您第一次將此優化工具套用至一組權數時 (例如，在初始定型步驟期間) 此 tensor 的值通常會初始化為零。 後續的執行應該使用 *OutputFirstMomentTensor* 中傳回的值。

這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。

`InputSecondMomentTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor，其中包含每個權數值之漸層的第二個估計值。 這些值通常是透過 *OutputSecondMomentTensor* 上一次執行這個運算子的結果來取得的。

當您第一次將此優化工具套用至一組權數時 (例如，在初始定型步驟期間) 此 tensor 的值通常會初始化為零。 後續的執行應該使用 *OutputSecondMomentTensor* 中傳回的值。

這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。

`GradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要套用至輸入參數的漸層 (權數) 用於梯度下降。 在定型期間，通常會在反向傳播階段中取得漸層。

這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。

`TrainingStepTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

純量 tensor，其中包含代表目前定型步驟計數的單一整數值。 此值連同 *Beta1* 和 *Beta2* 可用來計算第一個和第二次估計張量的指數衰減。

定型步驟值通常會在定型開頭從0開始，而且每個後續的定型步驟會遞增1。 這個運算子不會更新定型步驟值;您應該以手動方式（例如使用 [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc)）來進行。

這個 tensor 必須是純量 (，也就是 *大小* 等於 1) 且資料類型 [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)。

`OutputParametersTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

在套用漸層下降之後，將更新的參數保留 (權數) 值的輸出 tensor。

在系結期間，此 tensor 可為合格的輸入 tensor 加上別名，可用來執行此 tensor 的就地更新。 如需詳細資訊，請參閱「 [備註](#remarks) 」一節。

這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。

`OutputFirstMomentTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含第一次更新估計的輸出 tensor。 您應該儲存此 tensor 的值，並在後續定型步驟期間于 *InputFirstMomentTensor* 中提供這些值。

在系結期間，此 tensor 可為合格的輸入 tensor 加上別名，可用來執行此 tensor 的就地更新。 如需詳細資訊，請參閱「 [備註](#remarks) 」一節。

這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。

`OutputSecondMomentTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含已更新之第二次預估的輸出 tensor。 您應該儲存此 tensor 的值，並在後續定型步驟期間于 *InputSecondMomentTensor* 中提供這些值。

在系結期間，此 tensor 可為合格的輸入 tensor 加上別名，可用來執行此 tensor 的就地更新。 如需詳細資訊，請參閱「 [備註](#remarks) 」一節。

這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。

`LearningRate`

類型： **float**

學習率，也通常稱為「 *步驟」大小*。 學習速率是一種超參數，可在每個定型步驟上判斷加權更新沿著漸層向量的大小。

`Beta1`

類型： **float**

超參數，代表漸層首次估計的指數衰減率。 此值應介於0.0 到1.0 之間。 值為 0.9 f 是典型的。

`Beta2`

類型： **float**

超參數，代表漸層第二個時間估計的指數衰減率。 此值應介於0.0 到1.0 之間。 0.999 f 的值是典型的。

`Epsilon`

類型： **float**

用來防止零除的較小值。 若為32位浮點數輸入，則一般值包括 1e-8 或 `FLT_EPSILON` 。

## <a name="remarks"></a>備註
這個運算子支援就地執行，這表示每個輸出 tensor 都允許在系結期間為合格的輸入 tensor 加上別名。 例如，您可以為 *InputParametersTensor* 和 *OutputParametersTensor* 系結相同的資源，以便有效地達成輸入參數的就地更新。 這個運算子的所有輸入張量（ *TrainingStepTensor* 除外）都有資格以這種方式為別名。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *GradientTensor*、 *InputFirstMomentTensor*、 *InputParametersTensor*、 *InputSecondMomentTensor*、 *OutputFirstMomentTensor*、 *OutputParametersTensor*、 *OutputSecondMomentTensor* 和 *TrainingStepTensor* 必須有相同的 *資料類型*。
* *GradientTensor*、 *InputFirstMomentTensor*、 *InputParametersTensor*、 *InputSecondMomentTensor*、 *OutputFirstMomentTensor*、 *OutputParametersTensor* 和 *OutputSecondMomentTensor* 的 *大小* 必須相同。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 維度 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | 輸入 | {D0，D1，D2，D3} | 4 | FLOAT32、FLOAT16 |
| InputFirstMomentTensor | 輸入 | {D0，D1，D2，D3} | 4 | FLOAT32、FLOAT16 |
| InputSecondMomentTensor | 輸入 | {D0，D1，D2，D3} | 4 | FLOAT32、FLOAT16 |
| GradientTensor | 輸入 | {D0，D1，D2，D3} | 4 | FLOAT32、FLOAT16 |
| TrainingStepTensor | 輸入 | {1，1，1，1} | 4 | FLOAT32、FLOAT16 |
| OutputParametersTensor | 輸出 | {D0，D1，D2，D3} | 4 | FLOAT32、FLOAT16 |
| OutputFirstMomentTensor | 輸出 | {D0，D1，D2，D3} | 4 | FLOAT32、FLOAT16 |
| OutputSecondMomentTensor | 輸出 | {D0，D1，D2，D3} | 4 | FLOAT32、FLOAT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |