---
description: 允許在掛接磁片區時自動解除鎖定資料磁片區。
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Win32_EncryptableVolume 類別的 EnableAutoUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849444"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 EnableAutoUnlock 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **EnableAutoUnlock** 方法可讓您在掛接磁片區時自動解除鎖定資料磁片區。

自動解除鎖定可將外部金鑰儲存至作業系統，以將磁片區自動解除鎖定至目前執行中的作業系統磁片區。

若要使用此方法，作業系統磁片區必須已受 BitLocker 磁碟機加密保護，或必須進行加密。 此外，資料磁片區必須已經存在外部金鑰。 使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 建立可自動解除鎖定磁片區的外部金鑰。

## <a name="syntax"></a>語法


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

字串，識別用來自動解除鎖定磁片區類型「外部金鑰」的金鑰保護裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                           | Description                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                           | 此方法成功。<br/>                                                                                                                                        |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>          | 磁片區已鎖定。<br/>                                                                                                                                             |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>          | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                 |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                   | *VolumeKeyProtectorID* 參數未參考「外部金鑰」類型的有效金鑰保護裝置。<br/>                                                          |
| <dl> <dt>**FVE \_E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl>       | 無法針對目前正在執行的作業系統磁片區執行此方法。<br/>                                                                                       |
| <dl> <dt>**FVE \_E \_ OS \_ 未 \_ 受保護**</dt> <dt>2150694944 (0x80310020)</dt> </dl>      | 如果目前正在執行的作業系統磁片區未受 BitLocker 磁碟機加密保護，或沒有進行中的加密，則無法執行此方法。<br/> |
| <dl> <dt> **FVE \_ E \_ 磁片 \_ \_**</dt>區系結已在 <dt>2150694943 (0x8031001F)</dt> </dl> | 先前已啟用磁片區上的自動解除鎖定。<br/>                                                                                                    |



 

## <a name="remarks"></a>備註

假設有一個類型為「外部金鑰」的有效磁片區金鑰保護裝置，則會從保護裝置解壓縮相關的256位外部金鑰，並將其儲存到目前執行中作業系統的登錄，以及磁片區金鑰保護裝置識別碼。

如果刪除與磁片區金鑰保護裝置識別碼相關聯的外部金鑰，則會停用或暫停自動解除鎖定磁片區的功能。

> [!Note]  
> 目前不支援卸載式媒體。

 

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

 

 
