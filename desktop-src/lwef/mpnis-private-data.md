---
title: 'MPNIS_PRI加值稅E_DATA 結構 (MpClient .h) '
description: 私人 NIS 通知。
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRI加值稅E_DATA 結構舊版 Windows 環境功能
- PMPNIS_PRI加值稅E_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685567"
---
# <a name="mpnis_private_data-structure"></a>MPNIS \_ 私用 \_ 資料結構

私人 NIS 通知。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**dwNotificationType**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

通知的類型。

</dd> <dt>

**cbDataSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

保留資料的大小（以位元組為單位）。

</dd> <dt>

**pbData**
</dt> <dd>

類型：**位元組 \***

</dd> <dd>

保留資料的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





