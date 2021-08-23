---
title: 'MPTHREAT_STATS 結構 (MpClient .h) '
description: 威脅相關的統計資料。
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS 結構舊版 Windows 環境功能
- PMPTHREAT_STATS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7671b45dc09c8aca494ad270aa69fc386ef3d7c03d5144fdc3e89b4f657bb07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975938"
---
# <a name="mpthreat_stats-structure"></a>MPTHREAT \_ 統計結構

威脅相關的統計資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a>成員

<dl> <dt>

**ThreatCount**
</dt> <dd>

類型： **UINT**

</dd> <dd>

偵測到的威脅數目。

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

類型： **UINT**

</dd> <dd>

使用行為監視偵測到的威脅數目。

</dd> <dt>

**已保留**
</dt> <dd>

類型： **UINT \[ 4 \]**

</dd> <dd>

保留供日後使用的欄位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





