---
title: 'MPENDOFLIFE_DATA 結構 (MpClient .h) '
description: '\ 0034;生命週期結束 \ 0034;通知資料。'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA 結構舊版 Windows 環境功能
- PMPENDOFLIFE_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532ee5f80e76de49c2c20bb01958e95fc13603b8f4b65666639834c5cad0fa72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476280"
---
# <a name="mpendoflife_data-structure"></a>MPENDOFLIFE \_ 資料結構

「生命週期結束」通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**ftSignatureExpiry**
</dt> <dd>

類型： **FILETIME**

</dd> <dd>

簽章到期的時間。

</dd> <dt>

**ftPlatformExpiry**
</dt> <dd>

類型： **FILETIME**

</dd> <dd>

平臺到期的時間。

</dd> <dt>

**fAdminControlled**
</dt> <dd>

類型： **BOOL**

</dd> <dd>

如果系統管理員控制用來顯示通知的原則，則為 True。 如果設定，則會告訴 UI 不要顯示 EOL 通知。

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

類型： **BOOL**

</dd> <dd>

如果「生命週期結束」暫止或超過此值，則為 True。 如果為 false，則 UI 和用戶端可以清除任何 EOL 相關狀態。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





