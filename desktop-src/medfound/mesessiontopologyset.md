---
description: 在 IMFMediaSession：： SetTopology 方法以非同步方式完成之後引發。 媒體會話會在將拓撲解析成完整拓撲之後引發此事件，並將拓撲排入佇列以供播放。
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: 'MESessionTopologySet 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2b5454309855ff472c633388cddabe0c12fab09e2ae462aacd2de49c3c9bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957398"
---
# <a name="mesessiontopologyset-event"></a>MESessionTopologySet 事件

在 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法以非同步方式完成之後引發。 媒體會話會在將拓撲解析成完整拓撲之後引發此事件，並將拓撲排入佇列以供播放。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | 描述                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ 空白<br/>   | 沒有事件資料。<br/> <br/>                                                                    |
| VT \_ 不明<br/> | 完整拓撲之 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面的指標。<br/> <br/> |



## <a name="examples"></a>範例

下列範例會從 MESessionTopologySet 事件中取出 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 指標。


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




