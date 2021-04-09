---
title: Win32_TSLicenseKeyPack 類別的 ReinstallRetailPurchaseLicenseKeyPack 方法
description: 重新安裝透過零售通路購買的遠端桌面服務授權金鑰套件。
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- ReinstallRetailPurchaseLicenseKeyPack 方法遠端桌面服務
- ReinstallRetailPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ReinstallRetailPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024687"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 ReinstallRetailPurchaseLicenseKeyPack 方法 \_

重新安裝透過零售通路購買的遠端桌面服務授權金鑰套件。

## <a name="syntax"></a>語法


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
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

 

 





