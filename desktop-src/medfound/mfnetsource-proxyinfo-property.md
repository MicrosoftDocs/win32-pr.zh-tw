---
description: 儲存網路來源所使用之 proxy 伺服器的主機名稱和埠。
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: 'MFNETSOURCE_PROXYINFO 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996805"
---
# <a name="mfnetsource_proxyinfo-property"></a>MFNETSOURCE \_ proxyinfo.conf 屬性

儲存網路來源所使用之 proxy 伺服器的主機名稱和埠。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

寬字元字串 (**WCHAR** \*) 

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ proxyinfo.conf** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

這是唯讀的屬性。 若要從網路來源取得屬性值，請呼叫 **IPropertyStore：： GetValue** ，並在 *金鑰* 參數中傳遞 **PROPERTYKEY** 結構。 **PROPERTYKEY** 的 **fmtid** 成員必須設定為屬性 GUID。

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

 

 




