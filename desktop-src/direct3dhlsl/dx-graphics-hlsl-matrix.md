---
title: 矩陣類型
description: 矩陣是一種特殊的資料類型，包含一個和十六個元件。 矩陣的每個元件都必須屬於相同類型。
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- 矩陣類型 HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e6b98309c760a3da4d1e9c488e4aed049aa34f0b449042e8f00a02426cc513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726168"
---
# <a name="matrix-type"></a>矩陣類型

矩陣是一種特殊的資料類型，包含一個和十六個元件。 矩陣的每個元件都必須屬於相同類型。



|                         |
|-------------------------|
| **TypeComponents 名稱** |



 

## <a name="components"></a>單元



| 項目                                                                                                                             | 描述                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | 包含三個部分的單一名稱。 第一個部分是純 [量類型的](dx-graphics-hlsl-data-types.md) 其中一個。 第二個部分是資料列的數目。 第三個部分是資料行的數目。 資料列和資料行的數目是介於1到4（含）之間的正整數。<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**<br/>                                         | 可唯一識別變數名稱的 ASCII 字串。<br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a>範例

以下是一些範例：


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



您也可以使用此語法來宣告矩陣：


```
matrix <Type, Number> VariableName
```



矩陣類型會使用角括弧來指定類型、資料列數目和資料行數目。 這個範例會建立具有兩個數據列和兩個數據行的浮點數矩陣。 您可以使用任何純量資料類型。

以下是範例：


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





