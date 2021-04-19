---
description: COARefTime 類別會轉換秒和 100-毫微秒單位之間的參考時間。
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: 'COARefTime 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989254"
---
# <a name="coareftime-class"></a>COARefTime 類別

![coareftime 類別階層](images/cutil05.png)

`COARefTime`類別會轉換秒和 100-毫微秒單位之間的參考時間。

這個類別會在與 C/c + + 相容的自動化和參考時間相容的參考時間之間進行轉換。 自動化相容的介面會使用 **雙精度浮點數** 來代表時間（以秒為單位）。 其他介面會使用64位的 **LONGLONG** 值，以 100-毫微秒單位表示時間。 以下是針對這些值定義的類型：

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

篩選準則可以使用 `COARefTime` 類別在這兩種格式之間進行轉換。 這個類別衍生自 [**CRefTime**](creftime.md) 類別。



| 公用方法                                          | Description                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**COARefTime**](coareftime-coareftime.md)             | 函式方法。                                                   |
| 運算子                                               | 說明                                                           |
| [**double**](coareftime-double.md)                     | 將參考時間轉換為 **雙精度** 值。                    |
| [**參考 \_ 時間**](coareftime-reference-time.md)    | 將物件轉換為 **參考 \_ 時間** 值。                      |
| [**運算子 =**](coareftime-operator-assign.md)        | 指派新的參考時間。                                         |
| [**operator = =**](coareftime-operator-eq.md)           | 測試兩個參考時間是否相等。                       |
| [**operator！ =**](cmediatype-operator-neq.md)          | 測試兩個參考時間是否不相等。                     |
| [**運算子 <**](coareftime-operator-lt.md)         | 測試某個參考時間是否小於另一個參考時間。                     |
| [**運算子 >**](coareftime-operator-gt.md)         | 測試某個參考時間是否大於另一個參考時間。                  |
| [**運算子 <=**](coareftime-operator-lteq.md)      | 測試某個參考時間是否小於或等於另一個參考時間。         |
| [**運算子 >=**](coareftime-operator-gteq.md)      | 測試某個參考時間是否大於或等於另一個參考時間。      |
| [**運算子 +**](coareftime-operator-plus.md)          | 加入兩個參考時間。                                             |
| [* * 運算子 * *](coareftime-operator-minus.md)         | 從另一個參考時間減去一個參考時間。                            |
| [**運算子 + =**](coareftime-operator-plus-assign.md)  | 加入兩個參考時間，並將結果指派給這個物件。      |
| [**運算子 =**](coareftime-operator-minus-assign.md) | 減去兩個參考時間，並將結果指派給這個物件。 |
| [**運算元 \***](coareftime-operator-mult.md)         | 以值乘以參考時間。                               |
| [**運算子**](coareftime-operator-div.md)           | 將參考時間除以某個值。                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




