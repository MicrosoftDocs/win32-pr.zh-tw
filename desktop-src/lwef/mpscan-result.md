---
title: 'MPSCAN_RESULT 結構 (MpClient .h) '
description: 掃描的結果。
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT 結構舊版 Windows 環境功能
- PMPSCAN_RESULT 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187315"
---
# <a name="mpscan_result-structure"></a>MPSCAN \_ 結果結構

掃描的結果。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a>成員

<dl> <dt>

**ScanType**
</dt> <dd>

類型： **[ **MPSCAN \_ 類型**](mpscan-type.md)**

</dd> <dd>

掃描類型。 請參閱 [**MPSCAN \_ 類型**](mpscan-type.md)。

</dd> <dt>

**來源**
</dt> <dd>

類型： **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

掃描來源，例如使用者或系統起始。 請參閱 [**MPSOURCE**](mpsource.md)。

</dd> <dt>

**ScanGuid**
</dt> <dd>

類型： **GUID**

</dd> <dd>

掃描識別碼。

</dd> <dt>

**StartTime**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

掃描開始時間。

</dd> <dt>

**EndTime**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

掃描結束時間。

</dd> <dt>

**ThreatStats**
</dt> <dd>

類型： **[ **MPTHREAT \_ 統計** 資料](mpthreat-stats.md)**

</dd> <dd>

威脅相關的統計資料。 請參閱 [**MPTHREAT \_ 統計**](mpthreat-stats.md)資料。

</dd> <dt>

**ResourceStats**
</dt> <dd>

類型： **[ **MPRESOURCE \_ 統計** 資料](mpresource-stats.md)**

</dd> <dd>

與資源相關的統計資料。 請參閱 [**MPRESOURCE \_ 統計**](mpresource-stats.md)資料。

</dd> <dt>

**SignatureVersion**
</dt> <dd>

類型： **ULONGLONG**

</dd> <dd>

用於掃描的簽章版本。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPRESOURCE \_ 統計資料**](mpresource-stats.md)
</dt> <dt>

[**MPSCAN \_ 類型**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**MPTHREAT \_ 統計資料**](mpthreat-stats.md)
</dt> </dl>

 

 





