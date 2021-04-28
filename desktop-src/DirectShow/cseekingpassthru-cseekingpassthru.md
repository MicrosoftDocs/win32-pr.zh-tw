---
description: CSeekingPassThru。 CSeekingPassThru 函式-函數方法。
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: 'CSeekingPassThru. CSeekingPassThru (Seekpt. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085376"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a>CSeekingPassThru. CSeekingPassThru 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

包含物件名稱的字串。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md) 。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 忽略。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Seekpt (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSeekingPassThru 類別**](cseekingpassthru.md)
</dt> </dl>

 

 




