---
title: InputPatch：： Operator 函數
description: 傳回修補程式中的第 n 個控制點。 |InputPatch：： Operator 函數
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
keywords:
- 運算子函式 HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81c768d138f6ee1853f9930a56f1a1864b468e8be9ff421f4dba1698b790053c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986028"
---
# <a name="inputpatchoperator--function"></a>InputPatch：： Operator 函數

傳回修補程式中的 <sup>第</sup> *n* 個控制點。

## <a name="syntax"></a>語法

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*n* \[ in\]
</dt> <dd>

類型： **uint**

輸入索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **T**

第 *n*<sup></sup>個控制點。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




