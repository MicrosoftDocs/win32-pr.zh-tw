---
title: Win32_TSLicenseKeyPack 類別的 ImportAgreementLicenseKeyPack 方法
description: 從另一部遠端桌面授權伺服器匯入，這是透過授權合約購買的遠端桌面服務授權金鑰套件，並會透過網際網路自動連接來驗證金鑰套件授權。
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- ImportAgreementLicenseKeyPack 方法遠端桌面服務
- ImportAgreementLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ImportAgreementLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b911a722f4f26aaf83debcb70413cb9dad2b40d2ca12b4ad3310aee4510ca1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603801"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Win32 TSLicenseKeyPack 類別的 ImportAgreementLicenseKeyPack 方法 \_

從另一部遠端桌面授權伺服器匯入，這是透過授權合約購買的遠端桌面服務授權金鑰套件，並會透過網際網路自動連接來驗證金鑰套件授權。

## <a name="syntax"></a>語法


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
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

*AgreementType* \[在\]
</dt> <dd>

合約類型。

<dt>

0
</dt> <dd>

授權金鑰套件來自選取的大量授權合約 (，適用于具有250或更多電腦) 的客戶。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。

</dd> <dt>

1
</dt> <dd>

授權金鑰套件適用于具有250或更多電腦的客戶 Enterprise 大量授權合約。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。

</dd> <dt>

2
</dt> <dd>

授權金鑰套件來自較高教育機構的校園大量授權合約。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。

</dd> <dt>

3
</dt> <dd>

授權金鑰套件來自主要和次要機構的學校大量授權合約。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。

</dd> <dt>

4
</dt> <dd>

授權金鑰套件來自服務提供者的服務提供者授權合約，可讓您每月授權 Microsoft 軟體。 *SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。

</dd> <dt>

5
</dt> <dd>

授權金鑰套件來自另一個授權合約，例如開放價值、多年 Open License，以及 Open 訂用帳戶授權。 *SAgreementNumber* 參數是與您的程式資訊一起提供的合約編號。

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[在\]
</dt> <dd>

合約編號或註冊編號。 *SAgreementNumber* 參數是不含連字號的七位數數位字串。

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

要匯入的授權數目。

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

 

 





