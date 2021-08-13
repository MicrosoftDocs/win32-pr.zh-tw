---
title: RWByteAddressBuffer：： Store4 函數
description: 設定四個值。
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Store4 函式 HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc644647616f6c6654023be23aaa8e420dbb85ad439547d1befd44c0ea7b210c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789969"
---
# <a name="store4-function"></a>Store4 函式

設定四個值。

## <a name="syntax"></a>語法

``` syntax
void Store4(
  in uint address,
  in uint4 values
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

類型： **uint4**

四個輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




