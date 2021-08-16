---
description: 伺服器用來識別用戶端的唯一識別碼。
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: 'MFNETSOURCE_CLIENTGUID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9585f5ac9cd69148272cb986746f6849aad4c3aa048b46baf2f75aeaba77c092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738987"
---
# <a name="mfnetsource_clientguid-property"></a>MFNETSOURCE \_ CLIENTGUID 屬性

伺服器用來識別用戶端的唯一識別碼。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**GUID**

VT \_ CLSID

**puuid**



## <a name="remarks"></a>備註

**MFNETSOURCE \_ CLIENTGUID** 常數會定義屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。 若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

如果未設定或設定為 **GUID \_ Null**，Microsoft 媒體基礎會產生每個會話的匿名 GUID，以確保使用者的隱私權。

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

 

 




