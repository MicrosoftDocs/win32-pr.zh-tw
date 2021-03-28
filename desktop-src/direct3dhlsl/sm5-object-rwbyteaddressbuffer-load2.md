---
title: RWByteAddressBuffer：： Load2 (uint) 函數
description: 取得兩個值。 |RWByteAddressBuffer：： Load2 (uint) 函數
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
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
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974396"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>RWByteAddressBuffer：： Load2 (uint) 函數

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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Load2 方法](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




