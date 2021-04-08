---
title: 'MPSTATUS_INFO 結構 (MpClient .h) '
description: 惡意程式碼防護管理員的狀態資訊。
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO 結構舊版 Windows 環境功能
- PMPSTATUS_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685565"
---
# <a name="mpstatus_info-structure"></a>MPSTATUS \_ 資訊結構

惡意程式碼防護管理員的狀態資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**ProductStatus**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

整體產品狀態。 這是 [**MPSTATUS \_ 旗**](mpstatus-flag.md)標的位旗標組合。

</dd> <dt>

**LastQuickScan**
</dt> <dd>

類型： **[ **MPSCAN \_ 結果**](mpscan-result.md)**

</dd> <dd>

惡意程式碼防護管理員上次掃描的結果。 請參閱 [**MPSCAN \_ 結果**](mpscan-result.md)。

</dd> <dt>

**LastFullScan**
</dt> <dd>

類型： **[ **MPSCAN \_ 結果**](mpscan-result.md)**

</dd> <dd>

惡意程式碼防護管理員上次完整掃描的結果。 請參閱 [**MPSCAN \_ 結果**](mpscan-result.md)。

</dd> <dt>

**ThreatStats**
</dt> <dd>

類型： **[ **MPTHREAT \_ 統計** 資料](mpthreat-stats.md)**

</dd> <dd>

作用中的威脅統計資料。 請參閱 [**MPTHREAT \_ 統計**](mpthreat-stats.md)資料。

</dd> <dt>

**ThreatState**
</dt> <dd>

類型： **[**MPTHREAT \_ STATS \_ DATA**](mpthreat-stats-data.md) \[ MP \_ 威脅 \_ STAT \_ 最大 \_ 值 + 1\]**

</dd> <dd>

其他威脅統計資料，例如威脅數目。 請參閱 [**MPTHREAT \_ 統計 \_ 資料**](mpthreat-stats-data.md)。

</dd> <dt>

**元件**
</dt> <dd>

類型： **[**MPCOMPONENT \_ STATUS**](mpcomponent-status.md) \[ MPCOMPONENT int32.maxvalue \_ + 1\]**

</dd> <dd>

多個元件的狀態陣列。 使用 [**MPCOMPONENT \_ ID**](mpcomponent-id.md) 列舉中的值做為陣列中的索引。

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

UNC 中的產品到期時間戳記。 只有在已設定到期狀態時，這才有效。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPCOMPONENT \_ 識別碼**](mpcomponent-id.md)
</dt> <dt>

[**MPCOMPONENT \_ 狀態**](mpcomponent-status.md)
</dt> <dt>

[**MPSCAN \_ 結果**](mpscan-result.md)
</dt> <dt>

[**MPSTATUS \_ 旗標**](mpstatus-flag.md)
</dt> <dt>

[**MPTHREAT \_ 統計資料**](mpthreat-stats.md)
</dt> <dt>

[**MPTHREAT \_ 統計 \_ 資料**](mpthreat-stats-data.md)
</dt> </dl>

 

 





