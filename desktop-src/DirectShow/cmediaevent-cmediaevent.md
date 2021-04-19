---
description: 函式方法。
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: 'CMediaEvent. CMediaEvent (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77b87fa589728592874b0dea96f7b6efca501471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982609"
---
# <a name="cmediaeventcmediaevent-constructor"></a>CMediaEvent. CMediaEvent 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

用於偵測之物件名稱的指標。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。

</dd> </dl>

## <a name="remarks"></a>備註

在靜態記憶體中配置 *pName* 參數。 這個名稱會在物件的建立和刪除時，出現在偵錯工具的終端機上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaEvent 類別**](cmediaevent.md)
</dt> </dl>

 

 




