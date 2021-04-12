---
description: 指定 proxy 伺服器的埠號碼。
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: 'MFNETSOURCE_PROXYPORT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191878"
---
# <a name="mfnetsource_proxyport-property"></a>MFNETSOURCE \_ PROXYPORT 屬性

指定 proxy 伺服器的埠號碼。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**DWORD** (儲存為 **LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PROXYPORT** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。 若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。 如果未針對 HTTP 設定此屬性，則 proxy 定位器預設會使用80的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> <dt>

[網路來源的 Proxy 支援](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




