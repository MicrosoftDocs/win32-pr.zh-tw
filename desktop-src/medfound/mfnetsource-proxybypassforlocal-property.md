---
description: 指定 proxy 定位器是否應針對本機位址使用 proxy 伺服器。
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: 'MFNETSOURCE_PROXYBYPASSFORLOCAL 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1de60371ac71e570b9c11abcbc255e20efe1793884ebb0746834d32a34353006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954788"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>MFNETSOURCE \_ PROXYBYPASSFORLOCAL 屬性

指定 proxy 定位器是否應針對本機位址使用 proxy 伺服器。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

布林 (**LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。 若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。 如果 proxy 伺服器要用於本機位址，此值必須設定為0。否則，非零值會設定預設 proxy 定位器，以略過本機位址的 proxy 伺服器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> <dt>

[網路來源的 Proxy 支援](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




