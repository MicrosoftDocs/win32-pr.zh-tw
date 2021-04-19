---
title: Win32_TSLicenseKeyPack 類別的 ImportOpenPurchaseLicenseKeyPack 方法
description: 從另一部遠端桌面授權伺服器匯入 Open License 遠端桌面服務授權金鑰套件。
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- ImportOpenPurchaseLicenseKeyPack 方法遠端桌面服務
- ImportOpenPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ImportOpenPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976975"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 ImportOpenPurchaseLicenseKeyPack 方法 \_

從另一部遠端桌面授權伺服器匯入 Open License 遠端桌面服務授權金鑰套件。

## <a name="syntax"></a>語法


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
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

要匯入的授權數目

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

 

 





