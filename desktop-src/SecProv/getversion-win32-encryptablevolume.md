---
description: 傳回磁片區的 FVE 中繼資料版本。
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Win32_EncryptableVolume 類別的 GetVersion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972190"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetVersion 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetVersion** 方法會傳回磁片區的 FVE 中繼資料版本。

## <a name="syntax"></a>語法


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*版本* \[擴展\]
</dt> <dd>

類型： **uint32**

不帶正負號的整數，表示磁片區的中繼資料版本。



| 值                                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl> | 作業系統未知。<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Windows Vista 格式，這表示在執行 Windows Vista 的電腦上，磁片區受到 BitLocker 保護。<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Windows 7 格式，表示在執行 Windows 7 的電腦上使用 BitLocker 保護磁片區，或使用 [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) 方法升級元資料格式。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

如果磁片區已解除鎖定，而且沒有其他錯誤，則此方法會傳回零。



| 傳回碼/值                                                                                                                                                       | Description                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                       | 此方法已成功。<br/>                               |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl> | *Version* 參數的值無效。<br/> |
| <dl> <dt>**錯誤 \_不正確 \_ DATA**</dt> <dt>13 (0xD)</dt> </dl>       | 驅動程式傳回了不支援的資料格式。<br/>     |



 

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

 

 
