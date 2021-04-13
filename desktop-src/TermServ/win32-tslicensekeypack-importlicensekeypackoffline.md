---
title: Win32_TSLicenseKeyPack 類別的 ImportLicenseKeyPackOffline 方法
description: 從另一部遠端桌面授權伺服器匯入，這是使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- ImportLicenseKeyPackOffline 方法遠端桌面服務
- ImportLicenseKeyPackOffline 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ImportLicenseKeyPackOffline 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508636"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 ImportLicenseKeyPackOffline 方法 \_

從另一部遠端桌面授權伺服器匯入，這是使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。

## <a name="syntax"></a>語法


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sLicenseKeyPackId* \[在\]
</dt> <dd>

包含35字元的授權碼。 只應將35個字元的英數位元字串指定為輸入。 不應新增連字號。

</dd> <dt>

*sSourceLSName* \[在\]
</dt> <dd>

來源遠端桌面授權伺服器的名稱。 這可以是完整的辨別名稱或伺服器的 IP 位址。

</dd> <dt>

*sSourceLSProductId* \[在\]
</dt> <dd>

遠端桌面授權伺服器識別碼。 是35字元的英數位元字串，不能包含連字號。

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

 

 





