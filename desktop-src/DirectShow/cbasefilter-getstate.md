---
description: '>getstate 方法會 (執行中、已停止或已暫停的) 來抓取篩選的狀態。 這個方法會實 IMediaFilter：： >getstate 方法。'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: 'CBaseFilter. >getstate 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b6ed61b8b1e72652e9590d11827322256d4923bd92405206e5c5419cd5e7ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017166"
---
# <a name="cbasefiltergetstate-method"></a>CBaseFilter. >getstate 方法

`GetState`方法會 (執行中、已停止或已暫停) 來抓取篩選的狀態。 這個方法會實 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) 方法。

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

變數的指標，此變數會接收 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，以指出篩選的狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="remarks"></a>備註

在基類中，所有狀態轉換都是同步的，而 *dwMilliSecsTimeout* 參數則會被忽略。 如果衍生類別會執行非同步狀態轉換，它應該覆寫此方法以在狀態轉換期間等候，並在 *dwMilliSecsTimeout* 毫秒內等候。

如果您的篩選準則不會在暫停時傳遞資料，請覆寫 `GetState` 方法，以傳回 VFW 時無法提示的值， \_ \_ \_ (請參閱 [傳遞範例](delivering-samples.md)) 。 例如：


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




