---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: 檢查 *InputTensor* 的每個專案是否為 IEEE-754-inf、inf 或兩者（視指定的 *InfinityMode* 而定），並將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803101"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC 結構 (directml .h) 

檢查 *InputTensor* 的每個專案是否為 IEEE-754-inf、inf 或兩者（視指定的 *InfinityMode* 而定），並將結果 (1 表示 true、0表示 false) 至 *OutputTensor* 的對應元素。

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要從中讀取的輸入 tensor。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的輸出 tensor。


`InfinityMode`

類型： **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**

[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) ，判斷要檢查的無限大正負號。

* 如果 **DML_IS_INFINITY_MODE_EITHER**，則如果專案為-inf 或 inf，則會傳回1，否則會傳回0。
* 如果 **DML_IS_INFINITY_MODE_POSITIVE**，則如果元素為 inf，則會傳回1，否則會傳回0。
* 如果 **DML_IS_INFINITY_MODE_NEGATIVE**'，則如果元素為-inf，則會傳回1，否則會傳回0。


## <a name="remarks"></a>備註
## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor* 和 *OutputTensor* 必須有相同的 *DimensionCount* 和 *大小*。

## <a name="tensor-support"></a>Tensor 支援
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 和更新版本
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16 |
| OutputTensor | 輸出 | 1至8 | UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 和更新版本
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16 |
| OutputTensor | 輸出 | 4 | UINT8 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10，版本 2004 (10.0;組建 19041)  |
| **最低支援的伺服器** | Windows Server，版本 2004 (10.0;組建 19041)  |
| **標頭** | directml。h |