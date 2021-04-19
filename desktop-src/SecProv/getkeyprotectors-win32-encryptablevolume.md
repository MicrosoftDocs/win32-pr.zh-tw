---
description: 列出用來保護磁片區加密金鑰的保護裝置。
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Win32_EncryptableVolume 類別的 GetKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970151"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetKeyProtectors 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectors** 方法會列出用來保護磁片區加密金鑰的保護裝置。 如果提供保護裝置類型，則只會傳回指定類型的磁片區金鑰保護裝置。

## <a name="syntax"></a>語法


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*KeyProtectorType* \[在中，選擇性\]
</dt> <dd>

類型： **uint32**

不帶正負號的整數，指定要傳回的金鑰保護裝置類型。

如果未指定此參數，則會傳回磁片區的所有可用金鑰保護裝置。



| 值                                                                         | 意義                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | 所有類型。<br/> 系統會傳回所有金鑰保護裝置。<br/> |
| <dl> <dt>1</dt> </dl>  | 信賴平臺模組 (TPM) 。<br/>                         |
| <dl> <dt>2</dt> </dl>  | 外部金鑰。<br/>                                          |
| <dl> <dt>3</dt> </dl>  | 數值密碼。<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM 和 PIN。<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM 和啟動金鑰。<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM 和 PIN 和啟動金鑰。<br/>                           |
| <dl> <dt>7</dt> </dl>  | 公開金鑰。<br/>                                            |
| <dl> <dt>8</dt> </dl>  | 密碼。<br/>                                            |
| <dl> <dt>9</dt> </dl>  | TPM 憑證<br/>                                        |
| <dl> <dt>10</dt> </dl> |  (SID) 的安全識別碼<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[擴展\]
</dt> <dd>

類型：**字串 \[ \]**

字串陣列，識別用來保護磁片區加密金鑰的金鑰保護裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                  | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/>                                                                          |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | 已指定 *VolumeKeyProtectorID* 參數，但未參考有效的 *KeyProtectorType*。<br/> |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                   |



 

## <a name="remarks"></a>備註

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

 

 
