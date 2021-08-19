---
title: 'MPCLEAN_DATA 結構 (MpClient .h) '
description: 傳遞給清除回呼函數的通知資料。
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA 結構舊版 Windows 環境功能
- PMPCLEAN_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece20324fc06fb68a813b374a698b2e27264068c9051bb2a5fff328c7ad328d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476336"
---
# <a name="mpclean_data-structure"></a>MPCLEAN \_ 資料結構

傳遞給清除回呼函數的通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**ThreatID**
</dt> <dd>

類型： **MPTHREAT \_ 識別碼**

</dd> <dd>

**MPNOTIFY \_ clean \_ 威脅 \_** 的威脅識別碼開始 / **MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功** / **MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗** 事件。 設定用來識別防毒軟體相關威脅的位位。

</dd> <dt>

**ThreatAction**
</dt> <dd>

類型： **[ **MPTHREAT \_ 動作**](mpthreat-action.md)**

</dd> <dd>

**MPNOTIFY \_ clean \_ 威脅 \_** 的威脅動作開始 / **MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功** / **MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗** 事件。 請參閱 [**MPTHREAT \_ 動作**](mpthreat-action.md)。

</dd> <dt>

**dwStatus**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

與所採取動作相關聯的其他狀態或動作。 這是 [**MPSTATUS \_ 旗**](mpstatus-flag.md)標的位旗標組合。

</dd> <dt>

**ResourceInfo**
</dt> <dd>

類型： **PMPRESOURCE \_ 資訊**

</dd> <dd>

**MPNOTIFY \_ clean \_ 威脅 \_** 的資源資訊開始 / **MPNOTIFY \_ 乾淨 \_ 威脅 \_ 成功** / **MPNOTIFY \_ 清除 \_ 威脅 \_ 失敗** 的事件。 請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPRESOURCE \_ 資訊**](mpresource-info.md)
</dt> <dt>

[**MPSTATUS \_ 旗標**](mpstatus-flag.md)
</dt> <dt>

[**MPTHREAT \_ 動作**](mpthreat-action.md)
</dt> </dl>

 

 





