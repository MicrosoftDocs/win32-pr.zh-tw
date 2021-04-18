---
title: Win32_TSLicenseReport 類別的 FetchReportFailedPerUserSummaryEntries 方法
description: 取得失敗遠端桌面服務每個使用者用戶端存取授權 (RDS \ 160; 的摘要資訊。報表) 的每個使用者 Cal。
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- FetchReportFailedPerUserSummaryEntries 方法遠端桌面服務
- FetchReportFailedPerUserSummaryEntries 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，FetchReportFailedPerUserSummaryEntries 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983318"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a>Win32 TSLicenseReport 類別的 FetchReportFailedPerUserSummaryEntries 方法 \_

抓取每個使用者用戶端存取授權的失敗遠端桌面服務摘要資訊， (RDS 每個使用者的 Cal) 從報告。

## <a name="syntax"></a>語法


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartIndex* \[在\]
</dt> <dd>

要抓取之第一個報表專案的索引。 第一個報表專案的索引為零。

</dd> <dt>

*計數* \[in、out\]
</dt> <dd>

要從報表物件取出的報表專案數目。 值為零表示要抓取從 *StartIndex* 開始的所有報表專案。 傳回時，包含 *ReportFailedPerUserSummaryEntries* 陣列中的專案數。

</dd> <dt>

*ReportFailedPerUserSummaryEntries* \[擴展\]
</dt> <dd>

[**Win32 \_ TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md)類別的陣列，代表已取出的授權專案。 *Count* 參數包含這個陣列中的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                            |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> </dl>

 

 





