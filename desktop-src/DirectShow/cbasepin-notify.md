---
description: CBasePin。通知方法-通知方法會通知 pin，要求品質變更。 這個方法會執行 IQualityControl：： Notify 方法。
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: 'CBasePin： Notify 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e74a8880e446300ca142bfcf28633d267d184178a0c3572c3a8049667536978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910438"
---
# <a name="cbasepinnotify-method"></a>CBasePin。通知方法

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

傳遞品質控制訊息之篩選準則的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標。

</dd> <dt>

*問* 
</dt> <dd>

指定包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

基類會傳回 E \_ >notimpl。

## <a name="remarks"></a>備註

輸出圖釘應覆寫此方法，以接受品質控制訊息。

如果已安裝外部品質管制員 (請參閱 [**CBasePin：： SetSink**](cbasepin-setsink.md)) ，將訊息傳遞給該品質管制員。 否則，篩選器應該會處理訊息本身，或將訊息傳遞至上游。 如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




