---
title: Win32_TSLicenseKeyPack 類別的 RemoveLicensesWithIdCount 方法
description: 從指定的金鑰套件中移除指定的遠端桌面服務授權數目。
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- RemoveLicensesWithIdCount 方法遠端桌面服務
- RemoveLicensesWithIdCount 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，RemoveLicensesWithIdCount 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7cf3c5b47a68828fc4c4d35d682f9d1a79491e7b1b76489d0d1385ea765ccc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939998"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 RemoveLicensesWithIdCount 方法 \_

從指定的金鑰套件中移除指定的遠端桌面服務授權數目。

## <a name="syntax"></a>語法


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*KeyPackId* \[在\]
</dt> <dd>

包含要移除之授權的金鑰組識別碼。

</dd> <dt>

*LicenseCount* \[在\]
</dt> <dd>

要卸載的授權數目。

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

 

 





