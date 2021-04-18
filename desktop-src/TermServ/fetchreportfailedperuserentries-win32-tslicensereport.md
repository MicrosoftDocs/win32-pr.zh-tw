---
title: Win32_TSLicenseReport 類別的 FetchReportFailedPerUserEntries 方法
description: 取得 (RDS \ 160; 的每個使用者用戶端存取授權失敗遠端桌面服務詳細資料;報表) 的每個使用者 Cal。
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- FetchReportFailedPerUserEntries 方法遠端桌面服務
- FetchReportFailedPerUserEntries 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，FetchReportFailedPerUserEntries 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509287"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a>Win32 TSLicenseReport 類別的 FetchReportFailedPerUserEntries 方法 \_

抓取每個使用者用戶端存取授權的失敗遠端桌面服務詳細資料 (RDS 每個使用者的 Cal) 從報告。

## <a name="syntax"></a>語法


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
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

要從報表物件取出的報表專案數目。 值為零表示要抓取從 *StartIndex* 開始的所有報表專案。 傳回時，包含 *ReportFailedPerUserEntries* 陣列中的專案數。

</dd> <dt>

*ReportFailedPerUserEntries* \[擴展\]
</dt> <dd>

[**Win32 \_ TSLicenseReportFailedPerUserEntry**](win32-tslicensereportfailedperuserentry.md)類別的陣列，代表已取出的授權專案。 *Count* 參數包含這個陣列中的元素數目。

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

 

 





