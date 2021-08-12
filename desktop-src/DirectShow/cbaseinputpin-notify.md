---
description: CBaseInputPin。通知方法-通知方法會通知 pin，要求品質變更。 這個方法會執行 IQualityControl：： Notify 方法。
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: 'CBaseInputPin： Notify 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2067c7698c1af7d7295cffed552ab4f58d0402594dd13bfd82224c81652b9aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659161"
---
# <a name="cbaseinputpinnotify-method"></a>CBaseInputPin。通知方法

`Notify`方法會通知 pin，要求品質變更。 這個方法會 [**執行 IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSelf* 
</dt> <dd>

傳送品質控制訊息之篩選準則的指標。

</dd> <dt>

*問* 
</dt> <dd>

包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

篩選通常會將品質控制訊息傳遞至上游輸出 pin，而不是輸入 pin。 因此，這個方法會傳回 \_ [確定]，而不執行任何操作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> <dt>

[品質控制管理](quality-control-management.md)
</dt> </dl>

 

 




