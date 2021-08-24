---
title: ByteAddressBuffer：： Load (int) 函數
description: 取得一個值。 |ByteAddressBuffer：： Load (int) 函數
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Load function HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a9854f85ebd92b9f57e4b2339f374ad8f7816ea7b9ba31e37c9404b08c14864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671448"
---
# <a name="byteaddressbufferloadint-function"></a>ByteAddressBuffer：： Load (int) 函數

取得一個值。

## <a name="syntax"></a>語法

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*位址* \[在\]
</dt> <dd>

類型： **int**

輸入位址（以位元組為單位），必須是4的倍數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint**

一個值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](byteaddressbuffer-load.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




