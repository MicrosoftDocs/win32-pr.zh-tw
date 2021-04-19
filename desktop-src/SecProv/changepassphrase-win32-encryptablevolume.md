---
description: 使用新的複雜密碼來取得新的衍生金鑰。
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Win32_EncryptableVolume 類別的 ChangePassphrase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988927"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ChangePassphrase 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ChangePassphrase** 方法會使用新的複雜密碼來取得新的衍生金鑰。 計算衍生金鑰之後，會使用新的衍生金鑰來保護加密磁片區的主要金鑰。

## <a name="syntax"></a>語法


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> <dt>

*NewPassphrase* \[在\]
</dt> <dd>

類型： **字串**

指定複雜密碼的更新字串。

</dd> <dt>

*NewProtectorID* \[擴展\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的更新唯一字串識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                                       | Description                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                                       | 此方法成功。<br/>                                                                                  |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>                      | 磁片區已被 BitLocker 磁碟機加密鎖定。 您必須從主控台解除鎖定磁片磁碟機。<br/>   |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                           |
| <dl> <dt>**FVE \_E \_ \_**</dt>重迭的更新 <dt>2150694948 (0x80310024)</dt> </dl>                  | 已由另一個執行緒更新加密磁片區的控制區塊。<br/>                                   |
| <dl> <dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>            | 指定的金鑰保護裝置不是正確的類型。 <br/>                                                    |
| <dl> <dt>**FVE \_E \_ 原則 \_ 不正確複雜 \_ 密碼 \_ 長度**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | 提供的更新複雜密碼不符合最小或最大長度需求。 <br/>                  |
| <dl> <dt>**FVE \_E \_ 原則 \_ \_ \_ 複雜密碼太簡單**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | 更新的複雜密碼不符合系統管理員在群組原則中設定的複雜性需求。 <br/> |



 

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

 

 




