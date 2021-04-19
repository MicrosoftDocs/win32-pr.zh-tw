---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: 使用指定的常 *數值* 來填滿 tensor。
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: d2b69f1f6b1c9768c24cab9a58bba3c3cadb04bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106989102"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a>DML_FILL_VALUE_CONSTANT_OPERATOR_DESC 結構 (directml .h) 

使用指定的常 *數值* 來填滿 tensor。 這個運算子會執行下列虛擬虛擬。

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a>成員

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 這個 tensor 可能會有任何大小。


`ValueDataType`

類型： **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**

*值* 欄位的資料類型，必須符合 *OutputTensor。*


`Value`

類型： **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**

用來填滿輸出的常數值， *ValueDataType* 決定如何解讀欄位。

## <a name="examples"></a>範例

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |