---
title: OutputPatch：： Operator 函數
description: 傳回修補程式中的第 n 個控制點。 |OutputPatch：： Operator 函數
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 684925491ce7b5ac50cb293b3c8a0270557c9b9e65fcfcde63e9699127bc7ed0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023468"
---
# <a name="outputpatchoperator--function"></a>OutputPatch：： Operator 函數

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
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




