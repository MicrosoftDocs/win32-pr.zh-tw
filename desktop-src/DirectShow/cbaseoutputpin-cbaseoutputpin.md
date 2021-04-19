---
description: 函式方法。
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: 'CBaseOutputPin. CBaseOutputPin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0461c5056ee48caa19f21d1fcb8fcf1636157d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978471"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a>CBaseOutputPin. CBaseOutputPin 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObjectName* 
</dt> <dd>

包含物件之偵錯工具名稱的字串。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*pFilter* 
</dt> <dd>

建立此釘選之篩選準則的指標。

</dd> <dt>

*pLock* 
</dt> <dd>

[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。 這可以是與 filter lock [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)相同的重要區段。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。

</dd> <dt>

*pName* 
</dt> <dd>

包含 pin 名稱的寬字元字串 (也用來作為 pin 識別碼) 。

</dd> </dl>

## <a name="remarks"></a>備註

所有參數都會直接傳遞至 [**CBasePin**](cbasepin.md) 的函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




