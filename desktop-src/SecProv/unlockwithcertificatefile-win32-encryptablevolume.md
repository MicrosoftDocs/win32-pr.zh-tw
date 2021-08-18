---
description: 使用提供的憑證檔案來取得衍生金鑰，並解除鎖定加密的磁片區。
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Win32_EncryptableVolume 類別的 UnlockWithCertificateFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 576de5820e5b16b59a0b77659a4833a261ecd9ef8445306ce3d6f320c664f833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004226"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 UnlockWithCertificateFile 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithCertificateFile** 方法會使用提供的 [*憑證*](../secgloss/c-gly.md)檔案來取得衍生金鑰，並解除鎖定加密的磁片區。

> [!Note]  
> 如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。

 

## <a name="syntax"></a>語法


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

類型： **字串**

字串，指定用來取出憑證指紋之 .cer 檔案的位置和名稱。 [*加密*](../secgloss/e-gly.md)憑證必須以 .cer 格式匯出 ([*可辨別編碼規則*](../secgloss/d-gly.md) (DER) 編碼的二進位 [*x.509*](../secgloss/x-gly.md)或 Base-64 編碼的 x.509) 。 您可以從 Microsoft PKI、協力廠商 PKI 或自我簽署來產生加密憑證。

</dd> <dt>

*PIN* \[在\]
</dt> <dd>

類型： **字串**

使用者指定的個人識別碼字串。 此字串必須包含4到20位數的序列。 這個字串是用來以無訊息方式驗證 [*金鑰儲存提供者*](../secgloss/k-gly.md) ， (KSP) 搭配 [*智慧卡*](../secgloss/s-gly.md)使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                            | 此方法成功。<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**錯誤 \_\_找不 \_ 到**</dt>檔案 <dt>0000000002 (0x2)</dt> </dl>                 | 系統無法提出指定的檔案。<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | 無法使用所提供的資訊來解除鎖定磁片區。 <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt> </dl>    | 提供的金鑰保護裝置不存在於磁片區上。 您必須輸入其他金鑰保護裝置。<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_E \_ PRI加值稅EKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | 無法授權與指定憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md)。 未提供私密金鑰授權，或提供的授權無效。<br/> |



 

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

 

 
