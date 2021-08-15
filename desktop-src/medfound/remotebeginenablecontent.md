---
description: IMFContentProtectionManager：： BeginEnableContent 方法的可遠端執行版本。
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: 'RemoteBeginEnableContent (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a39f11fbecaab436a6db82ccb2880a56a783ef1ec43f0db6b408bd870917cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238719"
---
# <a name="remotebeginenablecontent"></a>RemoteBeginEnableContent

[**IMFContentProtectionManager：： BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)方法的可遠端執行版本。

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>備註

應用程式無法直接呼叫這個方法，而物件也不會執行此方法。 方法不會出現在介面的 vtable 中。 如果跨進程界限呼叫 [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mfuuid .lib</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




