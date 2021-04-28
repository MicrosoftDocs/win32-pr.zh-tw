---
description: CBasePin。 CBasePin 函式-函數方法。
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: 'CBasePin. CBasePin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099426"
---
# <a name="cbasepincbasepin-constructor"></a>CBasePin. CBasePin 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
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

[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。 可以是與 filter lock [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)相同的重要區段。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。 在建立物件之前，將值初始化為「 \_ 確定」。 只有在發生錯誤時，才會變更此值。

</dd> <dt>

*pName* 
</dt> <dd>

包含 pin 名稱的寬字元字串。 如需詳細資訊，請參閱 [**CBasePin：： QueryPinInfo**](cbasepin-querypininfo.md)。

</dd> <dt>

*dir* 
</dt> <dd>

指定釘選方向的 [**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction) 列舉的成員。

</dd> </dl>

## <a name="remarks"></a>備註

*PLock* 所指定的重要區段會將釘選的狀態序列化，包括其線上狀態、配置器的選擇、媒體類型，以及排清作業的狀態。 請勿使用這個重要區段來序列化串流作業。 如需詳細資訊，請參閱 [篩選圖形中的](data-flow-in-the-filter-graph.md)資料流程。

篩選可能會在其函式方法中建立釘選，因此在此時， *pFilter* 指標可能不會參考有效的物件。 儲存指標，但不要在釘選的函式內進行取值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




