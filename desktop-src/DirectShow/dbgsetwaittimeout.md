---
description: 設定調試超時值。 在零售組建中略過。
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: 'DbgSetWaitTimeout 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976021"
---
# <a name="dbgsetwaittimeout-function"></a>DbgSetWaitTimeout 函式

設定調試超時值。 在零售組建中略過。

## <a name="syntax"></a>語法


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwTimeout* 
</dt> <dd>

超時值（以毫秒為單位），或無限期等候無限期等候。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

在 debug 組建中， [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) 和 [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) 函數會使用此值做為逾時間隔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxdebug (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[等候調試函式](wait-debugging-functions.md)
</dt> </dl>

 

 




