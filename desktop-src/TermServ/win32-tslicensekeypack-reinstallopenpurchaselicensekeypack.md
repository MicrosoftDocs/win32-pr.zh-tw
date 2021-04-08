---
title: Win32_TSLicenseKeyPack 類別的 ReinstallOpenPurchaseLicenseKeyPack 方法
description: 重新安裝 Open License 遠端桌面服務授權金鑰套件。
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- ReinstallOpenPurchaseLicenseKeyPack 方法遠端桌面服務
- ReinstallOpenPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ReinstallOpenPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686350"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 ReinstallOpenPurchaseLicenseKeyPack 方法 \_

重新安裝 Open License 遠端桌面服務授權金鑰套件。

## <a name="syntax"></a>語法


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sLicenseNumber* \[在\]
</dt> <dd>

授權金鑰套件所提供的8個字元數位字串。 *SLicenseNumber* 參數不能包含連字號。

</dd> <dt>

*sAuthorizationNumber* \[在\]
</dt> <dd>

以授權金鑰提供的15個字元的英數位元字串。 *SAuthorizationNumber* 參數不能包含連字號。

</dd> <dt>

*ProductVersion* \[在\]
</dt> <dd>

產品版本。

<dt>

0
</dt> <dd>

不支援。

</dd> <dt>

1
</dt> <dd>

不支援。

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[在\]
</dt> <dd>

產品類型。

<dt>

0
</dt> <dd>

遠端桌面服務授權金鑰套件產品類型是依裝置。 因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。

</dd> <dt>

1
</dt> <dd>

遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。 因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。

</dd> <dt>

2
</dt> <dd>

此產品類型無效。

</dd> </dl> </dd> <dt>

*LicenseCount* \[在\]
</dt> <dd>

要安裝的授權數目。

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

 

 





