---
title: 'MPSCAN_DATA 結構 (MpClient .h) '
description: 掃描傳遞給回呼的資料。
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA 結構舊版 Windows 環境功能
- PMPSCAN_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466941"
---
# <a name="mpscan_data-structure"></a>MPSCAN \_ 資料結構

掃描傳遞給回呼的資料。

此結構包含累計威脅和資源統計資料。 這些 stat 欄位一律有效。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**ScanType**
</dt> <dd>

類型： **[ **MPSCAN \_ 類型**](mpscan-type.md)**

</dd> <dd>

掃描類型。

</dd> <dt>

**ResourceInfo**
</dt> <dd>

類型： **PMPRESOURCE \_ 資訊**

</dd> <dd>

資源資訊。 請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。

</dd> <dt>

**ResourceStats**
</dt> <dd>

類型： **[ **MPRESOURCE \_ 統計** 資料](mpresource-stats.md)**

</dd> <dd>

與資源相關的累計統計資料。

</dd> <dt>

**ThreatStats**
</dt> <dd>

類型： **[ **MPTHREAT \_ 統計** 資料](mpthreat-stats.md)**

</dd> <dd>

成功完成掃描的威脅統計資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPRESOURCE \_ 資訊**](mpresource-info.md)
</dt> <dt>

[**MPRESOURCE \_ 統計資料**](mpresource-stats.md)
</dt> <dt>

[**MPSCAN \_ 類型**](mpscan-type.md)
</dt> <dt>

[**MPTHREAT \_ 統計資料**](mpthreat-stats.md)
</dt> </dl>

 

 





