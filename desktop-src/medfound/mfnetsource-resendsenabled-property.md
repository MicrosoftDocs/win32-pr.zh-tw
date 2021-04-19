---
description: 指定網路來源是否傳送 UDP 重新傳送要求以回應遺失的封包。
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: 'MFNETSOURCE_RESENDSENABLED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979757"
---
# <a name="mfnetsource_resendsenabled-property"></a>MFNETSOURCE \_ RESENDSENABLED 屬性

指定網路來源是否傳送 UDP 重新傳送要求以回應遺失的封包。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

布林 (**LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ RESENDSENABLED** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

這個屬性的預設值為 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端記錄](client-logging.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




