---
title: ByteAddressBuffer：： Load4 (uint) 函數
description: 取得四個值。 |ByteAddressBuffer：： Load4 (uint) 函數
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
keywords:
- Load4 函式 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a623c62ce9038d4e06cfbb952808aeb0530cb2e937c83578d9ef0e71c9b0a038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509998"
---
# <a name="byteaddressbufferload4uint-function"></a>ByteAddressBuffer：： Load4 (uint) 函數

取得四個值。

## <a name="syntax"></a>語法

``` syntax
uint4 Load4(
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

類型： **uint4**

四個值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Load4 方法](byteaddressbuffer-load4.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




