---
description: 使用複雜密碼來取得衍生金鑰。
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Win32_EncryptableVolume 類別的 ProtectKeyWithPassphrase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966696"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ProtectKeyWithPassphrase 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithPassphrase** 方法會使用複雜密碼來取得衍生金鑰。 計算衍生金鑰之後，會使用衍生金鑰來保護加密磁片區的主要金鑰。

## <a name="syntax"></a>語法


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FriendlyName* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

字串，指定此金鑰保護裝置的使用者指派字串識別碼。 如果未指定此參數，則會使用空白值。

</dd> <dt>

複雜 *密碼* \[在\]
</dt> <dd>

類型： **字串**

指定複雜密碼的字串。

</dd> <dt>

*VolumeKeyProtectorID* \[擴展\]
</dt> <dd>

類型： **字串**

可唯一識別已建立金鑰保護裝置的字串。

如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                                        | Description                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                                        | 此方法成功。<br/>                                                                                    |
| <dl> <dt>**FVE \_E \_ 不 \_ 允許 \_ 在 \_ 安全 \_ 模式2150694976中**</dt> <dt> (0x80310040)</dt> </dl>         | 在安全模式中使用 BitLocker 磁碟機加密只能用於復原用途。<br/>                     |
| <dl> <dt>**FVE \_E \_ 原則複雜 \_ 密碼 \_ 不 \_ 允許**</dt> <dt>2150695018 (0x8031006A)</dt> </dl>     | 群組原則不允許建立複雜密碼。<br/>                                                    |
| <dl> <dt>**FVE \_E \_ FIPS \_ 可防止複雜 \_ 密碼**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>           | 需要 FIPS 合規性的群組原則設定導致無法產生或使用複雜密碼。<br/> |
| <dl> <dt>**FVE \_E \_ 原則 \_ 不正確複雜 \_ 密碼 \_ 長度**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | 提供的複雜密碼不符合最小或最大長度需求。<br/>                             |
| <dl> <dt>**FVE \_E \_ 原則 \_ \_ \_ 複雜密碼太簡單**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | 複雜密碼不符合系統管理員在群組原則中設定的複雜性需求。<br/>            |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>                       | 磁片區已被 BitLocker 磁碟機加密鎖定。 您必須從主控台解除鎖定磁片磁碟機。<br/>     |
| <dl> <dt>**FVE \_E \_ \_**</dt>重迭的更新 <dt>2150694948 (0x80310024)</dt> </dl>                   | 已由另一個執行緒更新加密磁片區的控制區塊。<br/>                                     |
| <dl> <dt>**FVE \_E \_ KEY \_ 保護裝置 \_ 不 \_ 支援**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | 目前在磁片區上的 BitLocker 磁碟機加密版本不支援金鑰保護裝置。<br/>      |
| <dl> <dt>**FVE \_\_ \_ \_ \_ 不 \_ 允許使用 E OS 磁片**</dt>區複雜密碼 <dt>2150695021 (0x8031006D)</dt> </dl> | 複雜密碼無法新增至作業系統磁片區。 <br/>                                               |
| <dl> <dt>**FVE \_E \_ 保護裝置 \_ 存在**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | 提供的金鑰保護裝置已經存在於此磁片區上。<br/>                                                     |



 

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

 

 




