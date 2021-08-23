---
description: Win32_EncryptableVolume 類別的 ProtectKeyWithCertificateThumbprint 方法-驗證所提供憑證的「增強金鑰使用方法」 (EKU) 物件識別碼 (OID) 。
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Win32_EncryptableVolume 類別的 ProtectKeyWithCertificateThumbprint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 900138c611198114397caa94894a3802475e2bebe5138629c0f2b9bd2c58c220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891524"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ProtectKeyWithCertificateThumbprint 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithCertificateThumbprint** 方法會驗證所提供憑證 (OID) 的增強金鑰使用方法 (EKU) [*物件識別碼*](../secgloss/o-gly.md)。

## <a name="syntax"></a>語法


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FriendlyName* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

字串，指定此金鑰保護裝置的使用者指派字串識別碼。 如果未指定此參數，則會使用憑證中的主體名稱來建立 *FriendlyName* 參數。

</dd> <dt>

*CertThumbprint* \[在\]
</dt> <dd>

類型： **字串**

指定憑證指紋的字串。

</dd> <dt>

*VolumeKeyProtectorID* \[擴展\]
</dt> <dd>

類型： **字串**

唯一識別已建立金鑰保護裝置的字串，可用來管理此金鑰保護裝置。

如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                                           | 此方法成功。<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**錯誤 \_不正確 \_ DATA**</dt> <dt>13 (0xD)</dt> </dl>                                           | 資料無效。<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_E \_ 非 \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | 指定之憑證的 EKU 屬性不允許它用於 BitLocker 磁碟機加密。 BitLocker 不需要憑證擁有 EKU 屬性，但如果有設定，則必須將它設定為與 BitLocker 設定的 oid 相符的 OID。<br/> |
| <dl> <dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 不 \_ 允許**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | 群組原則不允許搭配 BitLocker 使用使用者憑證（例如智慧卡）。<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 必須 \_ 是 \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | 群組原則要求您提供智慧卡來使用 BitLocker。<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_E \_ 原則會 \_ 禁止 \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | 群組原則不允許使用自我簽署憑證。<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>備註

如果 OID 與登錄中服務控制器相關聯的 OID 不相符，則此方法會失敗。 這可防止使用者在磁片區上手動設定資料修復代理 (DRA) 保護裝置。 Dra 只能由服務設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 企業版， \[ 僅 Windows 7 旗艦版桌面應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
