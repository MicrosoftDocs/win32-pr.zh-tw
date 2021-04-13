---
description: 變更與加密磁片區相關聯的 PIN。
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Win32_EncryptableVolume 類別的 ChangePIN 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511160"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ChangePIN 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ChangePIN** 方法會變更與加密磁片區相關聯的 PIN。 如果啟用 [允許啟動的增強式 Pin] 群組原則，PIN 除了數位之外，還可以包含字母、符號和空格。

## <a name="syntax"></a>語法


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> <dt>

*NewPIN* \[在\]
</dt> <dd>

類型： **字串**

使用者指定的個人識別碼字串。 如果啟用 [允許啟動的增強式 Pin] 群組原則、4到20個字母、符號、空格或數位，則此字串必須包含4到20位數的序列或。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                                | 此方法成功。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt> </dl>              | 在這部電腦上找到可開機的 CD/DVD。 移除 CD/DVD 並重新啟動電腦。<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_E \_ 不正確 \_ PIN \_ 字元**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | *NewPIN* 參數包含不正確字元。 當停用 [允許啟動的增強式 Pin] 群組原則時，只支援數位。<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>     | *VolumeKeyProtectorID* 參數未參考類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。 您可以使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 或 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法來建立適當類型的金鑰保護裝置。<br/> |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>               | 磁片區已鎖定。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>               | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_E \_ 原則 \_ 不正確 \_ PIN \_ 長度**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | 提供的 *NewPIN* 參數長度超過20個字元、少於4個字元，或小於群組原則指定的最小長度。<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt> </dl>        | 提供的金鑰保護裝置不存在於磁片區上。<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt> </dl>        | 在這部電腦上找不到相容的可信賴平臺模組 (TPM) 。<br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>備註

**ChangePIN** 方法會根據現有的保護裝置資訊和新提供的 pin 來建立新的 TPM 和 pin 保護裝置。 新的保護裝置將會有相同的 GUID。 您也可以呼叫 **ChangePIN** 方法來變更任何使用 pin 的金鑰保護裝置的 pin，例如 TPM 和 pin，或使用 PIN 和 USB 的 tpm。

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

 

 
