---
title: 'MPTHREAT_INFO 結構 (MpClient .h) '
description: 包含威脅的相關資訊。
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO 結構舊版 Windows 環境功能
- PMPTHREAT_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466656"
---
# <a name="mpthreat_info-structure"></a>MPTHREAT \_ 資訊結構

包含威脅的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**ThreatID**
</dt> <dd>

類型： **MPTHREAT \_ 識別碼**

</dd> <dd>

威脅識別碼。 設定用來識別防毒軟體相關威脅的位位。

</dd> <dt>

**DetectionID**
</dt> <dd>

類型： **GUID**

</dd> <dd>

偵測識別碼。

</dd> <dt>

**名稱**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

威脅名稱。

</dd> <dt>

**ThreatType**
</dt> <dd>

類型： **[ **MPTHREAT \_ 類型**](mpthreat-type.md)**

</dd> <dd>

威脅類型。 用來區分不同的威脅類型，例如已知的不良、不明或已知良好。 請參閱 [**MPTHREAT \_ 類型**](mpthreat-type.md)。

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

類型： **[ **MPTHREAT \_ 嚴重性**](mpthreat-severity.md)**

</dd> <dd>

威脅重要性。 請參閱 [**MPTHREAT \_ 嚴重性**](mpthreat-severity.md)。

</dd> <dt>

**ThreatCategory**
</dt> <dd>

類型： **[ **MPTHREAT \_ 類別**](mpthreat-category.md)**

</dd> <dd>

威脅類別，例如特洛伊程式或 keylogger。 請參閱 [**MPTHREAT \_ 類別**](mpthreat-category.md)。

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

威脅簡短描述識別碼。

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

威脅建議描述識別碼。

</dd> <dt>

**ThreatStatus**
</dt> <dd>

類型： **[ **MPTHREAT \_ 狀態**](mpthreat-status.md)**

</dd> <dd>

威脅狀態，例如偵測、清除或隔離。 請參閱 [**MPTHREAT \_ 狀態**](mpthreat-status.md)。

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

**SuggestedActionArray** 中的建議動作計數。

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

類型： **[**MPTHREAT \_ 動作**](mpthreat-action.md) \[ MP 的 \_ 最大 \_ 建議\]**

</dd> <dd>

建議動作的陣列。 請參閱 [**MPTHREAT \_ 動作**](mpthreat-action.md)。

</dd> <dt>

**ResourceCount**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

**ResourceList** 中的資源計數。

</dd> <dt>

**ResourceList**
</dt> <dd>

類型： **PMPRESOURCE \_ INFO \** _

</dd> <dd>

已識別威脅的資源清單。 請參閱 [_ *MPRESOURCE \_ 資訊* *](mpresource-info.md)。

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

上次變更威脅狀態的時間。

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

類型： **HRESULT**

</dd> <dd>

與威脅狀態相關聯的狀態碼。

</dd> <dt>

**ThreatDetection**
</dt> <dd>

類型： **[ **MPTHREAT \_ 偵測**](mpthreat-detection.md)**

</dd> <dd>

威脅偵測類型，例如具體、可疑或泛型。 請參閱 [**MPTHREAT \_ 偵測**](mpthreat-detection.md)。

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

類型： **GUID**

</dd> <dd>

隔離 guid。

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

類型： **[ **MPEXECUTION \_ 狀態**](mpexecution-status.md)**

</dd> <dd>

威脅的執行狀態，例如「未知」、「已封鎖」或「作用中」。 請參閱 [**MPEXECUTION \_ 狀態**](mpexecution-status.md)。

</dd> <dt>

**資料**
</dt> <dd>

額外資訊。 適當結構的指標取決於 **ThreatType** 的值。

<dl> <dt>

**pKnownBad**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPTHREAT INFOEX**

</dd> <dd>

當 **ThreatType**  ==  **MPTHREAT \_ 類型 \_ KNOWNBAD** 時。 請參閱 [**MPTHREAT \_ INFOEX \_ 未使用**](mpthreat-infoex-unused.md)。

</dd> <dt>

**pBehavior**
</dt> <dd>

類型： **PMPTHREAT \_ INFOEX \_ 行為**

</dd> <dd>

**ThreatType**  ==  **MPTHREAT \_ 類型 \_ 行為** 時。 請參閱 [**MPTHREAT \_ INFOEX \_ 行為**](mpthreat-infoex-behavior.md)。

</dd> <dt>

**pUnknown**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPTHREAT INFOEX**

</dd> <dd>

當 **ThreatType**  ==  **MPTHREAT \_ 類型 \_ 未知** 時。 請參閱 [**MPTHREAT \_ INFOEX \_ 未使用**](mpthreat-infoex-unused.md)。

