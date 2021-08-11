---
description: 儲存實 IMFSSLCertificateManager 介面之類別的 IUnknown 指標。
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: 'MFNETSOURCE_SSLCERTIFICATE_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f853ae3fe44a9c4508386df4096e4adac36f3cec8a8cf199eb91cb87e1fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243292"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER 屬性

儲存實 [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager)介面之類別的 **IUnknown** 指標。 用戶端實作此實作會提供在伺服器要求用戶端 SSL 憑證時取得用戶端 SSL 憑證的方法。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**IUnknown 指標**

VT \_ 不明

**punkVal**



## <a name="remarks"></a>備註

**MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER** 常數會定義屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。 若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




