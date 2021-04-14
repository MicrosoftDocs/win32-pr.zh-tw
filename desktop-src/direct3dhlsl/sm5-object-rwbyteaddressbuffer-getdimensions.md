---
title: RWByteAddressBuffer：： GetDimensions 函數
description: 取得緩衝區的長度。 |RWByteAddressBuffer：： GetDimensions 函數
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322408"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a>RWByteAddressBuffer：： GetDimensions 函數

取得緩衝區的長度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*dim* \[ out\]
</dt> <dd>

類型： **uint**

緩衝區的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




