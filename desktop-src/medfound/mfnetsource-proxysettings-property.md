---
description: 指定預設 proxy 定位器的設定。
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: 'MFNETSOURCE_PROXYSETTINGS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114593"
---
# <a name="mfnetsource_proxysettings-property"></a>MFNETSOURCE \_ PROXYSETTINGS 屬性

指定預設 proxy 定位器的設定。 這個屬性的值是 [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) 列舉的成員。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PROXYSETTINGS** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

在建立預設 proxy 定位器物件時，應用程式可以使用這個屬性來設定 proxy 定位器。 若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。

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

 

 




