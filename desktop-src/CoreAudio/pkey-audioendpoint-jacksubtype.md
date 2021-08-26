---
description: PKEY \_ AudioEndpoint \_ JackSubType 屬性包含音訊端點裝置的輸出類別 GUID。
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: 'PKEY_AudioEndpoint_JackSubType (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95ca24d48a35299144f36d052ceea2e2d0d12c56fbc03b58a993fd95772c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053728"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

**PKEY \_ AudioEndpoint \_ JackSubType** 屬性包含音訊端點裝置的輸出類別 GUID。 標頭檔 Ksmedia 會定義 Guid;每個 GUID 都會指定連接的類型。 這些 Guid 也有相關聯的釘選類別。 例如，標頭檔 Ksmedia 會針對顯示埠定義 GUID **KSNODETYPE \_ DISPLAYPORT \_ 介面** ，此介面會連接到 GUID **PINNAME \_ DISPLAYPORT \_ OUT** 所定義的 KS pin。

如需詳細資訊，請參閱 Windows DDK 檔中的 pin 分類屬性描述。

**PROPVARIANT** 結構的 **vt** 成員會設定為 **vt \_ LPWSTR**。

**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 終止的寬字元字串，其中包含分類 GUID。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 




