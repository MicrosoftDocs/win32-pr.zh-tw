---
description: 使用提供的憑證指紋來取得衍生金鑰，並解除鎖定加密的磁片區。
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Win32_EncryptableVolume 類別的 UnlockWithCertificateThumbprint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690091"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 UnlockWithCertificateThumbprint 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithCertificateThumbprint** 方法會使用提供的 [*憑證*](../secgloss/c-gly.md)指紋來取得衍生金鑰，並解除鎖定加密的磁片區。

> [!Note]  
> 如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。

 

## <a name="syntax"></a>語法


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CertThumbprint* \[在\]
</dt> <dd>

類型： **字串**

憑證指紋值為0，因此會搜尋本機存放區以取得適當的憑證。 如果找到單一 BitLocker 憑證，搜尋便會成功。 如果找不到一個或多個憑證，方法將會失敗。

</dd> <dt>

*PIN* \[在\]
</dt> <dd>

類型： **字串**

使用者指定的個人識別碼字串。 此字串必須包含4到20位數的序列。 這個字串是用來以無訊息方式驗證 [*金鑰儲存提供者*](../secgloss/k-gly.md) ， (KSP) 搭配 [*智慧卡*](../secgloss/s-gly.md)使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                            | Description                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                            | 此方法成功。<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | 無法使用所提供的資訊來解除鎖定磁片區。 <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt> </dl>    | 提供的金鑰保護裝置不存在於磁片區上。 您必須輸入其他金鑰保護裝置。<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_E \_ PRI加值稅EKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | 無法授權與指定憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 。 未提供私密金鑰授權，或提供的授權無效。<br/> |



 

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

 

 
