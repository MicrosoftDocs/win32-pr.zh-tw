---
description: 刪除磁片區的指定金鑰保護裝置。
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Win32_EncryptableVolume 類別的 DeleteKeyProtector 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e54e857e9aafda94878b3219209ee0cda65789cd408ed115c5d0f088f7907822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668058"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 DeleteKeyProtector 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **DeleteKeyProtector** 方法會刪除磁片區的指定金鑰保護裝置。

如果未加密的磁片區具有金鑰保護裝置，則當 **DeleteKeyProtector** 移除最後一個金鑰保護裝置時，磁片區會還原成標準 NTFS 檔案系統。

如果磁片區從未經過加密，則刪除金鑰保護裝置將會還原為 NTFS。

如果磁片區尚未完整解密，請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再移除磁片區的最後一個金鑰保護裝置，以確保磁片區的加密部分仍然可供存取。

## <a name="syntax"></a>語法


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                          | 描述                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                          | 此方法成功。<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>         | 磁片區已鎖定。<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>         | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                                                                                                                                                              |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                  | *VolumeKeyProtectorID* 參數未參考有效的金鑰保護裝置。<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_\_ \_ 需要 E 鍵**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | 如果啟用金鑰保護裝置，則無法移除部分或完整加密磁片區的最後一個金鑰保護裝置。 請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再移除此最後一個金鑰保護裝置，以確保磁片區的加密部分仍然可供存取。 <br/> |
| <dl> <dt>**FVE \_E \_ 磁片 \_ \_**</dt>區系結已在 <dt>2150694943 (0x8031001F)</dt> </dl> | 無法刪除此金鑰保護裝置，因為它已用來自動解除鎖定磁片區。 <br/> 請先使用 [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) 停用自動解除鎖定，再刪除此金鑰保護裝置。<br/>                                                    |



 

## <a name="remarks"></a>備註

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

 

 
