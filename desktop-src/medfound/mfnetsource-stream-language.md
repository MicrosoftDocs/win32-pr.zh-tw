---
description: 儲存在 Accept-Language 標頭中傳送的字串。
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: 'MFNETSOURCE_STREAM_LANGUAGE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c44b6f55fd2f5652a41d9aa5eed76e60e73152343d2baf6c577be56bc462c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344538"
---
# <a name="mfnetsource_stream_language-property"></a>MFNETSOURCE \_ 資料流程 \_ 語言屬性

儲存在 Accept-Language 標頭中傳送的字串。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**WCHAR\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>備註

MFNETSOURCE \_ 資料流程 \_ 語言常數會定義屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。 若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

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

 

 




