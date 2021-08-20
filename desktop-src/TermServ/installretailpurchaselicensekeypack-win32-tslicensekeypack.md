---
title: Win32_TSLicenseKeyPack 類別的 InstallRetailPurchaseLicenseKeyPack 方法
description: 安裝透過零售通路購買的遠端桌面服務授權金鑰套件。
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- InstallRetailPurchaseLicenseKeyPack 方法遠端桌面服務
- InstallRetailPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，InstallRetailPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427107e6d581c839ee83767c7c95426e13d16a392b7764924997c01785b85d46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129589"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 InstallRetailPurchaseLicenseKeyPack 方法 \_

安裝透過零售通路購買的遠端桌面服務授權金鑰套件。

## <a name="syntax"></a>語法


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sLicenseCode* \[在\]
</dt> <dd>

包含25個字元的授權碼。 只應提供25個字元的英數位元字串做為輸入。 不應新增連字號。

</dd> <dt>

*KeyPackId* \[擴展\]
</dt> <dd>

接收金鑰組識別碼。

</dd> </dl>

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

 

