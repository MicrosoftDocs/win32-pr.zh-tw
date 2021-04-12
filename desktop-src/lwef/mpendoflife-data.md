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
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104850"
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
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





