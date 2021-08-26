---
title: Win32_TSLicenseReportPerDeviceEntry 類別
description: 提供有關每一裝置用戶端存取使用權 (RDS \ 160; 的失敗遠端桌面服務詳細資料;) 的每一裝置 CAL。
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry 類別遠端桌面服務
- Win32_TSLicenseReportPerDeviceEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbcdad271a346820b318c94bed7ce6b9b9527d3fdd7df9cc3f1dc9d9a97aae3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008418"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>Win32 \_ TSLicenseReportPerDeviceEntry 類別

提供 (RDS 每一裝置的 CAL) 的每一裝置用戶端存取授權失敗遠端桌面服務詳細資料。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseReportPerDeviceEntry** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseReportPerDeviceEntry** 類別具有這些屬性。

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

「VDI 進階版 Suite 每個裝置訂用帳戶授權」

「RDS 每一裝置的 CAL」

「RDS 每個使用者的 CAL」

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

授權的到期日。

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

**sHardwareId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

電腦的硬體識別碼。

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

嘗試授權發行的電腦名稱稱。

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

[**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

