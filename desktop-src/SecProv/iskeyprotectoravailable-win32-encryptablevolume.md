---
description: 指出磁片區是否可供磁片區使用。
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Win32_EncryptableVolume 類別的 IsKeyProtectorAvailable 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191256"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 IsKeyProtectorAvailable 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsKeyProtectorAvailable** 方法會指出磁片區是否有可用的保護裝置。

如果提供保護裝置類型，則此方法會指出指定類型的保護裝置是否可供磁片區使用。

## <a name="syntax"></a>語法


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*KeyProtectorType* \[在中，選擇性\]
</dt> <dd>

類型： **uint32**

不帶正負號的整數，表示所查詢之磁片區金鑰保護裝置的類型。

如果未指定此參數，則會查詢磁片區的所有可用金鑰保護裝置。



| 值                                                                         | 意義                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | 所有類型。<br/> 系統會查詢所有金鑰保護裝置。<br/> |
| <dl> <dt>1</dt> </dl>  | 信賴平臺模組 (TPM) 。<br/>                        |
| <dl> <dt>2</dt> </dl>  | 外部金鑰。<br/>                                         |
| <dl> <dt>3</dt> </dl>  | 數位密碼。<br/>                                   |
| <dl> <dt>4</dt> </dl>  | TPM 和 PIN。<br/>                                          |
| <dl> <dt>5</dt> </dl>  | TPM 和啟動金鑰。<br/>                                  |
| <dl> <dt>6</dt> </dl>  | TPM 和 PIN 和啟動金鑰。<br/>                          |
| <dl> <dt>7</dt> </dl>  | 公開金鑰。<br/>                                           |
| <dl> <dt>8</dt> </dl>  | 密碼。<br/>                                           |
| <dl> <dt>9</dt> </dl>  | TPM 憑證<br/>                                       |
| <dl> <dt>10</dt> </dl> |  (SID) 的安全識別碼<br/>                             |



 

</dd> <dt>

*IsKeyProtectorAvailable* \[擴展\]
</dt> <dd>

類型： **布林值**

布林值，指出磁片區上是否存在指定類型的磁片區金鑰保護裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                         | Description                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                         | 此方法成功。<br/>                                                                      |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl> | 已指定 *KeyProtectorType* 參數，但未參考有效的金鑰保護裝置類型。<br/> |



 

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

 

 
