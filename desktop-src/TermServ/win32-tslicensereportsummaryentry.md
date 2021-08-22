---
title: Win32_TSLicenseReportSummaryEntry 類別
description: 提供 (RDS \ 160; 的每個使用者用戶端存取授權已安裝和發行遠端桌面服務的摘要;) 的每個使用者 Cal。
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry 類別遠端桌面服務
- Win32_TSLicenseReportSummaryEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58efc2c70019037219d8eca986fa8afd81e4dc2d06cd638ee24fc59947e3bf3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137794"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>Win32 \_ TSLicenseReportSummaryEntry 類別

提供每個使用者用戶端存取授權 (RDS 每個使用者的 Cal) 的已安裝和發行遠端桌面服務的摘要。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseReportSummaryEntry** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseReportSummaryEntry** 類別具有這些屬性。

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已安裝的 RDS 每個使用者 Cal 數目。

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

所發出的 RDS 每個使用者 Cal 數目。

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已發出 RDS 每個使用者 CAL 的遠端桌面服務版本。

<dt>

"Windows Server 2012"
</dt> <dd>

此授權僅支援執行 Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 的伺服器。

</dd> <dt>

"Windows Server 7"
</dt> <dd>

此授權僅支援執行 Windows Server 2008 R2 或 Windows Server 2008 的伺服器。

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

此授權僅支援執行 Windows Server 2008 的伺服器。

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件的產品版本識別碼。

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

不支援。

</dd> <dt>

0
</dt> <dd>

不支援。

</dd> </dl>

</dd> <dt>

**TSCALAvailability**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RDS 每個使用者 Cal 的可用性。 這會是下列其中一個值。

<dt>

目前
</dt> <dd>

您可以使用 RDS 每個使用者的 Cal。

</dd> <dt>

有限
</dt> <dd>

RDS 每個使用者 Cal 的可用性有限。

</dd> <dt>

"None"
</dt> <dd>

無法使用 RDS 每個使用者的 Cal。

</dd> <dt>

「未追蹤」
</dt> <dd>

未追蹤 RDS 每個使用者 Cal 的可用性。

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RDS 每個使用者 Cal 的類型。 這會是下列其中一個值。

<dt>

「每個裝置」
</dt> <dd>

每個裝置會發出 RDS 每個使用者的 Cal。

</dd> <dt>

「每位使用者」
</dt> <dd>

每個使用者都會發出 RDS 每個使用者的 Cal。

</dd> <dt>

不明
</dt> <dd>

RDS 每個使用者 Cal 的類型未知。

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





