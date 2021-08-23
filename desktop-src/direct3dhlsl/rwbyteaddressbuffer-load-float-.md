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
ms.openlocfilehash: 4885a94041201eed790768cd6b75d07f8bd5ccd24b9d37ce56df734adced15ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672158"
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



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 




