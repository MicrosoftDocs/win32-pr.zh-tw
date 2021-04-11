---
description: IMFMediaEventGenerator：： EndGetEvent 方法的可遠端執行版本。
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: 'RemoteEndGetEvent (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3c4a5fe87dddf5fc1d256d61d8c863c2f1d9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691619"
---
# <a name="remoteendgetevent"></a>RemoteEndGetEvent

[**IMFMediaEventGenerator：： EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent)方法的可遠端執行版本。

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a>備註

應用程式無法直接呼叫這個方法，而物件也不會執行此方法。 方法不會出現在介面的 vtable 中。 如果跨進程界限呼叫 [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mfuuid .lib</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




