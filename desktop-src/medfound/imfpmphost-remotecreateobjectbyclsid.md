---
description: IMFPMPHost：： CreateObjectByCLSID 方法的可遠端執行版本。
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: 'RemoteCreateObjectByCLSID (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2274eb66c2dcd3452e6c3fbad1ab300ba705333a78e8eaa761eab70c54104ca0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061188"
---
# <a name="remotecreateobjectbyclsid"></a>RemoteCreateObjectByCLSID

[**IMFPMPHost：： CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid)方法的可遠端執行版本。

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a>備註

應用程式無法直接呼叫這個方法，而物件也不會執行此方法。 方法不會出現在介面的 vtable 中。 如果跨進程界限呼叫 [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mfuuid .lib</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[PMP 媒體會話](pmp-media-session.md)
</dt> <dt>

[受保護的媒體路徑](protected-media-path.md)
</dt> </dl>

 

 




