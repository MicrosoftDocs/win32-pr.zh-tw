---
title: Win32_TSLicenseReport 類別
description: 提供 (RDS \ 160; 的每個使用者用戶端存取使用權遠端桌面服務實例每個使用者 CAL) 在遠端桌面授權伺服器上產生的使用方式報告，以及授權報告產生、提取及刪除作業的方法。
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport 類別遠端桌面服務
- Win32_TSLicenseReport 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843176"
---
# <a name="win32_tslicensereport-class"></a>Win32 \_ TSLicenseReport 類別

提供遠端桌面服務的每個使用者用戶端存取授權 (RDS 每個使用者的 CAL) 在遠端桌面授權伺服器上產生的使用方式報告，以及授權報告產生、提取和刪除作業的方法。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseReport** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSLicenseReport** 類別具有這些方法。



| 方法                                                                                                         | 描述                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | 刪除遠端桌面授權伺服器上的報表物件。 這不是靜態方法。<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | 抓取報表物件中的專案。<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | 抓取每個使用者用戶端存取授權的失敗遠端桌面服務詳細資料 (RDS 每個使用者的 Cal) 從報告。<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | 抓取每個使用者用戶端存取授權的失敗遠端桌面服務摘要資訊， (RDS 每個使用者的 Cal) 從報告。<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | 從報告取得 (RDS 每一裝置的 Cal) 的每一裝置用戶端存取授權發出遠端桌面服務的資訊。<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | 從報表物件中抓取授權摘要。<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | 不支援這個方法。<br/> **Windows server 2008 R2 和 Windows server 2008：** 在遠端桌面授權伺服器上產生目前的每個使用者授權使用量報表。<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | 在遠端桌面授權伺服器上產生目前的每個使用者授權使用量報表。<br/>                                                                                              |



 

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseReport** 類別具有這些屬性。

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

報表名稱。

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

資料類型： **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 授權報告產生日期和時間。

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

不支援這個屬性。

**Windows server 2008 R2 和 Windows server 2008：** 已安裝的 RDS 每個使用者 Cal 數目。

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

不支援這個屬性。

**Windows server 2008 R2 和 Windows server 2008：** 目前使用中的 RDS 每個使用者 Cal 數目。

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

不支援這個屬性。

**Windows server 2008 R2 和 Windows server 2008：** RD 授權報表範圍類型。

</dd> <dt>

**ScopeValue**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

不支援這個屬性。

**Windows server 2008 R2 和 Windows server 2008：** RD 授權報表範圍值。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 授權報表版本。

</dd> </dl>

## <a name="remarks"></a>備註

使用 WMI 產生的報表會顯示在 RD 授權管理員中。 使用 WMI 刪除的報表也會從 RD 授權管理員中刪除。

您必須是 Administrators 群組的成員，才能使用這個類別。

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

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

