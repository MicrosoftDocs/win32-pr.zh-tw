---
description: IMFWorkQueueServices：： BeginUnregisterTopologyWorkQueuesWithMMCSS 方法的可遠端執行版本。
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: 'RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4fe3fe7f7f82e426eabe2ffd6e0aadb19879ceef713c4a66c44ee4cfceea50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724448"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a>RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS

[**IMFWorkQueueServices：： BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss)方法的可遠端執行版本。

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>備註

應用程式無法直接呼叫這個方法，而物件也不會執行此方法。 方法不會出現在介面的 vtable 中。 如果跨進程界限呼叫 [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。

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

 

 




