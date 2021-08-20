---
title: 'max 宏 (Minwindef .h) '
description: Max 宏會比較兩個值並傳回較大的值。 資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。 引數的資料類型和傳回值相同。
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- 最大宏 Windows 多媒體
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc592fcc588c14ee04c1f595c5b5bc95c860b2ab0b761906886010db478d5f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138644"
---
# <a name="max-macro"></a>max 巨集

**Max** 宏會比較兩個值並傳回較大的值。 資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。 引數的資料類型和傳回值相同。

## <a name="syntax"></a>語法


```C++
 max(
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

傳回值是兩個指定值的最大值。

## <a name="remarks"></a>備註

**Max** 宏的定義如下：


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Minwindef。h</dt> </dl> |



 

 





