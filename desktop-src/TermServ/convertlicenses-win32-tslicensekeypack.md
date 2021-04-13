---
title: Win32_TSLicenseKeyPack 類別的 ConvertLicenses 方法
description: 轉換目前金鑰套件中的授權。
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- ConvertLicenses 方法遠端桌面服務
- ConvertLicenses 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ConvertLicenses 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384081"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 ConvertLicenses 方法 \_

轉換目前金鑰套件中的授權。 如果授權是每個使用者的授權，則會轉換成每個裝置的授權。 如果授權是個別裝置授權，則會轉換為每個使用者的授權。

## <a name="syntax"></a>語法


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[在\]
</dt> <dd>

要轉換的授權數目。

</dd> <dt>

*KeypackID* \[擴展\]
</dt> <dd>

結果金鑰套件的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





