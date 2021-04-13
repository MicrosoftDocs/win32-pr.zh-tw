---
title: Buffer：： Operator 函數
description: 傳回唯讀的資源變數。 |Buffer：： Operator 函數
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Operator 函數直接寫入
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386348"
---
# <a name="bufferoperator--function"></a>Buffer：： Operator 函數

傳回唯讀的資源變數。

## <a name="syntax"></a>語法

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pos* \[在\]
</dt> <dd>

類型： **uint**

索引位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




