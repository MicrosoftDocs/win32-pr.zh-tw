---
description: '\#網路來源用於記錄的 &0034; cs (使用者代理程式) &0034; 欄位的第二部分值 \# 。'
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: 'MFNETSOURCE_PLAYERUSERAGENT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b431780345c8b297bf154813a9713b5b158ecc99cc4384294ee983b8066ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243420"
---
# <a name="mfnetsource_playeruseragent-property"></a>MFNETSOURCE \_ PLAYERUSERAGENT 屬性

網路來源用於記錄的 [cs (使用者代理程式) ] 欄位的第二個部分值。 應用程式可以將此屬性設定為任何字串值。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

寬字元字串 (**WCHAR** \*) 

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PLAYERUSERAGENT** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端記錄](client-logging.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> <dt>

[**MFNETSOURCE \_ BROWSERUSERAGENT**](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




