---
title: Win32_TSLicenseReportEntry 類別
description: 提供 (RDS \ 160; 的每個使用者用戶端存取使用權發出遠端桌面服務的詳細資料;) 的每個使用者 CAL。
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry 類別遠端桌面服務
- Win32_TSLicenseReportEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383953"
---
# <a name="win32_tslicensereportentry-class"></a>Win32 \_ TSLicenseReportEntry 類別

提供每個使用者用戶端存取使用權 (RDS 每個使用者 CAL) 所發出遠端桌面服務的詳細資料。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseReportEntry** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseReportEntry** 類別具有這些屬性。

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定所發出之 CAL 的類型。 這會是下列其中一個值。

**Windows server 2008 R2 和 Windows server 2008：** 不支援這個屬性。

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

**ExpirationDate**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發給使用者之授權的到期日。

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

**使用者**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

授權簽發者的使用者名稱。

</dd> </dl>

## <a name="remarks"></a>備註

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

