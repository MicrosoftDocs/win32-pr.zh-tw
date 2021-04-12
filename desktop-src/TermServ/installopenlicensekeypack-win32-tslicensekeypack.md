---
title: Win32_TSLicenseKeyPack 類別的 InstallOpenLicenseKeyPack 方法
description: 安裝 Open License 遠端桌面服務授權金鑰套件。
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- InstallOpenLicenseKeyPack 方法遠端桌面服務
- InstallOpenLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，InstallOpenLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464793"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 InstallOpenLicenseKeyPack 方法 \_

安裝 Open License 遠端桌面服務授權金鑰套件。

## <a name="syntax"></a>語法


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>參數

*sLicenseNumber* \[在\]

授權金鑰套件所提供的8個字元數位字串。 *SLicenseNumber* 參數不能包含連字號。

*sAuthorizationNumber* \[在\]

以授權金鑰提供的15個字元的英數位元字串。 *SAuthorizationNumber* 參數不能包含連字號。

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
</dt> <dd>

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

 

