---
title: 'MPTHREAT_LOCALIZED_INFO 結構 (MpClient .h) '
description: 威脅的當地語系化資訊。
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO 結構舊版 Windows 環境功能
- PMPTHREAT_LOCALIZED_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff28c77c60421fcaabe31580400ad87823ad3edf3536d96ba3ba5eec177ad94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555948"
---
# <a name="mpthreat_localized_info-structure"></a>MPTHREAT \_ 當地語系化的 \_ 資訊結構

威脅的當地語系化資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**ThreatID**
</dt> <dd>

類型： **MPTHREAT \_ 識別碼**

</dd> <dd>

威脅識別碼。 設定用來識別防毒軟體相關威脅的位位。

</dd> <dt>

**CategoryName**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

威脅分類，例如特洛伊程式或 keylogger。

</dd> <dt>

**CategoryDescription**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

威脅類別目錄的描述。

</dd> <dt>

**SeverityName**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

威脅嚴重性層級，例如「嚴重」或「適中」。

</dd> <dt>

**SeverityDescription**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

威脅嚴重性層級的描述。

</dd> <dt>

**ShortDescription**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

威脅的簡短描述。

</dd> <dt>

**DefaultActionName;**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

引擎建議的預設動作名稱，例如移除或隔離。

</dd> <dt>

**建議**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

特定威脅的建議。

</dd> <dt>

**ThreatUrl**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

包含威脅相關資訊之網頁的 URL。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





