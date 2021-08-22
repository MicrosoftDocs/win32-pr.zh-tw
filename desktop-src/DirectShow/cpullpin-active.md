---
description: 使用中的方法會建立從輸出圖釘提取資料的工作者執行緒。 這個方法也會認可配置器。
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: 'CPullPin 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6572ad0b415f4c1a51133d080e84a2e869787dea0c23614478b09c7b86296b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073522"
---
# <a name="cpullpinactive-method"></a>CPullPin 方法

使用 **中** 的方法會建立從輸出圖釘提取資料的工作者執行緒。 這個方法也會認可配置器。

## <a name="syntax"></a>語法


```C++
HRESULT Active();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | 描述                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                                                   |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | Pin 連接未正確建立。<br/>          |
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 無法建立執行緒，或執行緒已經存在。<br/> |



 

## <a name="remarks"></a>備註

當擁有篩選變成作用中時，請呼叫這個方法。  (如果您的輸入 pin 衍生自 [**CBasePin**](cbasepin.md)，請覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。 ) 

在呼叫這個方法之前，請先呼叫 [**CPullPin：：連線**](cpullpin-connect.md)方法，以建立與輸出圖釘的連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




