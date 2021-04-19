---
title: DirectML 列舉
description: 下列列舉是在 DirectML 中宣告。
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: 6479b1bfe4216a5bdbe8aaee78c258f6f4a64f94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106992630"
---
# <a name="directml-enumerations"></a>DirectML 列舉

下列列舉是在 DirectML 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題和描述 |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/direct3d12/directml/ne-directml-dml_axis_direction)。 定義常數，以指定運算子的指定軸的方向 (例如，加總，選取最小的專案，然後選取) 的最小元素。 |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type)。 定義常數，指定) 系結描述 [DML_BINDING_DESC 結構](/windows/desktop/api/directml/ns-directml-dml_binding_desc)所參考之資源 (的本質。 |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction)。 定義常數，指定 DirectML 卷積運算子的方向 (如 [DML_CONVOLUTION_OPERATOR_DESC 結構](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)) 所述。 |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode)。 定義常數，指定 DirectML 卷積運算子的模式 (如 [DML_CONVOLUTION_OPERATOR_DESC 結構](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)) 所述。 |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags)。 提供其他裝置建立選項給 [DMLCreateDevice](/windows/desktop/api/directml/nf-directml-dmlcreatedevice)。 |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/direct3d12/directml/ne-directml-dml_depth_space_order)。 定義常數，用於控制 DirectML 運算子 [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) 和 **DML_OPERATOR_SPACE_TO_DEPTH1** 中所套用的轉換。 |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags)。 提供選項給 DirectML，以控制操作員的執行。 |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature)。 定義一組可從 DirectML 裝置查詢的選用特性和功能。 |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/direct3d12/directml/ne-directml-dml_graph_edge_type)。 定義指定圖形邊緣類型的常數。 如需此列舉的用法，請參閱 [DML_GRAPH_EDGE_DESC](./directml/ns-directml-dml_graph_edge_desc.md) 。 |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/direct3d12/directml/ne-directml-dml_graph_node_type)。 定義指定圖形節點類型的常數。 如需此列舉的用法，請參閱 [DML_GRAPH_NODE_DESC](./directml/ns-directml-dml_graph_node_desc.md) 。 |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode)。 定義常數，指定 DirectML upsample 2-d 運算子的模式 (如 [DML_UPSAMPLE_2D_OPERATOR_DESC 結構](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc)) 所述。 |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform)。 定義常數，指定要套用至 DirectML tensor 的矩陣轉換。 |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type)。 定義運算子描述的型別。 |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode)。 定義常數，指定 DirectML pad 運算子 (的模式，如 [DML_PADDING_OPERATOR_DESC 結構](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc)) 所述。 |
| [**DML_RANDOM_GENERATOR_TYPE**](./directml/ne-directml-dml_random_generator_type.md)。 定義常數，指定隨機亂數產生器的類型。 |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction)。 定義常數，以指定週期性 DirectML 運算子的方向。 |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function)。 定義常數，指定用於 DirectML 減少運算子的特定縮減演算法 (如 [DML_REDUCE_OPERATOR_DESC 結構](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)) 所述。 |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type)。 指定 tensor 中之值的資料類型。 |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags)。 在 tensor 描述中指定其他選項。 |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type)。 識別 tensor 描述的類型。 |

## <a name="related-topics"></a>相關主題

* [DirectML 參考](direct3d-directml-reference.md)
* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)