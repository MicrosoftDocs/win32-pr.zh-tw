---
description: IMFSourceResolver：： BeginCreateObjectFromByteStream 方法的可遠端執行版本。
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: 'RemoteBeginCreateObjectFromByteStream (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ac0365da83ec3f6bedc3ab45b9aef1458ed04c97ccdbfc1e00484824de47e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268978"
---
# <a name="remotebegincreateobjectfrombytestream"></a>RemoteBeginCreateObjectFromByteStream

[**IMFSourceResolver：： BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)方法的可遠端執行版本。

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>備註

應用程式無法直接呼叫這個方法，而物件也不會執行此方法。 方法不會出現在介面的 vtable 中。 如果跨進程界限呼叫 [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mfuuid .lib</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




