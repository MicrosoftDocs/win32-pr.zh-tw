---
title: Win32_TSLicenseReportFailedPerUserSummaryEntry 類別
description: 提供每個使用者發行失敗的網域詳細資料。
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserSummaryEntry 類別遠端桌面服務
- Win32_TSLicenseReportFailedPerUserSummaryEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933975"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a>Win32 \_ TSLicenseReportFailedPerUserSummaryEntry 類別

提供每個使用者發行失敗的網域詳細資料。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** 類別具有這些屬性。

<dl> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

指定授權發行失敗的網功能變數名稱稱。

</dd> <dt>

**FailedIssuanceCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

失敗的 issuances 數目。

</dd> </dl>

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

[**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

