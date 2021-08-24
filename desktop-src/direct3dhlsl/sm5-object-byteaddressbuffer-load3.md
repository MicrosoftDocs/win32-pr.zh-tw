---
title: ByteAddressBuffer：： Load3 (uint) 函數
description: 取得三個值。 |ByteAddressBuffer：： Load3 (uint) 函數
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3 函式 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bd36958eb2c16d45e6228c9919cb22bb772c8861131c26710fff032276bce6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510008"
---
# <a name="byteaddressbufferload3uint-function"></a>ByteAddressBuffer：： Load3 (uint) 函數

取得三個值。

## <a name="syntax"></a>語法

``` syntax
uint3 Load3(
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

類型： **uint3**

三個值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Load3 方法](byteaddressbuffer-load3.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




