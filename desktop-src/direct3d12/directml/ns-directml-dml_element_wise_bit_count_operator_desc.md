---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: 針對輸入 tensor 的每個元素計算位 NOT，並將結果寫入輸出 tensor。
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: bb42be1e1f00fcf749ed271d55a7958b43464f1a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981920"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC 結構 (directml .h) 

針對輸入 tensor 的每個元素計算位 NOT，並將結果寫入輸出 tensor。

輸入和輸出 tensor 必須有相同的 *DimensionCount*、 *大小* 和 *資料類型*。

這個運算子支援就地執行，這表示允許輸出 tensor 在系結期間為輸入 tensor 加上別名。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要從中讀取的輸入 tensor。

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的輸出 tensor。

## <a name="example"></a>範例

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | UINT32、UINT16、UINT8 |
| OutputTensor | 輸出 | 1至8 | UINT32、UINT16、UINT8 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |