---
description: 在 IMFMediaSession：： SetTopology 方法以非同步方式完成之後引發。 媒體會話會在將拓撲解析成完整拓撲之後引發此事件，並將拓撲排入佇列以供播放。
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: 'MESessionTopologySet 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943796"
---
# <a name="mesessiontopologyset-event"></a>MESessionTopologySet 事件

在 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法以非同步方式完成之後引發。 媒體會話會在將拓撲解析成完整拓撲之後引發此事件，並將拓撲排入佇列以供播放。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                                              |
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




