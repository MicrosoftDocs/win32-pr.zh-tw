---
description: IMFWorkQueueServices：： EndRegisterPlatformWorkQueueWithMMCSS 方法的可遠端執行版本。
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: 'RemoteEndRegisterPlatformWorkQueueWithMMCSS (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14414d9fe6d093ee797d8c9e4879bd54cf89b3dbfc60b526ae8556f78ecc34e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878295"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a>RemoteEndRegisterPlatformWorkQueueWithMMCSS

[**IMFWorkQueueServices：： EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss)方法的可遠端執行版本。

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a>備註

應用程式無法直接呼叫這個方法，而物件也不會執行此方法。 方法不會出現在介面的 vtable 中。 如果跨進程界限呼叫 [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mfuuid .lib</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




