---
title: Win32_TSLicenseReportFailedPerUserEntry 類別
description: 提供有關每個使用者用戶端存取使用權的失敗遠端桌面服務詳細資料 (RDS \ 160;) 的每個使用者 CAL。
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry 類別遠端桌面服務
- Win32_TSLicenseReportFailedPerUserEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383950"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>Win32 \_ TSLicenseReportFailedPerUserEntry 類別

提供每個使用者用戶端存取使用權 (RDS 每個使用者 CAL) 的失敗遠端桌面服務詳細資料。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseReportFailedPerUserEntry** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseReportFailedPerUserEntry** 類別具有這些屬性。

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定所發出之 CAL 的類型。 這會是下列其中一個值。

「內建 TS 每一裝置的 CAL」

「TS 每一裝置的 CAL」

「TS 網際網路連接器 CAL」

「TS 每個使用者 CAL」

「TS 或 RDS 每一裝置的 CAL」

「TS 或 RDS 每個使用者的 CAL」

「每個裝置訂用帳戶授權的 VDI 標準套件」

「VDI Premium Suite 每個裝置訂用帳戶授權」

「RDS 每一裝置的 CAL」

「RDS 每個使用者的 CAL」

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已發出 RDS 每個使用者 CAL 的遠端桌面服務版本。 這會是下列其中一個值。

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

**TriedIssuanceOn**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

嘗試發佈授權的日期。

</dd> <dt>

**使用者**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

嘗試發行授權的使用者名稱。

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

[**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

