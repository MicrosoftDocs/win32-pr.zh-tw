---
description: 捕獲公開金鑰保護裝置的公開金鑰和憑證指紋。
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Win32_EncryptableVolume 類別的 GetKeyProtectorCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975220"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetKeyProtectorCertificate 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorCertificate** 方法會抓取公開金鑰保護裝置的 [*公開金鑰*](../secgloss/p-gly.md)和 [*憑證*](../secgloss/c-gly.md)指紋。

## <a name="syntax"></a>語法


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> <dt>

*PublicKey* \[擴展\]
</dt> <dd>

類型： **uint8 \[ \]**

指定公開金鑰的位元組陣列。

</dd> <dt>

*CertThumbprint* \[擴展\]
</dt> <dd>

類型： **字串**

指定憑證指紋的字串。

</dd> <dt>

*CertType* \[擴展\]
</dt> <dd>

類型： **uint32**

指定金鑰保護裝置類型的不帶正負號的整數。 此整數可用來區分資料修復代理 (DRA) 和使用者憑證。



| 值                                                                        | 意義                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | 憑證是 DRA。<br/>     |
| <dl> <dt>2</dt> </dl> | 憑證不是 DRA。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                                       | Description                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                                       | 此方法成功。<br/>                                                                           |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | 指定的金鑰保護裝置不是金鑰保護裝置。 您必須輸入其他金鑰保護裝置。<br/>            |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>                      | 此磁片磁碟機已由 BitLocker 磁碟機加密鎖定。 您必須將此磁片區從主控台解除鎖定。 <br/> |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                    |
| <dl> <dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 需要**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | 群組原則需要使用使用者憑證（例如智慧卡）。<br/>                           |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
