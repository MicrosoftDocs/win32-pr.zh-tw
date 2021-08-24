---
title: ByteAddressBuffer：： Load2 (uint) 函數
description: 取得兩個值。 |ByteAddressBuffer：： Load2 (uint) 函數
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- Load2 函式 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fac3b1cd0fffca1a68089c3c21bfd5d6aea5f270493319b044a0bbe290d88a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845728"
---
# <a name="byteaddressbufferload2uint-function"></a>ByteAddressBuffer：： Load2 (uint) 函數

取得兩個值。

## <a name="syntax"></a>語法

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*位址* \[在\]
</dt> <dd>

類型： **uint**

輸入位址（以位元組為單位），必須是4的倍數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint2**

兩個值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Load2 方法](byteaddressbuffer-load2.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




