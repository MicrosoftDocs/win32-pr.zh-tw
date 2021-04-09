---
description: 開始解密完整加密的磁片區，或繼續解密部分加密的磁片區。
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: 'Win32_EncryptableVolume 類別的解密方法 (Infocard) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849450"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的解密方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **解密** 方法會開始解密完整加密的磁片區，或繼續解密部分加密的磁片區。

當解密暫停或進行中時，此方法的行為與 [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)相同。 當加密暫停或進行中時，此方法會還原加密並開始解密。 解密完成之後，這個磁片區上的所有金鑰保護裝置都會從系統中移除，而磁片區會轉換成標準 NTFS 檔案系統。

> [!Note]  
> 如果光碟已加密硬體，則 **解密** 方法會將頻外狀態設為「永遠解除鎖定」、移除所有相關聯的中繼資料，以及將磁片磁碟機的安全識別碼設為零。

 

## <a name="syntax"></a>語法


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

這個方法會立即傳回。 如果磁片區已經完全解密，而且沒有其他錯誤存在，這個方法會傳回0。



| 傳回碼/值                                                                                                                                                                       | Description                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                       | 此方法成功。<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>      | 磁片區已鎖定。<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_E \_ 再次 \_ 已啟用**</dt> <dt>2150694953 (0x80310029)</dt> </dl> | 此磁片區無法解密，因為可用來自動解除鎖定資料磁片區的金鑰可以使用。 <br/> 使用 [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) 來移除這些金鑰。<br/> |



 

## <a name="security-considerations"></a>安全性考量

呼叫 **解密** 方法會讓資料保持未受保護。

如果在使用此方法之前，磁片區的保護狀態為 1 () 保護，此方法的成功完成會將保護狀態變更為 0 (保護關閉) ，因為依定義，部分加密的磁片區不受保護。

## <a name="remarks"></a>備註

如果磁片區尚未完全解密，執行 **解密** 會導致 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 表示解密正在進行中，並顯示維持加密的磁片區百分比。

如果在執行此方法之前，磁片區的保護狀態是「開啟」，則執行此方法會將保護狀態變更為「關閉」，因為依定義，部分加密的磁片區不受保護。

如果這個方法是在目前正在執行的作業系統磁片區上執行，而這個作業系統磁片區是用來自動解除鎖定資料磁片區 (請參閱方法 [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) 您必須先呼叫方法 [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| 標頭<br/>                   | <dl> <dt>Infocard。h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
