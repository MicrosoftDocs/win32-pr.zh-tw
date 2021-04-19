---
description: 當播放速率變更時，會呼叫 ChangeRate 方法。
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: 'CSourceSeeking. ChangeRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975999"
---
# <a name="csourceseekingchangerate-method"></a>CSourceSeeking. ChangeRate 方法

`ChangeRate`當播放速率變更時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

[**CSourceSeeking：： SetRate**](csourceseeking-setrate.md)方法會呼叫這個方法，而衍生的類別必須在此方法中執行。 **SetRate** 方法會更新 [**CSourceSeeking：： m \_ dRateSeeking**](csourceseeking-m-drateseeking.md)成員變數，但不會驗證新值。 應一律拒絕零的速率。 小於零的速率表示會有負面的播放。 大部分的篩選不支援負數速率。

下列範例顯示可能的實作為：


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




