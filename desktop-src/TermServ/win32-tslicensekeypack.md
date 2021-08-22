---
title: Win32_TSLicenseKeyPack 類別
description: 提供用來查看和安裝遠端桌面服務授權金鑰套件的方法和屬性。
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack 類別遠端桌面服務
- Win32_TSLicenseKeyPack 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7927270f262d0a66722660bf4b2c8f15cf75f49bb807abcff604af9edf58d99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137811"
---
# <a name="win32_tslicensekeypack-class"></a>Win32 \_ TSLicenseKeyPack 類別

提供用來查看和安裝遠端桌面服務授權金鑰套件的方法和屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a>成員

**Win32 \_ TSLicenseKeyPack** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSLicenseKeyPack** 類別具有這些方法。



| 方法                                                                                                        | 描述                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | 轉換目前金鑰套件中的授權。<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | 從另一部遠端桌面授權伺服器匯入，這是透過授權合約購買的遠端桌面服務授權金鑰套件，並會透過網際網路自動連接來驗證金鑰套件授權。<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | 從另一部遠端桌面授權伺服器匯入，這是使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | 從另一部遠端桌面授權伺服器匯入 Open License 遠端桌面服務授權金鑰套件。<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | 從另一部遠端桌面授權伺服器匯入，這是透過零售通路購買的遠端桌面服務授權金鑰套件。<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | 安裝透過合約授權購買的遠端桌面服務授權金鑰套件。<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | 安裝遠端桌面服務授權金鑰套件，此套件會使用透過網際網路或電話所收到的授權金鑰包識別碼。<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | 安裝透過 open license 合約購買的遠端桌面服務授權金鑰套件。<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | 安裝透過零售商店購買的遠端桌面服務授權金鑰套件。<br/>                                                                                                                                 |
| [**ReinstallAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | 重新安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | 重新安裝使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。<br/>                                                                                       |
| [**ReinstallOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | 重新安裝 Open License 遠端桌面服務授權金鑰套件。<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | 重新安裝透過零售通路購買的遠端桌面服務授權金鑰套件。<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | 從指定的金鑰套件中移除指定的遠端桌面服務授權數目。<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | 卸載遠端桌面服務授權金鑰套件。<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | 使用指定的金鑰套件識別碼卸載遠端桌面服務授權金鑰套件。<br/>                                                                                                                                |



 

### <a name="properties"></a>屬性

**Win32 \_ TSLicenseKeyPack** 類別具有這些屬性。

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ( "0"、"1"、"2"、"3" ) 、 [**BITVALUES**](/windows/desktop/WmiSdk/standard-qualifiers) ( "RD 會話"、"VDI 會話"、"CALISTA"、"vdi 合作夥伴" ) 
</dt> </dl>

TS 授權金鑰套件存取權限的辨識符號

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件中的可用授權數總計。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件的描述。

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

資料類型： **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件的到期日。

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件中已發行的授權總數。

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

遠端桌面服務授權金鑰套件的識別碼。

</dd> <dt>

**KeyPackType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面授權伺服器的金鑰套件類型。

| 值 | 描述 |
|-------|-------------|
| 0 | 遠端桌面服務的授權金鑰包類型未知。 |
| 1 | 遠端桌面服務授權金鑰套件類型是零售版購買。 |
| 2 | 遠端桌面服務的授權金鑰包類型為大量購買。 |
| 3 | 遠端桌面服務授權金鑰套件類型是並行授權。 |
| 4 | 遠端桌面服務的授權金鑰包類型為暫時性。 |
| 5 | 遠端桌面服務授權金鑰套件類型是 open 授權。 |
| 6 | 不支援。 |

**ProductType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件的產品類型。

| 值 | 描述 |
|-------|-------------|
| 0 | 遠端桌面服務授權金鑰套件產品類型是依裝置。 因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。 |
| 1 | 遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。 因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。 |
| 2 | 此產品類型無效。 |

**ProductVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件的產品版本。

| 值 | 描述 |
|-------|-------------|
| "Windows Server 2012" | 此授權僅支援執行 Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 的伺服器。 |
| "Windows Server 7" | 此授權僅支援執行 Windows Server 2008 R2 或 Windows Server 2008 的伺服器。 |
| "Windows Server 2008" | 只有執行 Windows Server 2008 的伺服器受到此金鑰套件的支援。 |

**ProductVersionID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件的產品版本識別碼。

| 值 | 描述 |
|-------|-------------|
| 0 | 不支援 |
| 1 | 不支援 |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**TotalLicenses**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務授權金鑰套件中的授權總數。

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

TS 授權金鑰套件類型和模型的辨識符號。 範例： VDI 每個裝置訂用帳戶授權，TS 每個使用者 CAL

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

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

