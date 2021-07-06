---
title: DirectML 結構
description: 下列結構是在 DirectML 中宣告。
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: fb923bb7546dffb6320802b933a170ccef685d21
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282577"
---
# <a name="directml-structures"></a>DirectML 結構

下列結構是在 DirectML 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題和描述 |
|-|
| [**DML_ACTI加值稅ION_CELU_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_activation_celu_operator_desc)。 在 *InputTensor* 中的每個元素上執行連續 differentiable 指數線性單位 (CELU) 啟動函式，並將結果放入 *OutputTensor* 的對應元素。 |
| [**DML_ACTI加值稅ION_ELU_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_elu_operator_desc)。 描述 DirectML 運算子，這個運算子會在輸入中的每個元素上執行指數線性單位 (ELU) 啟動函式。 |
| [**DML_ACTI加值稅ION_HARDMAX_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_hardmax_operator_desc)。 描述在輸入上執行 hardmax 函式的 DirectML 啟用運算子。 |
| [**DML_ACTI加值稅ION_HARD_SIGMOID_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_hard_sigmoid_operator_desc)。 描述在輸入中的每個元素上執行硬式 sigmoid 函式的 DirectML 啟用運算子。 |
| [**DML_ACTI加值稅ION_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_identity_operator_desc)。 描述執行 identity 函數的 DirectML 啟動運算子。 |
| [**DML_ACTI加值稅ION_LEAKY_RELU_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_leaky_relu_operator_desc)。 描述在輸入中的每個元素上執行有漏洞的 DirectML 運算子， (ReLU) 啟用函式。 |
| [**DML_ACTI加值稅ION_LINEAR_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_linear_operator_desc)。 描述在輸入中的每個元素上執行線性啟用函式的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_LOG_SOFTMAX_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_log_softmax_operator_desc)。 描述在輸入上執行 softmax 啟用功能的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_PARAMETERIZED_RELU_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_parameterized_relu_operator_desc)。 描述 DirectML 運算子，這個運算子會在輸入中的每個元素上執行參數化的已更正線性單位 (ReLU) 啟用函式。 |
| [**DML_ACTI加值稅ION_PARAMETRIC_SOFTPLUS_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_parametric_softplus_operator_desc)。 描述在輸入中的每個元素上執行參數化 softplus 啟用函式的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_RELU_GRAD_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_activation_relu_grad_operator_desc)。 計算 (ReLU) 的已更正線性單位反向傳播漸層。 |
| [**DML_ACTI加值稅ION_RELU_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_relu_operator_desc)。 描述 DirectML 運算子，這個運算子會在輸入中的每個元素上執行可更正的線性單位 (ReLU) 啟動函式。 |
| [**DML_ACTI加值稅ION_SCALED_ELU_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_scaled_elu_operator_desc)。 描述 DirectML 運算子，這個運算子會在輸入中的每個元素上執行調整的指數線性單位 (ELU) 啟用函式。 |
| [**DML_ACTI加值稅ION_SCALED_TANH_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_scaled_tanh_operator_desc)。 描述在輸入中的每個元素上執行縮放雙曲正切函數啟用函式的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_SHRINK_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_activation_shrink_operator_desc)。 描述在輸入上執行 elementwise shrink 啟用函數的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_SIGMOID_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_sigmoid_operator_desc)。 描述在輸入中的每個元素上執行 sigmoid 啟用函式的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_SOFTMAX_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_softmax_operator_desc)。 描述在輸入上執行 softmax 啟用函數的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_SOFTPLUS_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_softplus_operator_desc)。 描述在輸入中的每個元素上執行 softplus 啟用函式的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_SOFTSIGN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_softsign_operator_desc)。 描述在輸入中的每個元素上執行 softsign 啟用函式的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_TANH_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_tanh_operator_desc)。 描述在輸入中的每個元素上執行雙曲正切函數啟用函式的 DirectML 運算子。 |
| [**DML_ACTI加值稅ION_THRESHOLDED_RELU_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_activation_thresholded_relu_operator_desc)。 描述在輸入中的每個元素上執行 thresholded 的 DirectML 運算子， (ReLU) 啟用函式。 |
| [**DML_ADAM_OPTIMIZER_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_adam_optimizer_operator_desc)。 根據 Adam (**ADA** ptive **M** oment 估計) 演算法，使用提供的漸層來計算更新的加權 (參數) 。 這個運算子是優化工具，通常用於定型迴圈的加權更新步驟，以執行梯度下降。 |
| [**DML_AVERAGE_POOLING_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_average_pooling_operator_desc)。 描述在輸入上執行平均共用函數的 DirectML 運算子。 |
| [**DML_ARGMAX_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_argmax_operator_desc)。 輸出一或多個輸入 tensor 維度內最大值元素的索引。 |
| [**DML_ARGMIN_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_argmin_operator_desc)。 輸出一或多個輸入 tensor 維度內最小值元素的索引。 |
| [**DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_average_pooling_grad_operator_desc)。 計算平均共用 (的反向傳播梯度，請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)) 。 |
| [**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC**](./directml/ns-directml-dml_batch_normalization_grad_operator_desc.md)。 計算 [批次](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)正規化的反向傳播漸層。 |
| [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_batch_normalization_operator_desc)。 描述在輸入上執行批次正規化函數的 DirectML 運算子。 |
| [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc)。 包含系結的描述，讓您可以透過呼叫其中一個 [IDMLBindingTable](/windows/desktop/api/directml/nn-directml-idmlbindingtable) 方法，將它加入至系結資料表。 |
| [**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties)。 包含特定已編譯運算子的系結需求或運算子初始化運算式的相關資訊。 |
| [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc)。 指定 [IDMLDevice：： CreateBindingTable](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) 和 [IDMLBindingTable：： Reset](/windows/desktop/api/directml/nf-directml-idmlbindingtable-reset)的參數。 |
| [**DML_BUFFER_ARRAY_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding)。 指定屬於個別緩衝區系結陣列的資源系結。 |
| [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding)。 指定由 Direct3D 12 緩衝區中的位元組範圍所描述的資源系結，以位移和大小表示為 [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)。 |
| [**DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)。 描述將儲存在 Direct3D 12 緩衝區資源中的 tensor。 |
| [**DML_CAST_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_cast_operator_desc)。 描述 DirectML 資料重組運算子，該運算子會執行 cast 函式 f (x) = cast (x) ，將輸入中的每個專案轉換成輸出 tensor 的資料類型，並將結果儲存在輸出中的對應元素。 |
| [**DML_CONVOLUTION_INTEGER_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_convolution_integer_operator_desc)。 使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在整數資料上執行向前卷積。 |
| [**DML_CONVOLUTION_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)。 描述在輸入上執行卷積函數的 DirectML 矩陣乘法運算子。 |
| [**DML_CUMULATIVE_PRODUCT_OPERATOR_DESC**](./directml/ns-directml-dml_cumulative_product_operator_desc.md)。 將 tensor 的元素乘以軸，並將執行中的產品計數寫入輸出 tensor 中。 |
| [**DML_CUMULATIVE_SUMMATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_cumulative_summation_operator_desc)。 將 tensor 的專案加總在軸上，將總和的執行總和寫入輸出 tensor 中。 |
| [**DML_DEPTH_TO_SPACE_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_depth_to_space_operator_desc)。 描述 DirectML 資料重組運算子，可將 (permutes) 資料從深度重新排列到空間資料的區塊。 |
| [**DML_DEPTH_TO_SPACE1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_depth_to_space1_operator_desc)。 重新排列 (permutes) 資料從深度到空間資料的區塊。 運算子會輸出輸入 tensor 的複本，其中深度維度的值會移至 [高度] 和 [寬度] 維度的空間區塊中。 |
| [**DML_DIAGONAL_MATRIX_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_diagonal_matrix_operator_desc)。 描述 DirectML 數學運算子，這個運算子會產生類似類似矩陣的矩陣，並在主要對角和零的其他地方使用。 |
| [**DML_DYNAMIC_QUANTIZE_LINEAR_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_dynamic_quantize_linear_operator_desc)。 計算量化 *InputTensor* 所需的量化比例和零點值，然後套用該量化，將結果寫入 *OutputTensor*。 |
| [**DML_ELEMENT_WISE_ABS_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_abs_operator_desc)。 描述 DirectML 數學運算子，這個運算子會執行專案的絕對值函式 f (x) = abs (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_ACOS_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_acos_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的反余弦函數 f (x) = acos (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_ACOSH_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_acosh_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的反雙曲余弦函數 f (x) = log (x + sqrt (x * x-1) ) * scale + 偏差，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_ADD_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_add_operator_desc)。 描述 DirectML 數學運算子，這個運算子會執行將 ATensor 中的每個元素加入至 BTensor 中其對應元素的函式。 |
| [**DML_ELEMENT_WISE_ADD1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_add1_operator_desc)。 描述 DirectML 數學運算子，這個運算子會執行將 <i>ATensor</i> 中的每個元素新增至 <i>BTensor</i>中其對應元素的函式，f (a，b) = a + b，並具有已融合啟用的選項。 |
| [**DML_ELEMENT_WISE_ASIN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_asin_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的反正弦函數 f (x) = asin (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_ASINH_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_asinh_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的反雙曲正弦函數 f (x) = log (x + sqrt (x * x + 1) ) * scale + 偏差，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_ATAN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_atan_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的反正切函數 f (x) = atan (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_ATANH_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_atanh_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的反雙曲正切函數 f (x) = (記錄 ( (1 + x) / (1 x) ) /2) * scale + 偏差，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC**](./directml/ns-directml-dml_element_wise_atan_yx_operator_desc.md)。 針對 *ATensor* 和 *BTensor* 的每個專案計算雙引數反正切值，其中 *ATensor* 是 *Y 軸* ，而 *BTensor* 是 *X 軸*，將結果放入 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_bit_and_operator_desc)。 在輸入張量的每個對應元素之間計算位 AND，然後將結果寫入輸出 tensor。 |
| [**DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_bit_count_operator_desc)。 針對輸入 tensor 的每個元素計算位 NOT，並將結果寫入輸出 tensor。 |
| [**DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_bit_not_operator_desc)。 針對輸入 tensor 的每個元素，計算位人口計數 (設定為 1) ，然後將結果寫入輸出 tensor。 |
| [**DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_bit_or_operator_desc)。 計算輸入張量的每個對應元素的位 OR，然後將結果寫入輸出 tensor。 |
| [**DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_bit_shift_left_operator_desc)。 依 *BTensor* 的對應元素所指定的位數，對 *ATensor* 的每個元素執行邏輯左移位，將結果放入 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_bit_shift_right_operator_desc)。 依 *BTensor* 的對應元素所指定的位數，對 *ATensor* 的每個元素執行邏輯右移位，將結果放入 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_bit_xor_operator_desc)。 在輸入張量的每個對應專案之間計算位 XOR (獨佔或) ，然後將結果寫入輸出 tensor。 |
| [**DML_ELEMENT_WISE_CEIL_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_ceil_operator_desc)。 描述 DirectML 數學運算子，該運算子會執行元素範圍上限函式 f (x) = ceil (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC**](./directml/ns-directml-dml_element_wise_clip_grad_operator_desc.md)。 計算 [元素取向剪輯](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)的反向傳播漸層。 |
| [**DML_ELEMENT_WISE_CLIP_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_clip_operator_desc)。 描述 DirectML 數學運算子，該運算子會執行元素取向的剪輯函式 f (x) = 夾具 (x * 縮放 + 偏差、minValue、int32.maxvalue) ，其中尺規和偏差詞彙是選擇性的，而夾具 (x) = min (int32.maxvalue、max (minValue、x) ) 。 |
| [**DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_constant_pow_operator_desc)。 描述 DirectML 運算子，該運算子會執行元素取向的常數 power 函式 f (x) = pow (x * 縮放 + 偏差、指數) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_COS_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_cos_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素取向的余弦函數 f (x) = cos (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_COSH_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_cosh_operator_desc)。 描述 DirectML 三角函數運算子，該運算子會執行元素的雙曲余弦函數 f (x) = ( (e ^ x + e ^-x) /2) * scale + 偏差，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_dequantize_linear_operator_desc)。 描述在中的每個元素上執行線性 dequantize 函式的 DirectML 運算子， `InputTensor` 其相對於和中的對應元素 `ScaleTensor` `ZeroPointTensor` 。 |
| [**DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC**](./directml/ns-directml-dml_element_wise_difference_square_operator_desc.md)。 從 *ATensor* 的對應元素減去 *BTensor* 的每個元素，並將結果乘以本身，並將結果放入 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_DIVIDE_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_divide_operator_desc)。 描述 DirectML 的數學運算子，這個運算子會執行將中的每個專案除以 `ATensor` 其對應元素的函式 `BTensor` 。 |
| [**DML_ELEMENT_WISE_ERF_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_erf_operator_desc)。 描述 DirectML 的數學運算子，該運算子會執行元素等級的自然指數函式 f (x) = exp (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_EXP_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_exp_operator_desc)。 描述 DirectML 的數學運算子，該運算子會執行元素等級的自然指數函式 f (x) = exp (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_FLOOR_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_floor_operator_desc)。 描述 DirectML 數學運算子，該運算子會執行元素面向的 floor 函式 f (x) = floor (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_identity_operator_desc)。 描述 DirectML 泛型運算子，這個運算子會執行元素取向的身分識別函式 f (x) = x * 縮放比例 + 偏差。 |
| [**DML_ELEMENT_WISE_IF_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_if_operator_desc)。 描述基本上執行三元語句的 DirectML 數學運算子 `if` 。 |
| [**DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_is_infinity_operator_desc)。 檢查 *InputTensor* 的每個專案是否為 IEEE-754-inf、inf 或兩者（視指定的 *InfinityMode* 而定），並將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_IS_NAN_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_is_nan_operator_desc)。 描述 DirectML 數學運算子，判斷輸入是否為 NaN，elementwise。 |
| [**DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_logical_and_operator_desc)。 描述 DirectML 數學運算子，這個運算子會在中的每個專案和其對應的元素之間執行邏輯 AND 函式 `ATensor` `BTensor` 。 |
| [**DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_logical_equals_operator_desc)。 描述 DirectML 數學運算子，這個運算子會在中的每個專案和其對應的元素之間執行邏輯相等函數 `ATensor` `BTensor` 。 |
| [**DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_logical_greater_than_operator_desc)。 描述 DirectML 數學運算子，這個運算子會在中的每個專案和其對應的元素之間執行邏輯大於函式 `ATensor` `BTensor` 。 |
| [**DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_logical_greater_than_or_equal_operator_desc)。 在輸入張量的每一對對應元素上執行邏輯 *大於或等於* ，將結果 (1 表示 true，將0設為 true) 至對應的 *OutputTensor* 元素。 |
| [**DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_logical_less_than_operator_desc)。 描述 DirectML 數學運算子，這個運算子會在中的每個專案和其對應的元素之間執行邏輯小於函式 `ATensor` `BTensor` 。 |
| [**DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_logical_less_than_or_equal_operator_desc)。 在輸入張量的每一對對應元素上執行邏輯 *小於或等於，並* 將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_logical_not_operator_desc)。 描述在輸入中的每個元素上執行邏輯 NOT 函數的 DirectML 數學運算子。 |
| [**DML_ELEMENT_WISE_LOGICAL_OR_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_logical_or_operator_desc)。 描述 DirectML 數學運算子，這個運算子會在中的每個專案 `ATensor` 與其在中的對應專案之間執行邏輯 OR 函數 `BTensor` 。 |
| [**DML_ELEMENT_WISE_LOGICAL_XOR_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_logical_xor_operator_desc)。 描述 DirectML 數學運算子，這個運算子會在中的每個專案 `ATensor` 與其在中的對應專案之間，執行邏輯專有或 (XOR) 函數 `BTensor` 。 |
| [**DML_ELEMENT_WISE_LOG_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_log_operator_desc)。 描述 DirectML 數學運算子，這個運算子會執行專案自然的自然對數函式 f (x) = log (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_MAX_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_max_operator_desc)。 描述 DirectML 數學縮減運算子，這個運算子會在中的每個專案和其對應的元素之間執行最大函式 `ATensor` `BTensor` 。 |
| [**DML_ELEMENT_WISE_MEAN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_mean_operator_desc)。 描述 DirectML 數學縮減運算子，這個運算子會在中的每個專案和其對應的專案之間執行算術 mean 函數 `ATensor` `BTensor` 。 |
| [**DML_ELEMENT_WISE_MIN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_min_operator_desc)。 描述 DirectML 數學縮減運算子，這個運算子會在中的每個專案和其對應的元素之間執行最小函式 `ATensor` `BTensor` 。 |
| [**DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_modulus_floor_operator_desc)。 針對輸入張量中的每一對對應元素，計算與 Python 模數相同結果的模數，並將結果放入 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_modulus_truncate_operator_desc)。 針對輸入張量的每一對對應元素計算 C 模數運算子，並將結果放入 *OutputTensor* 的對應元素。|
| [**DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_multiply_operator_desc)。 描述 DirectML 的數學運算子，這個運算子會執行將中的每個專案乘以 `ATensor` 其對應元素的函式 `BTensor` 。 |
| [**DML_ELEMENT_WISE_POW_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_pow_operator_desc)。 描述 DirectML 數學運算子，這個運算子會執行專案取向的函式 f (x、指數) = pow (x * 刻度 + 偏差、指數) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_quantize_linear_operator_desc)。 描述 DirectML 運算子，它會針對中的每個專案，執行線性量化函式， `InputTensor` 以及其在和 ZeroPointTensor 中的對應元素 `ScaleTensor` 。 |
| [**DML_ELEMENT_WISE_QUANTIZED_LINEAR_ADD_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_quantized_linear_add_operator_desc)。 將 *ATensor* 中的每個元素加入至 *BTensor* 中的對應元素，並將結果放入 *OutputTensor* 的對應元素。 |
| [**DML_ELEMENT_WISE_RECIP_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_recip_operator_desc)。 描述在輸入中的每個元素上執行交互函數的 DirectML 數學運算子。 |
| [**DML_ELEMENT_WISE_ROUND_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_round_operator_desc)。 將 *InputTensor* 的每個元素四捨五入為整數值，並將結果放入 *OutputTensor* 的對應元素。|
| [**DML_ELEMENT_WISE_SIGN_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_sign_operator_desc)。 描述在輸入上執行 elementwise shrink 啟用函數的 DirectML 運算子。 |
| [**DML_ELEMENT_WISE_SIN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_sin_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素取向的正弦函數 f (x) = sin (x * scale + 偏差) ，其中小數位數和偏差詞彙都是選擇性的。 |
| [**DML_ELEMENT_WISE_SINH_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_sinh_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的雙曲正弦函數 f (x) = ( (e ^ x-e ^-x) /2) * scale + 偏差，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_SQRT_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_sqrt_operator_desc)。 描述在輸入中的每個元素上執行平方根函數的 DirectML 數學運算子。 |
| [**DML_ELEMENT_WISE_SUBTRACT_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_subtract_operator_desc)。 描述 DirectML 的數學運算子，這個運算子會在中從其對應的元素中執行減去中的每個專案 `BTensor` `ATensor` 。 |
| [**DML_ELEMENT_WISE_TAN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_tan_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素取向的正切函數 f (x) = tan (x * scale + 偏差) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_TANH_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_element_wise_tanh_operator_desc)。 描述 DirectML 三角函數運算子，這個運算子會執行元素的反雙曲正切函數 f (x) = tanh (x) * scale + 偏差，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_ELEMENT_WISE_THRESHOLD_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_threshold_operator_desc)。 描述 DirectML 數學運算子，這個運算子會執行元素等級臨界值函式 f (x) = max (x * scale + 偏差，min) ，其中尺規和偏差詞彙是選擇性的。 |
| [**DML_FEATURE_DATA_TENSOR_DATA_TYPE_SUPPORT**](/windows/desktop/api/directml/ns-directml-dml_feature_data_tensor_data_type_support)。 提供有關 DirectML 裝置是否支援張量內特定資料類型的詳細資料。 |
| [**DML_FEATURE_QUERY_TENSOR_DATA_TYPE_SUPPORT**](/windows/desktop/api/directml/ns-directml-dml_feature_query_tensor_data_type_support)。 用來查詢 DirectML 裝置，以支援張量中的特定資料類型。 |
| [**DML_FILL_VALUE_CONSTANT_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_fill_value_constant_operator_desc)。 使用指定的常 *數值* 來填滿 tensor。|
| [**DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_fill_value_sequence_operator_desc)。 使用序列填滿 tensor。|
| [**DML_GATHER_ELEMENTS_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_gather_elements_operator_desc)。 使用索引 tensor，在指定的軸上收集輸入 tensor 的元素，以重新對應至輸入。 |
| [**DML_GATHER_ND_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc)。 使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。|
| [**DML_GATHER_ND1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_gather_nd1_operator_desc)。 使用索引 tensor 將索引重新對應到輸入的整個 subblocks，以收集輸入 tensor 中的元素。|
| [**DML_GATHER_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_gather_operator_desc)。 描述 DirectML 資料重組運算子，當指定了排名 r = 1 的資料 tensor &gt; ，以及排名 q 的索引 tensor 時，會收集資料 (之軸維度中的專案。根據預設，最外層是軸 = = 0) 依索引編制索引，並將其串連于排名 q + (r-1) 的輸出 tensor 中。 |
| [**DML_GEMM_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_gemm_operator_desc)。 描述在輸入上執行一般矩陣乘法函數的 DirectML 運算子： y = Alpha * transposeA () * transposeB (B) + Beta * C。 |
| [**DML_GRAPH_DESC**](/windows/win32/api/directml/ns-directml-dml_graph_desc)。 描述用來編譯結合、優化運算子的 DirectML 運算子圖形。|
| [**DML_GRAPH_EDGE_DESC**](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc)。 [DML_GRAPH_DESC](/windows/win32/api/directml/ns-directml-dml_graph_desc)所定義的 DirectML 運算子圖形內之連接的一般容器，並傳遞至[IDMLDevice1：： CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)。|
| [**DML_GRAPH_NODE_DESC**](/windows/win32/api/directml/ns-directml-dml_graph_node_desc)。 [DML_GRAPH_DESC](/windows/win32/api/directml/ns-directml-dml_graph_desc)所定義之 DirectML 運算子圖形內的節點泛型容器，並傳遞至[IDMLDevice1：： CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)。|
| [**DML_GRU_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_gru_operator_desc)。 描述 DirectML 深度學習運算子，該運算子會在輸入上) 一層閘道週期性單位 (GRU) 函式執行 (標準層。 |
| [**DML_INPUT_GRAPH_EDGE_DESC**](/windows/win32/api/directml/ns-directml-dml_input_graph_edge_desc)。 描述 [DML_GRAPH_DESC](/windows/desktop/api/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)。 此結構是用來定義從圖形輸入到內部節點輸入的連接。|
| [**DML_INTERMEDIATE_GRAPH_EDGE_DESC**](/windows/win32/api/directml/ns-directml-dml_intermediate_graph_edge_desc)。 描述 [DML_GRAPH_DESC](/windows/desktop/api/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)。 此結構是用來定義內部節點之間的連接。|
| [**DML_JOIN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_join_operator_desc)。 描述在輸入張量陣列上執行聯結函數的 DirectML 運算子。 |
| [**DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC**](./directml/ns-directml-dml_local_response_normalization_grad_operator_desc.md)。 計算 [本機回應](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)正規化的反向傳播漸層。 |
| [**DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_local_response_normalization_operator_desc)。 描述在輸入上執行本機回應正規化 (LRN) 函數的 DirectML 運算子。 |
| [**DML_LP_NORMALIZATION_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_lp_normalization_operator_desc)。 描述 DirectML 運算子，這個運算子會沿著輸入 tensor 的指定軸執行 Lp 正規化函數。 |
| [**DML_LP_POOLING_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_lp_pooling_operator_desc)。 描述跨輸入 tensor 執行 Lp 共用函數的 DirectML 運算子。 |
| [**DML_LSTM_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_lstm_operator_desc)。 描述 DirectML 深度學習運算子，這個運算子會在輸入上執行一層完整的長期記憶體 (LSTM) 函數。 |
| [**DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_matrix_multiply_integer_operator_desc)。 在整數資料上執行矩陣乘法函數。|
| [**DML_MAX_POOLING_GRAD_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_max_pooling_grad_operator_desc)。 計算最大共用 (的反向傳播漸層查看 [DML_MAX_POOLING2_OPERATOR_DESC](/windows/win32/api/directml/windows/win32/api/directml/ns-directml-dml_max_pooling2_operator_desc)) 。 |
| [**DML_MAX_POOLING_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_max_pooling_operator_desc)。 描述跨輸入 tensor 執行最大共用函數的 DirectML 運算子。 |
| [**DML_MAX_POOLING1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc)。 描述 DirectML 運算子，這個運算子會根據核心大小、stride 大小和填充長度) ，在輸入 tensor (上執行最大共用函數，y = max (x1 + x2 + .。。 x_pool_size) 。 |
| [**DML_MAX_POOLING2_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_max_pooling2_operator_desc)。 在 [輸入] tensor 上，計算滑動視窗內各元素的最大值，並選擇性地傳回所選最大值的索引。|
| [**DML_MAX_UNPOOLING_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_max_unpooling_operator_desc)。 描述 DirectML 運算子，該運算子會在明確的情況下填滿特定 (圖形的輸出 tensor，或輸入圖形加上填補) 零，然後將輸入 tensor 的每個值，從對應的索引陣列的元素位移寫入輸出 tensor 中。 |
| [**DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc)。 描述在輸入 tensor 上執行 mean 變異正規化函數的 DirectML 運算子。 |
| [**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization1_operator_desc)。 在輸入 tensor 上執行 mean 變異數正規化函數。 這個運算子會計算輸入 tensor 的平均數和變異數，以執行正規化。|
| [**DML_NONZERO_COORDINATES_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_nonzero_coordinates_operator_desc)。 計算輸入 tensor 的所有非零元素的 N 維座標。 |
| [**DML_ONE_HOT_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_one_hot_operator_desc)。 描述 DirectML 運算子，它會產生 tensor，其中每個專案都以 &mdash; ' on ' 或 ' off ' 值填滿兩個值。 |
| [**DML_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_operator_desc)。 運算子描述的一般容器。 您可以使用此結構中指定的參數來建立 DirectML 運算子。 |
| [**DML_OPERATOR_GRAPH_NODE_DESC**](/windows/win32/api/directml/ns-directml-dml_operator_graph_node_desc)。 會說明由 [DML_GRAPH_DESC](/windows/desktop/api/directml/ns-directml-dml_graph_desc) 所定義之 DirectML 運算子圖形內的節點，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)。|
| [**DML_OUTPUT_GRAPH_EDGE_DESC**](/windows/win32/api/directml/ns-directml-dml_output_graph_edge_desc)。 描述 [DML_GRAPH_DESC](/windows/desktop/api/directml/ns-directml-dml_graph_desc) 所定義的 DirectML 運算子圖形內的連接，並傳遞至 [IDMLDevice1：： CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)。 此結構是用來定義從內部節點輸出到圖形輸出的連接。|
| [**DML_PADDING_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc)。 描述 DirectML 資料重組運算子，該運算子會以零 (或其他) 邊緣的值來擴大輸入 tensor。 |
| [**DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_quantized_linear_convolution_operator_desc)。 使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在量化資料上執行向前卷積。 這個運算子在數學上相當於 dequantizing 輸入、convolving，然後量化輸出。|
| [**DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_quantized_linear_matrix_multiply_operator_desc)。 在量化資料上執行矩陣乘法函數。 這個運算子在數學上相當於 dequantizing 輸入，然後執行矩陣相乘，然後量化輸出。|
| [**DML_RANDOM_GENERATOR_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_random_generator_operator_desc)。 以決定性產生的虛擬隨機、一致分散式位來填滿輸出 tensor。 這個運算子也可能會輸出已更新的內部產生器狀態，可在後續執行運算子期間使用。 |
| [**DML_REDUCE_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)。 描述在輸入上執行指定的縮減函數的 DirectML 運算子。 |
| [**DML_RESAMPLE_GRAD_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_resample_grad_operator_desc)。 計算重新取樣的反向傳播漸層 (請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)) 。 |
| [**DML_RESAMPLE_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc)。 描述 DirectML 運算子，這個運算子會使用縮放比例來計算目的地 tensor 大小，以將專案從來源 resamples 到目的地 tensor。 |
| [**DML_RESAMPLE1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)。 使用縮放因數來計算目的地 tensor 大小，以將來源中的專案 Resamples 至目的地 tensor。 您可以使用線性或最接近的相鄰插補模式。|
| [**DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_reverse_subsequences_desc)。 反轉 tensor 的一或多個 *個子序列* 元素。 根據提供的軸和序列長度，選擇要反轉的個子序列集。|
| [**DML_RNN_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_rnn_operator_desc)。 描述 DirectML 深度學習運算子，該運算子會執行一層簡單的遞迴類神經網路， (RNN 輸入上的) 函式。 |
| [**DML_ROI_ALIGN_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_roi_align_operator_desc)。 Performs an ROI align operation, as described in the [Mask R-CNN](https://arxiv.org/abs/1703.06870) paper. 總而言之，此作業會解壓縮來自輸入影像 tensor 的裁剪，並使用指定的 *InterpolationMode*，將其調整為 *OutputTensor* 最後2個維度所指定的一般輸出大小。 |
| [**DML_ROI_ALIGN1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_roi_align1_operator_desc)。 Performs an ROI align operation, as described in the [Mask R-CNN](https://arxiv.org/abs/1703.06870) paper. 總而言之，此作業會從輸入影像 tensor 中取出裁剪的視窗，並使用指定的 *InterpolationMode*，將其大小調整為最後2個 *OutputTensor* 維度所指定的一般輸出大小。 |
| [**DML_ROI_POOLING_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_roi_pooling_operator_desc)。 描述 DirectML 運算子，該運算子會根據感興趣的區域或 ROIs) ，在輸入 tensor (上執行共用函數。 |
| [**DML_SCALAR_UNION**](/windows/win32/api/directml/ns-directml-dml_scalar_union)。 純量類型的聯集。|
| [**DML_SCALE_BIAS**](/windows/desktop/api/directml/ns-directml-dml_scale_bias)。 包含提供給 DirectML 運算子之刻度和偏差詞彙的值。 |
| [**DML_SCATTER_ND_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_scatter_nd_operator_desc)。 將整個輸入 tensor 複製到輸出，然後使用 [更新] tensor 中的對應值來覆寫選取的索引。|
| [**DML_SCATTER_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_scatter_operator_desc)。 描述將整個輸入 tensor 複製到輸出的 DirectML 運算子，然後使用 [更新] tensor 中的對應值來覆寫選取的索引。 |
| [**DML_SIZE_2D**](/windows/desktop/api/directml/ns-directml-dml_size_2d)。 包含值，這些值可代表 DirectML 運算子的大小 (如提供給 tensor 中專案的2-d 平面、立體小數位數或任何2D 寬度/高度值的) 運算子。 |
| [**DML_SLICE_GRAD_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_slice_grad_operator_desc)。 計算配量的反向傳播漸層 (請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)) 。 |
| [**DML_SLICE_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_slice_operator_desc)。 描述 DirectML 資料重組運算子，這個運算子會沿著多個軸產生輸入 tensor 的配量。 |
| [**DML_SLICE1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)。  (輸入 tensor 的「配量」 ) 解壓縮單一子領域。|
| [**DML_SPACE_TO_DEPTH_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_space_to_depth_operator_desc)。 描述 DirectML 資料重組運算子，將空間資料的區塊重新排列為深度。 |
| [**DML_SPACE_TO_DEPTH1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_space_to_depth1_operator_desc)。 將空間資料的區塊重新排列為深度。 運算子會輸出輸入 tensor 的複本，其中高度和寬度維度的值會移至深度維度。|
| [**DML_SPLIT_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_split_operator_desc)。 描述 DirectML 資料重組運算子，將輸入 tensor 分割成多個輸出張量，沿著指定的軸。 |
| [**DML_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)。 DirectML tensor 描述的一般容器。 |
| [**DML_TILE_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_tile_operator_desc)。 描述 DirectML 資料重組運算子，該運算子會藉由並排輸入 tensor 來建立輸出 tensor。 |
| [**DML_TOP_K_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_top_k_operator_desc)。 描述可在指定的軸上抓取前 K 個元素的 DirectML 縮減運算子。 |
| [**DML_TOP_K1_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_top_k1_operator_desc)。 選取每個序列中的最大或最小 *K* 元素，沿著 *InputTensor* 軸，然後分別傳回 *OutputValueTensor* 和 *OutputIndexTensor* 中這些元素的值和索引。|
| [**DML_UPSAMPLE_2D_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc)。 描述 upsamples 輸入 tensor 中所含影像的 DirectML 影像處理運算子。 |
| [**DML_VALUE_SCALE_2D_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_value_scale_2d_operator_desc)。 描述 DirectML 運算子，該運算子會對輸入 tensor 中的值執行元素取向的縮放和偏差函數。 |

## <a name="related-topics"></a>相關主題

* [DirectML 參考](direct3d-directml-reference.md)
* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)