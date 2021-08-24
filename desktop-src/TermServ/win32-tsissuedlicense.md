---
title: Win32_TSIssuedLicense 類別
description: 描述 (RDS \ 160; 的每一裝置用戶端存取使用權遠端桌面服務實例每一裝置的 Cal) 從遠端桌面授權伺服器發出。
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense 類別遠端桌面服務
- Win32_TSIssuedLicense 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76127d41c6a571b6bc75bc74378b21f76f4b38c05f0a223d36e979dccf89a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656158"
---
# <a name="win32_tsissuedlicense-class"></a>Win32 \_ TSIssuedLicense 類別

描述從遠端桌面授權伺服器發出的每一裝置用戶端存取授權 (RDS 每一裝置的 Cal) 的遠端桌面服務實例。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a>成員

**Win32 \_ TSIssuedLicense** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSIssuedLicense** 類別具有這些方法。



| 方法                                         | 描述                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**撤銷**](revoke-win32-tsissuedlicense.md) | 撤銷 **Win32 \_ TSIssuedLicense** 物件所代表的 RDS 每一裝置 cal。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ TSIssuedLicense** 類別具有這些屬性。

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別授權將到期的日期。

</dd> <dt>

**IssueDate**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別授權的發出日期。

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別遠端桌面服務的授權金鑰套件。

</dd> <dt>

**LicenseId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

此授權的唯一識別碼。

</dd> <dt>

**LicenseStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

授權的狀態。

<dt>

0
</dt> <dd>

授權狀態不明。

</dd> <dt>

1
</dt> <dd>

授權是暫時性授權。

</dd> <dt>

2
</dt> <dd>

授權為使用中狀態。

</dd> <dt>

3
</dt> <dd>

授權是升級授權。

</dd> <dt>

4
</dt> <dd>

已撤銷授權。

</dd> <dt>

5
</dt> <dd>

授權狀態為 [擱置中]。

</dd> <dt>

6
</dt> <dd>

授權是並行授權。

</dd> </dl>

</dd> <dt>

**sHardwareId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

授權發出的硬體識別碼。

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

授權發出的電腦名稱稱。

</dd> <dt>

**sIssuedToUser**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發出授權的使用者名稱。

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

