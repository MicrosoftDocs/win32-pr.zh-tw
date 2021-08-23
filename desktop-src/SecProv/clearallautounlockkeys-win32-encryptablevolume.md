---
description: 移除儲存在目前正在執行的作業系統磁片區上的所有外部金鑰和相關資訊，以用來自動解除鎖定資料磁片區。
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Win32_EncryptableVolume 類別的 ClearAllAutoUnlockKeys 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 46ee3791425afafe63b0d566c3f4204fecc9195f4341b90caee4c95306afdeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668168"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ClearAllAutoUnlockKeys 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ClearAllAutoUnlockKeys** 方法會移除所有儲存在目前執行之作業系統磁片區的外部金鑰和相關資訊，以用來自動解除鎖定資料磁片區。

## <a name="syntax"></a>語法


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                   | 描述                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                   | 此方法成功。<br/>                                                        |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/> |
| <dl> <dt>**FVE \_E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | 方法只能針對目前正在執行的作業系統磁片區執行。<br/>     |



 

## <a name="remarks"></a>備註

**ClearAllAutoUnlockKeys** 與目前正在執行的作業系統相關聯的每個資料磁片區（甚至是目前尚未連線到該電腦的資料磁片區），可達到與執行 [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) 相同的功能。 它也會移除與不再存在之資料磁片區相關聯的任何過時解除鎖定資訊。

在目前執行中的作業系統磁片區上呼叫 [**解密**](decrypt-win32-encryptablevolume.md) 之前，請使用 **ClearAllAutoUnlockKeys** 來確保放置在作業系統登錄中的資訊可自動解除鎖定資料磁片區，而無法在磁片上清除。

順利執行 **ClearAllAutoUnlockKeys** 之後，就可以使用 [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) 或 [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) 方法來解除鎖定這部電腦上的所有資料磁片區。 使用 [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) 重新啟用資料磁片區的自動解除鎖定。

如果未傳回任何其他錯誤， **ClearAllAutoUnlockKeys** 會從登錄中移除任何磁片區保護程式識別碼，以及用來自動解除鎖定目前正在執行之作業系統磁片區的任何資料磁片區的外部金鑰。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Enterprise，僅 Windows vista 旗艦版傳統型 \[ 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
