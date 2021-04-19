---
description: CheckCapabilities 方法會查詢資料流程是否已指定搜尋功能。 這個方法會實 IMediaSeeking：： CheckCapabilities 方法。
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: 'CSourceSeeking. CheckCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994209"
---
# <a name="csourceseekingcheckcapabilities-method"></a>CSourceSeeking. CheckCapabilities 方法

`CheckCapabilities`方法會查詢資料流程是否已指定搜尋功能。 這個方法會實 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCapabilities* 
</dt> <dd>

一或多個搜尋中搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 屬性的位元組合指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | 並非 *pCapabilities* 中的所有功能都存在。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>      | *PCapabilities* 中的所有功能都存在。<br/>            |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數。<br/>                                  |



 

## <a name="remarks"></a>備註

如同實，這個方法會根據 [**CSourceSeeking：： m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md)成員變數來檢查 *\* pCapabilities* 的值。 但是，它不會將 *\* pCapabilities* 設定為等於 **m \_ dwSeekingCaps**，如 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities)方法所述。 此外，如果沒有任何指定的功能可供使用，則該方法不會傳回 E \_ 失敗。 更完整的實施方式如下：


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
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

 

 




