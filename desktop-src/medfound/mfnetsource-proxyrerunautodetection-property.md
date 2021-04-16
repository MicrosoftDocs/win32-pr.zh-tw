---
description: 指定預設 proxy 定位器是否應該強制 proxy 自動偵測。
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: 'MFNETSOURCE_PROXYRERUNAUTODETECTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512812"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a>MFNETSOURCE \_ PROXYRERUNAUTODETECTION 屬性

指定預設 proxy 定位器是否應該強制 proxy 自動偵測。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

布林 (**LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PROXYSETTINGS** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。 若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。 在自動偵測模式中，proxy 定位器會使用 WinInet proxy 偵測機制。 若要強制自動偵測，請將值設定為0。

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

 

 




