---
description: 開始位置變更時，會呼叫 ChangeStart 方法。
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: 'CSourceSeeking. ChangeStart 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987847"
---
# <a name="csourceseekingchangestart-method"></a>CSourceSeeking. ChangeStart 方法

`ChangeStart`開始位置變更時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

如果開始位置變更， [**CSourceSeeking：： SetPositions**](csourceseeking-setpositions.md) 方法就會呼叫這個方法。 這個方法是純虛擬的;衍生的類別必須加以執行。 搜尋作業之後，時間戳記應從零重新開機。 媒體時間應該會反映新的開始時間。 下列範例顯示可能的實作為：


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
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

 

 