</dd> <dt>

**pKnownGood**
</dt> <dd>

類型： **\_ \_ 未使用的 PMPTHREAT INFOEX**

</dd> <dd>

當 **ThreatType** = = MPTHREAT \_ 類型 \_ KNOWNGOOD 時。 請參閱 [**MPTHREAT \_ INFOEX \_ 未使用**](mpthreat-infoex-unused.md)。

</dd> <dt>

**pNis**
</dt> <dd>

類型： **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

當 **ThreatType**  ==  **MPTHREAT \_ 類型 \_ NIS** 時。 請參閱 [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)。

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

類型： **[ **MPDETECTION \_ 狀態**](mpdetection-state.md)**

</dd> <dd>

偵測的目前狀態。 請參閱 [**MPDETECTION \_ 狀態**](mpdetection-state.md)。

</dd> <dt>

**DetectionUser**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

與偵測相關聯的使用者，格式為 "domain/user"。

</dd> <dt>

**DetectionSource**
</dt> <dd>

類型： **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

偵測的來源。 請參閱 [**MPSOURCE**](mpsource.md)。

</dd> <dt>

**ProcessName**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

與偵測相關聯的處理常式名稱。

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

類型： **[ **MPDETECTION \_ 來源**](mpdetection-origin.md)**

</dd> <dd>

偵測的來源，例如本機或網路。 請參閱 [**MPDETECTION \_ 來源**](mpdetection-origin.md)。

</dd> <dt>

**reserved1**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

關於偵測的保留中繼資料。

</dd> <dt>

**DetectionTime**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

初始偵測的時間。

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

類型： **[ **MPEXECUTION \_ 狀態**](mpexecution-status.md)**

</dd> <dd>

補救之前的執行狀態。 請參閱 [**MPEXECUTION \_ 狀態**](mpexecution-status.md)。

</dd> <dt>

**RemediationTime**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

發生補救的時間。

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

類型： **[ **MPEXECUTION \_ 狀態**](mpexecution-status.md)**

</dd> <dd>

補救後的執行狀態。 請參閱 [**MPEXECUTION \_ 狀態**](mpexecution-status.md)。

</dd> <dt>

**CriticalFailure**
</dt> <dd>

類型： **BOOL**

</dd> <dd>

如果補救失敗是嚴重的，則為 True。

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

補救失敗的原因不重要。 未來不一定會支援此功能。

</dd> <dt>

**RemediationUser**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

要求補救的使用者，格式為 "domain/user"。

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

**RemediationResourceList** 中的資源計數。

</dd> <dt>

**RemediationResourceList**
</dt> <dd>

類型： **PMPRESOURCE \_ INFO \[ RemediationResourceCount \]**

</dd> <dd>

修復期間失敗的資源清單。 請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。

</dd> <dt>

**FailureResolved**
</dt> <dd>

類型： **BOOL**

</dd> <dd>

如果已解決補救失敗，則為 True。 這會將 bucket 移至完成或執行其他動作。

</dd> <dt>

**ResolvedReason**
</dt> <dd>

類型： **[ **MPRESOLVED \_ 原因**](mpresolved-reason.md)**

</dd> <dd>

解決補救失敗的原因。 這是偵測的移動原因無法執行其他動作或已完成。 請參閱 [**MPRESOLVED \_ 原因**](mpresolved-reason.md)。

</dd> <dt>

**AdditionalActions**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

需要額外的動作。

</dd> <dt>

**ResolvedActions**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

已執行的任何其他動作。

</dd> <dt>

**dwThreatStatusFlag**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

威脅偵測的額外資訊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**MPDETECTION \_ 來源**](mpdetection-origin.md)
</dt> <dt>

[**MPDETECTION \_ 狀態**](mpdetection-state.md)
</dt> <dt>

[**MPEXECUTION \_ 狀態**](mpexecution-status.md)
</dt> <dt>

[**MPRESOLVED \_ 原因**](mpresolved-reason.md)
</dt> <dt>

[**MPRESOURCE \_ 資訊**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**MPTHREAT \_ 動作**](mpthreat-action.md)
</dt> <dt>

[**MPTHREAT \_ 類別**](mpthreat-category.md)
</dt> <dt>

[**MPTHREAT \_ 偵測**](mpthreat-detection.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ 行為**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**\_ \_ 未使用的 MPTHREAT INFOEX**](mpthreat-infoex-unused.md)
</dt> <dt>

[**MPTHREAT \_ 嚴重性**](mpthreat-severity.md)
</dt> <dt>

[**MPTHREAT \_ 狀態**](mpthreat-status.md)
</dt> <dt>

[**MPTHREAT \_ 類型**](mpthreat-type.md)
</dt> </dl>

 

 





