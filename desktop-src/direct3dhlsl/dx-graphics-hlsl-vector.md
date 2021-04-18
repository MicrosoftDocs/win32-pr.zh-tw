---
title: '向量類型 (HLSL) '
description: 向量包含一到四個純量元件;向量的每個元件都必須是相同的類型。
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- 向量類型 HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "104991854"
---
# <a name="vector-type"></a>向量類型

向量包含一到四個純量元件;向量的每個元件都必須是相同的類型。



|                     |
|---------------------|
| **TypeNumber 名稱** |



 


```
TypeComponents Name
```



## <a name="components"></a>單元



| 項目                                                                                                                             | 描述                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | 包含兩個部分的單一名稱。 第一個部分是純 [量類型的](dx-graphics-hlsl-data-types.md) 其中一個。 第二個部分是元件的數目，必須介於1到4（含）之間。<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>                                         | 可唯一識別變數名稱的 ASCII 字串。<br/>                                                                                                                                                |



 

## <a name="examples"></a>範例

以下是一些範例：


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



您也可以使用此語法來宣告向量：


```
vector <Type, Number> VariableName
```



以下是一些範例：


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





