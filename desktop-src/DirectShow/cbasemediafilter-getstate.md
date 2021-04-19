---
description: '>getstate 方法會抓取物件的狀態 (執行中、已停止或已暫停) 。 這個方法會實 IMediaFilter：： >getstate 方法。'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: 'CBaseMediaFilter. >getstate 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977432"
---
# <a name="cbasemediafiltergetstate-method"></a>CBaseMediaFilter. >getstate 方法

方法會抓取 `GetState` 物件的狀態 (執行中、已停止或已暫停) 。 這個方法會實 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

逾時間隔（以毫秒為單位）。

</dd> <dt>

*State* 
</dt> <dd>

變數的指標，此變數會接收 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，指出物件的狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="remarks"></a>備註

在基類中，所有狀態轉換都是同步的，而 *dwMilliSecsTimeout* 參數則會被忽略。 如果衍生類別會執行非同步狀態轉換，它應該覆寫此方法以在狀態轉換期間等候，並在 *dwMilliSecsTimeout* 毫秒內等候。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseMediaFilter 類別**](cbasemediafilter.md)
</dt> </dl>

 

 




