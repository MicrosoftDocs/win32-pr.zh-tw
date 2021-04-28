---
description: CDynamicOutputPin。 CDynamicOutputPin 函式-函數方法。
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: 'CDynamicOutputPin. CDynamicOutputPin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099306"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a>CDynamicOutputPin. CDynamicOutputPin 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CDynamicOutputPin(
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

包含物件名稱之字串的指標。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*pFilter* 
</dt> <dd>

建立此釘選之篩選準則的指標。

</dd> <dt>

*pLock* 
</dt> <dd>

[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。 使用與篩選鎖定相同的重要區段 [ **CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。 在建立物件之前，將值初始化為「 \_ 確定」。 只有在發生錯誤時，才會變更此值。

</dd> <dt>

*pName* 
</dt> <dd>

包含 pin 識別碼之寬字元字串的指標。 如需詳細資訊，請參閱 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




