---
title: Win32_TSLicenseKeyPack 類別的 InstallAgreementLicenseKeyPack 方法
description: 安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- InstallAgreementLicenseKeyPack 方法遠端桌面服務
- InstallAgreementLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，InstallAgreementLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968791"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 InstallAgreementLicenseKeyPack 方法 \_

安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。

## <a name="syntax"></a>語法


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>參數

*AgreementType* \[在\]

合約類型。

| 值 | 描述 |
|-------|-------------|
| 0 | 授權金鑰套件來自選取的大量授權合約 (，適用于具有250或更多電腦) 的客戶。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。 |
| 1 | 授權金鑰套件是針對具有250或更多電腦的客戶提供的 Enterprise volume 授權合約。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。 |
| 2 | 授權金鑰套件來自較高教育機構的校園大量授權合約。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。 |
| 3 | 授權金鑰套件來自主要和次要機構的學校大量授權合約。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。 |
| 4 | 授權金鑰套件來自服務提供者的服務提供者授權合約，可讓您每月授權 Microsoft 軟體。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。 |
| 5 | 授權金鑰套件來自另一個授權合約，例如開放價值、多年 Open License，以及 Open 訂用帳戶授權。 *SAgreementNumber* 參數是與您的程式資訊一起提供的合約編號。 |

*sAgreementNumber* \[在\]

合約編號或註冊編號。 *SAgreementNumber* 參數是不含連字號的七位數數位字串。

*ProductVersion* \[在\]

產品版本。

| 值 | 描述 |
|-------|-------------|
| 0 | 不支援 |
| 1 | 不支援 |
| 2 | Windows Server 2008/Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[在\]

產品類型。

| 值 | 描述 |
|-------|-------------|
| 0 | 遠端桌面服務授權金鑰套件產品類型是依裝置。 因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。 |
| 1 | 遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。 因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。 |
| 2 | 此產品類型無效。 |

*LicenseCount* \[在\]

要安裝的授權數目。

*KeyPackId* \[擴展\]

接收金鑰組識別碼。

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

