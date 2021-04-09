---
description: KsQueryMediums 方法會抓取釘選所支援的媒體。
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'IKsPin：： KsQueryMediums 方法 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687964"
---
# <a name="ikspinksquerymediums-method"></a>IKsPin：： KsQueryMediums 方法

方法會抓取 `KsQueryMediums` pin 所支援的媒體。

## <a name="syntax"></a>語法


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppmi* \[擴展\]
</dt> <dd>

指向 [**KSMULTIPLE \_ 專案**](ksmultiple-item.md) 結構之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法會傳回工作配置的 [**KSMULTIPLE \_ 專案**](ksmultiple-item.md) 結構，後面接著零或多個 [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) 結構。 **KSMULTIPLE \_ 專案** 結構的 **Count** 成員會指定 **REGPINMEDIUM** 結構的數目。 每個 **REGPINMEDIUM** 結構都會定義釘選所支援的媒體。

呼叫端必須使用 **CoTaskMemFree** 函數釋放傳回的結構。

您必須在 Ksproxy 之前包含 Ks。

## <a name="examples"></a>範例

下列 helper 函式會嘗試比對指定媒體的釘選。


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Ksproxy。h</dt> </dl>    |
| 程式庫<br/>                  | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IKsPin 介面**](ikspin.md)
</dt> <dt>

[WDM 類別驅動程式篩選](wdm-class-driver-filters.md)
</dt> </dl>

 

 




