---
title: 'MPCALLBACK_DATA 結構 (MpClient .h) '
description: 傳遞至回呼函數的資料。
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA 結構舊版 Windows 環境功能
- PMPCALLBACK_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094516"
---
# <a name="mpcallback_data-structure"></a>MPCALLBACK \_ 資料結構

傳遞至回呼函數的資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**通知**
</dt> <dd>

類型： **[ **MPNOTIFY**](mpnotify.md)**

</dd> <dd>

將通知變更為 [報表]。

</dd> <dt>

**hResult**
</dt> <dd>

類型： **HRESULT**

</dd> <dd>

如果發生內部失敗，則為錯誤碼。

</dd> <dt>

**時間 戳**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

目前的時間戳記。

</dd> <dt>

**型別**
</dt> <dd>

類型： **[ **MPCALLBACK \_ 類型**](mpcallback-type.md)**

</dd> <dd>

回呼特殊資料類型。

</dd> <dt>

**資料**
</dt> <dd>

回呼特殊資料。 適當結構的指標取決於 **類型** 的值。

<dl> <dt>

**pStatusData**
</dt> <dd>

類型： **PMPSTATUS \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ 狀態** 時。 請參閱 [**MPSTATUS \_ 資料**](mpstatus-data.md)。

</dd> <dt>

**pScanData**
</dt> <dd>

類型： **PMPSCAN \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ SCAN** 時。 請參閱 [**MPSCAN \_ 資料**](mpscan-data.md)。

</dd> <dt>

**pCleanData**
</dt> <dd>

類型： **PMPCLEAN \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ CLEAN** 時。 請參閱 [**MPCLEAN \_ 資料**](mpclean-data.md)。

</dd> <dt>

**pPrecheckData**
</dt> <dd>

類型： **PMPCLEAN 前置檢查 \_ \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_** 前置檢查時。 請參閱 MPCLEAN 前置檢查 [**\_ \_ 資料**](mpclean-precheck-data.md)。

</dd> <dt>

**pThreatData**
</dt> <dd>

類型： **PMPTHREAT \_ 資料**

</dd> <dd>

當 **類型**  ==  **MPCALLBACK \_ 威脅** 時。 請參閱 [**MPTHREAT \_ 資料**](mpthreat-data.md)。

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

類型： **PMPSIGUPDATE \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ SIGUPDATE** 時。 請參閱 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md)。

</dd> <dt>

**pSampleData**
</dt> <dd>

類型： **PMPSAMPLE \_ 資料**

</dd> <dd>

當 **類型**  ==  **MPCALLBACK \_ 範例** 時。 請參閱 [**MPSAMPLE \_ 資料**](mpsample-data.md)。

</dd> <dt>

**pReservedData**
</dt> <dd>

類型： **PMPRESERVED \_ 資料**

</dd> <dd>

當 **類型**  ==  **MPCALLBACK \_ 保留** 時。 請參閱 [**MPRESERVED \_ 資料**](mpreserved-data.md)。

</dd> <dt>

**pConfigurationData**
</dt> <dd>

類型： **PMPCONFIGURATION \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ 設定 \_ 通知** 時。 請參閱 [**MPCONFIGURATION \_ 資料**](mpconfiguration-data.md)。

</dd> <dt>

**pFastPathData**
</dt> <dd>

類型： **PMPFASTPATH \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ FASTPATH** 時。 請參閱 [**MPFASTPATH \_ 資料**](mpfastpath-data.md)。

</dd> <dt>

**pExpirationData**
</dt> <dd>

類型： **PMPEXPIRATION \_ 資料**

</dd> <dd>

當 **類型**  ==  **MPCALLBACK \_ 產品 \_ 到期** 時。 請參閱 [**MPEXPIRATION \_ 資料**](mpexpiration-data.md)。

</dd> <dt>

**pNISPrivateData**
</dt> <dd>

類型： **PMPNIS \_ 私用 \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ NIS \_ 私** 用時。 請參閱 [**MPNIS \_ 私用 \_ 資料**](mpnis-private-data.md)。

</dd> <dt>

**pHealthData**
</dt> <dd>

類型： **PMPHEALTH \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ HEALTH** 時。 請參閱 [**MPHEALTH \_ 資料**](mphealth-data.md)。

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

類型： **PMPENDOFLIFE \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ ENDOFLIFE** 時。 請參閱 [**MPENDOFLIFE \_ 資料**](mpendoflife-data.md)。

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

類型： **PMPMALWARETOAST \_ 資料**

</dd> <dd>

當 **輸入**  ==  **MPCALLBACK \_ MALWARETOAST** 時。 請參閱 [**MPMALWARETOAST \_ 資料**](mpmalwaretoast-data.md)。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPCALLBACK \_ 類型**](mpcallback-type.md)
</dt> <dt>

[**MPCLEAN \_ 資料**](mpclean-data.md)
</dt> <dt>

[**MPCLEAN 前置檢查 \_ \_ 資料**](mpclean-precheck-data.md)
</dt> <dt>

[**MPCONFIGURATION \_ 資料**](mpconfiguration-data.md)
</dt> <dt>

[**MPENDOFLIFE \_ 資料**](mpendoflife-data.md)
</dt> <dt>

[**MPEXPIRATION \_ 資料**](mpexpiration-data.md)
</dt> <dt>

[**MPFASTPATH \_ 資料**](mpfastpath-data.md)
</dt> <dt>

[**MPHEALTH \_ 資料**](mphealth-data.md)
</dt> <dt>

[**MPMALWARETOAST \_ 資料**](mpmalwaretoast-data.md)
</dt> <dt>

[**MPNIS \_ 私用 \_ 資料**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**MPRESERVED \_ 資料**](mpreserved-data.md)
</dt> <dt>

[**MPSAMPLE \_ 資料**](mpsample-data.md)
</dt> <dt>

[**MPSCAN \_ 資料**](mpscan-data.md)
</dt> <dt>

[**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md)
</dt> <dt>

[**MPSTATUS \_ 資料**](mpstatus-data.md)
</dt> <dt>

[**MPTHREAT \_ 資料**](mpthreat-data.md)
</dt> </dl>

 

 





