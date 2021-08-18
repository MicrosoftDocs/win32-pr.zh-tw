---
title: Win32_TSLicenseReport 類別的 FetchReportEntries 方法
description: 遠端桌面服務 (RDS \ 160; 的每個使用者用戶端存取授權取得詳細資料報表) 的每個使用者 Cal。 每個專案都代表一個 RDS \ 160;每個目前使用中的使用者 CAL。
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- FetchReportEntries 方法遠端桌面服務
- FetchReportEntries 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，FetchReportEntries 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35c2af0578b0b130b5ef92bae5d374cc4ba2ba82c172689d00782e68b65c143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871728"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a>Win32 TSLicenseReport 類別的 FetchReportEntries 方法 \_

遠端桌面服務每個使用者用戶端存取授權的詳細資料， (RDS 每個使用者的 Cal) 從報告取得。 每個專案都代表目前使用中的 RDS 每個使用者 CAL。

## <a name="syntax"></a>語法


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartIndex* \[在\]
</dt> <dd>

要接收之第一個報表專案的索引。 第一個報表專案的索引為零。

</dd> <dt>

*計數* \[in、out\]
</dt> <dd>

要從報表物件取出的報表專案數目。 值為零表示要抓取從 *StartIndex* 開始的所有報表專案。 傳回時，包含 *ReportEntries* 陣列中的專案數。

</dd> <dt>

*ReportEntries* \[擴展\]
</dt> <dd>

傳回 [**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md) 類別的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 值為 **LSERVER \_ 我 \_ 沒有 \_ 其他 \_ 資料** (0x4001) 指出沒有其他報表專案。

## <a name="remarks"></a>備註

這不是靜態方法。 您必須從每個使用者授權使用量報表物件呼叫這個方法。

您必須是 Administrators 群組的成員，才能呼叫這個方法。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

