---
description: 指出是否可從 Windows 存取磁片區的內容。
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Win32_EncryptableVolume 類別的 GetLockStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970787"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetLockStatus 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetLockStatus** 方法會指出是否可以從 Windows 存取磁片區的內容。

## <a name="syntax"></a>語法


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LockStatus* \[擴展\]
</dt> <dd>

類型： **uint32**

指定是否可從 Windows 存取磁片區的內容。



| 值                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> 已 <dt>**解除鎖定**</dt> <dt>0</dt> </dl> | 針對標準 HDD：<br/> 可以存取磁片區的完整內容。 已解除鎖定的磁片區可能已完全解密，或有可在磁片上清除的加密金鑰。 包含目前正在執行之作業系統的磁片區 (例如，執行中的 Windows 磁片區) 一律可供存取且無法鎖定。<br/> 針對 EHDD：<br/> 頻外永久解除鎖定。<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**鎖定**</dt>的 <dt>1</dt> </dl>         | 針對標準 HDD：<br/> 無法存取磁片區的所有或部分內容。 鎖定的磁片區必須部分或完整加密，且不能在磁片上的純文字中提供加密金鑰。<br/> 針對 EHDD：<br/> 頻外已解除鎖定或鎖定。<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

使用 [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) 和 [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) 來取得磁片區內容的存取權。 使用 [**鎖定**](lock-win32-encryptablevolume.md) 方法來放棄存取磁片區內容。

包含目前執行之作業系統的磁片區永遠可供存取且無法鎖定。

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

 

 
