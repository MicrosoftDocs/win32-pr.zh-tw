---
description: 將修復資料備份至 Active Directory。
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Win32_EncryptableVolume 類別的 BackupRecoveryInformationToActiveDirectory 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bd24a13b7f41f2e87f48c2e5ba97a890d10df3245fcbc6e16f9291c1e0629d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892956"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 BackupRecoveryInformationToActiveDirectory 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **BackupRecoveryInformationToActiveDirectory** 方法會將修復資料備份至 Active Directory。 此方法要求磁片區上必須有數值密碼保護裝置。 您也必須將群組原則設定為可讓您將修復資訊備份到 Active Directory。

## <a name="syntax"></a>語法


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。 此金鑰保護裝置必須是數位密碼保護裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                            | 此方法成功。<br/>                                                                                    |
| <dl> <dt>**S \_FALSE**</dt> <dt>1 (0x1)</dt> </dl>                                         | 群組原則不允許將修復資訊儲存到 Active Directory。<br/>                         |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                             |
| <dl> <dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | 指定的金鑰保護裝置不是數位金鑰保護裝置。 您必須輸入數位密碼保護裝置。 <br/> |



 

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

 

 




