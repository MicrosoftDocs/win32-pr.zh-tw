---
description: 結構 CMsg 物件。
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: 'CMsg. CMsg (Msgthrd. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000832"
---
# <a name="cmsgcmsg-constructor"></a>CMsg. CMsg 函數

結構 [**CMsg**](cmsg.md) 物件。

## <a name="syntax"></a>語法


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*u* 
</dt> <dd>

要求碼，由執行緒類別的用戶端所定義，並由覆寫的背景工作執行緒函數理解。

</dd> <dt>

*dw* 
</dt> <dd>

要求碼的旗標參數。

</dd> <dt>

*lp* 
</dt> <dd>

背景工作執行緒所需的資料指標，作為參數或傳回值。 此資料不應以堆疊為基礎，因為它會在完成佇列作業之後被參考一段時間。

</dd> <dt>

*pEvent* 
</dt> <dd>

背景工作執行緒可以指示的事件物件指標，表示作業已完成。

</dd> </dl>

## <a name="remarks"></a>備註

此成員函式包含 [**CMsgThread**](cmsgthread.md) worker 執行緒的要求，以採取動作。 處理此訊息時，會將所有參數傳遞至背景工作執行緒函式作為參數。 參數的意義是由呼叫工作者執行緒的用戶端函數以及提供工作者執行緒執行函式的衍生類別所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




