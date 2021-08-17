---
title: Win32_TSLicenseServer 類別
description: 提供方法和屬性，以在遠端桌面授權伺服器上查看並設定遠端桌面授權 (RD 授權) 。
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer 類別遠端桌面服務
- Win32_TSLicenseServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7c73c1d1a48bbc76b4988afca8a07fd9ce505d0633c74f67306901259d9f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126508"
---
# <a name="win32_tslicenseserver-class"></a>Win32 \_ TSLicenseServer 類別

提供方法和屬性，以在遠端桌面授權伺服器上查看並設定遠端桌面授權 (RD 授權) 。

## <a name="syntax"></a>語法

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseServer** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSLicenseServer** 類別具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | 使用透過電話或網際網路取得的遠端桌面授權伺服器識別碼，來啟用遠端桌面授權伺服器。<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | 透過網際網路自動啟用遠端桌面授權伺服器。 當呼叫這個方法時， **FirstName**、 **LastName**、 **Company** 和 **國家/地區** 屬性不得為空白，否則方法將會失敗。<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | 將遠端桌面授權伺服器新增至與授權伺服器相同網域中網域控制站上的遠端桌面授權伺服器群組。<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | 變更遠端桌面授權伺服器的探索領域。<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | 不支援這個方法。<br/> **Windows server 2008 R2 和 Windows server 2008：** 在遠端桌面授權伺服器上建立終端機伺服器電腦本機群組。<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | 使用透過電話收到的確認碼來停用遠端桌面授權伺服器。<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | 透過網際網路停用遠端桌面授權伺服器。 當呼叫這個方法時， **FirstName** 和 **LastName** 屬性不得為空白，否則方法將會失敗。<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | 抓取目前的啟用狀態。<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | 如果伺服器目前已啟用，則抓取遠端桌面授權伺服器識別碼。<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | 抓取遠端桌面授權伺服器是否為指定網域中網域控制站上的遠端桌面授權伺服器群組的成員。<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | 抓取 RD 授權是否安裝在網域控制站上。<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | 抓取是否已在遠端桌面授權伺服器上啟用「防止授權升級」群組原則設定。<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | 抓取 Active Directory Domain Services (AD DS) 中是否發佈遠端桌面授權伺服器。<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | 抓取是否在 Active Directory Domain Services 中將遠端桌面授權伺服器註冊為服務連接點。<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | 抓取是否已在遠端桌面授權伺服器上啟用 [授權伺服器安全性群組] 群組原則設定。<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | 抓取 RD 工作階段主機伺服器是否允許從遠端桌面授權伺服器 (RDS Cal) 要求遠端桌面服務用戶端存取授權。<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | 不支援這個方法。<br/> **Windows server 2008 R2 和 Windows server 2008：** 抓取終端機伺服器電腦本機群組是否存在於遠端桌面授權伺服器上。<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | 抓取 RD 工作階段主機伺服器是否為遠端桌面授權伺服器上終端機伺服器電腦本機群組的成員。<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | 在 AD DS 發佈遠端桌面授權伺服器。<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | 使用透過電話或網際網路取得的新遠端桌面授權伺服器識別碼，重新開機遠端桌面授權伺服器。<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | 透過網際網路重新開機遠端桌面授權伺服器。 當呼叫這個方法時， **FirstName** 和 **LastName** 屬性不得為空白，否則方法將會失敗。<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | 在 Active Directory Domain Services 中，將遠端桌面授權伺服器註冊為服務連接點。<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | 從與授權伺服器相同網域的網域控制站上的遠端桌面授權伺服器群組中，移除遠端桌面授權伺服器。<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | 不支援這個方法。<br/> **Windows server 2008 R2 和 Windows server 2008：** 從遠端桌面授權伺服器移除終端機伺服器電腦本機群組。<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | 從 AD DS Unpublishes 遠端桌面授權伺服器。<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | 將遠端桌面授權伺服器移除為 Active Directory Domain Services 中的服務連接點。<br/>                                                                                                                       |



 

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseServer** 類別具有這些屬性。

<dl> <dt>

**位址**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的街道位址。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。 使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) 

</dd> <dt>

**城市**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的城市。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。 使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) 

</dd> <dt>

**公司**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的公司。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。

</dd> <dt>

**/**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的國家/地區。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RDS 授權資料庫的路徑。

</dd> <dt>

**電子郵件**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的電子郵件地址。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)、 [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)或 [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。  (針對這些方法呼叫，這個屬性是選擇性的。 ) 

</dd> <dt>

**名字**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的名字。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)、 [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)或 [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。

</dd> <dt>

**姓氏**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的姓氏。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)、 [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)或 [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的組織單位。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 時，會使用這個屬性。 使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) 

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的郵遞區號。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。 使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) 

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面授權伺服器的產品識別碼。

</dd> <dt>

**ServerRole**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述組織內遠端桌面授權伺服器的授權範圍。

<dt>

0
</dt> <dd>

相同工作組中的 RD 工作階段主機伺服器可以探索授權伺服器。

</dd> <dt>

1
</dt> <dd>

相同網域中 RD 工作階段主機伺服器可以探索授權伺服器。

</dd> <dt>

2
</dt> <dd>

相同樹系中的多個網域 RD 工作階段主機伺服器可以探索授權伺服器。

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 授權連絡人的狀態。 呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。 使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) 

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面授權伺服器的版本。

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面授權伺服器的版本號碼。

</dd> </dl>

## <a name="remarks"></a>備註

這個類別是 [單一](/windows/desktop/WmiSdk/standard-wmi-qualifiers) 類別，而且只能有一個實例。 此類別中包含的所有方法都是靜態的。

您必須是 Administrators 群組的成員，才能使用這個類別。 如果呼叫端不是系統管理員群組的成員，則傳回的屬性會是空的。

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

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

