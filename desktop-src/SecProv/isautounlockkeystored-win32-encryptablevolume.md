---
description: 指出是否有任何可用來自動解除鎖定資料磁片區的外部金鑰或相關資訊，是否存在於目前正在執行的作業系統磁片區中。
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Win32_EncryptableVolume 類別的 IsAutoUnlockKeyStored 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990373"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 IsAutoUnlockKeyStored 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsAutoUnlockKeyStored** 方法會指出是否有任何可用來自動解除鎖定資料磁片區的外部金鑰或相關資訊，是否存在於目前正在執行的作業系統磁片區中。

## <a name="syntax"></a>語法


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsAutoUnlockKeyStored* \[擴展\]
</dt> <dd>

類型： **布林值**

如果可用來自動解除鎖定資料磁片區的任何資訊都儲存在目前正在執行的作業系統磁片區的登錄中，則為 **true** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                   | Description                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                   | 此方法成功。<br/>                                                        |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/> |
| <dl> <dt>**FVE \_E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | 方法只能針對目前正在執行的作業系統磁片區執行。<br/>     |



 

## <a name="remarks"></a>備註

使用 [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) 從目前正在執行的作業系統磁片區中移除所有解除鎖定的資訊。

當目前執行中的作業系統磁片區正在執行時，系統會在針對資料磁片區執行 [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) 時，儲存用來解除鎖定磁片區的資訊。

**IsAutoUnlockKeyStored** 與 [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) 的不同之處在于，即使已針對目前連線到電腦的所有資料磁片區停用自動解除鎖定，仍可能會有與已中斷連線的資料磁片區或已不存在的資料磁片區相關聯的解除鎖定資訊。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
