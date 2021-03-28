---
title: RWByteAddressBuffer：： Load (int) 函數
description: 取得一個值。 |RWByteAddressBuffer：： Load (int) 函數
ms.assetid: C95C865E-E44D-46DC-A076-BD2903758432
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
ms.openlocfilehash: 6efff2363f844e6940b489dd2dda48cbdc0c6b75
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974036"
---
# <a name="rwbyteaddressbufferloadint-function"></a>RWByteAddressBuffer：： Load (int) 函數

取得一個值。

## <a name="syntax"></a>語法


``` syntax
uint Load(
  in int Location
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位置* \[在\]
</dt> <dd>

類型： **int**

緩衝區的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint**

一個值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 




