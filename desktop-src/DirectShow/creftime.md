---
description: CRefTime 類別是用來管理參考時間的 helper 類別。
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: 'CRefTime 類別 (Reftime) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d8f9d30b057c1c011dcbff1b7d8c88e9183d50ca1fc2b7dd046b79fe8279d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953950"
---
# <a name="creftime-class"></a>CRefTime 類別

![creftime 類別階層](images/cutil05.png)

`CRefTime`類別是用來管理參考時間的 helper 類別。

*參考時間* 是以 100-毫微秒單位表示的時間單位。 這個類別會共用與 [**參考 \_ 時間**](reference-time.md) 資料類型相同的資料版面配置，但會加入一些可提供比較、轉換和算術函數的方法和運算子。 如需參考時間的詳細資訊，請參閱[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。



| Public 成員變數                                                 | 描述                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**m \_ 時間**](creftime-m-time.md)                                      | 指定 **參考 \_ 時間** 值。              |
| 公用方法                                                          | 描述                                           |
| [**CRefTime**](creftime-creftime.md)                                   | 函式方法。                                   |
| [**GetUnits**](creftime-getunits.md)                                   | 以 100-毫微秒單位來抓取參考時間。 |
| [**Millisecs**](creftime-millisecs.md)                                 | 將參考時間轉換為毫秒。          |
| 運算子                                                               | 說明                                           |
| [**運算子參考 \_ 時間 ()**](creftime-operator-reference-time-.md) | 將物件轉換為 **參考 \_ 時間** 資料類型。  |
| [**運算子 =**](creftime-operator-assign.md)                           | 指派新的參考時間。                         |
| [**運算子 + =**](creftime-operator-plus-assign.md)                     | 加入兩個參考時間。                             |
| [**運算子 =**](creftime-operator-minus-assign.md)                    | 從另一個參考時間減去一個參考時間。            |



 

## <a name="remarks"></a>備註

使用此類別可能會有缺陷。 如果您套用 + = 運算子和 **CRefTime** 物件做為左運算元，並將 **LONG** 類型的變數套用為右運算元，則編譯器會將右運算元隱含地轉換為 **CRefTime** 物件。 這項強制型轉會使用將毫秒轉換成參考時間單位的 **CRefTime** 函式 \_ ; 因此，右運算元乘以10000：


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



不過，使用 + 運算子時，也不會發生相同的事：


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Reftime (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




