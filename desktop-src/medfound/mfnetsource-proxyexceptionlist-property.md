---
description: 指定可接受來自用戶端應用程式的連線，而不使用 proxy 伺服器的媒體伺服器清單（以分號分隔）。
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: 'MFNETSOURCE_PROXYEXCEPTIONLIST 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977899"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a>MFNETSOURCE \_ PROXYEXCEPTIONLIST 屬性

指定可接受來自用戶端應用程式的連線，而不使用 proxy 伺服器的媒體伺服器清單（以分號分隔）。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

寬字元字串 (**WCHAR** \*) 

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PROXYEXCEPTIONLIST** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。 若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。 Proxy 定位器不會針對這些位址執行 proxy 偵測。

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

 

 




