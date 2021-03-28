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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195962"
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




