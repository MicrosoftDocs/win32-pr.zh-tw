---
title: 'min 宏 (Minwindef .h) '
description: Min 宏會比較兩個值並傳回較小的值。 資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。 引數的資料類型和傳回值相同。
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- 最小宏 Windows 多媒體
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832adc4a4d326ca8e0689d1ca44ade2e0b77db770cabe6042e42c47e23a44f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985670"
---
# <a name="min-macro"></a>min 巨集

**Min** 宏會比較兩個值並傳回較小的值。 資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。 引數的資料類型和傳回值相同。

## <a name="syntax"></a>語法


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*value1* 
</dt> <dd>

指定兩個值的第一個。

</dd> <dt>

*value2* 
</dt> <dd>

指定兩個值的第二個。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是兩個指定值的較小者。

## <a name="remarks"></a>備註

**Min** 巨集定義如下：


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Minwindef。h</dt> </dl> |



 

 





