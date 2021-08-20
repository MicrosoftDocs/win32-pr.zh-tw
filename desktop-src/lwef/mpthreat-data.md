---
title: 'MPTHREAT_DATA 結構 (MpClient .h) '
description: 因為威脅偵測或修改而傳遞的通知資料。
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA 結構舊版 Windows 環境功能
- PMPTHREAT_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd6338a027e3b03971f357950bbc351acef0d3fcdca83b72130e0ea475164d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883228"
---
# <a name="mpthreat_data-structure"></a>MPTHREAT \_ 資料結構

因為威脅偵測或修改而傳遞的通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**ThreatID**
</dt> <dd>

類型： **MPTHREAT \_ 識別碼**

</dd> <dd>

威脅識別碼。 設定用來識別防毒軟體相關威脅的位位。

</dd> <dt>

**dwSessionID**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

與威脅相關聯的會話。 如果沒有會話特定資訊可供使用，則設定為-1。

</dd> <dt>

**ThreatAction**
</dt> <dd>

類型： **[ **MPTHREAT \_ 動作**](mpthreat-action.md)**

</dd> <dd>

已嘗試 **MPNOTIFY \_ 威脅 \_ 清除 \_ 成功** / **MPNOTIFY \_ 威脅 \_ 清除 \_ 失敗** 事件的威脅動作。

</dd> <dt>

**dwStatus**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

與所採取動作相關聯的其他狀態或動作。 這是 [**MPSTATUS \_ 旗**](mpstatus-flag.md)標的位旗標組合。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPSTATUS \_ 旗標**](mpstatus-flag.md)
</dt> <dt>

[**MPTHREAT \_ 動作**](mpthreat-action.md)
</dt> </dl>

 

 





