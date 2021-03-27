---
title: RWByteAddressBuffer：： Store 函數
description: 設定一個值。
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- 存放區函式 HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104971485"
---
# <a name="store-function"></a>Store 函數

設定一個值。

## <a name="syntax"></a>語法

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*位址* \[在\]
</dt> <dd>

類型： **uint**

輸入位址（以位元組為單位），必須是4的倍數。

</dd> <dt>

*值* \[在\]
</dt> <dd>

類型： **uint**

一個輸入值。

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

 

 




