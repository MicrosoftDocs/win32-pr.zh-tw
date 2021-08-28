---
title: Win32_TSLicenseKeyPack 類別的 ReinstallLicenseKeyPackOffline 方法
description: 重新安裝使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- ReinstallLicenseKeyPackOffline 方法遠端桌面服務
- ReinstallLicenseKeyPackOffline 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ReinstallLicenseKeyPackOffline 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b72ad2175e0d97cba5733461431726781aebc9a53c1a23f408f7d14e75dd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058326"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 ReinstallLicenseKeyPackOffline 方法 \_

重新安裝使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。

## <a name="syntax"></a>語法


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sLicenseKeyPackId* \[在\]
</dt> <dd>

包含35字元的授權碼。 只應將35個字元的英數位元字串指定為輸入。 不應新增連字號。

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

 

 





