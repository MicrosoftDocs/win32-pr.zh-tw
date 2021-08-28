---
description: 指出磁片區上所使用的加密演算法和金鑰大小。
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Win32_EncryptableVolume 類別的 GetEncryptionMethod 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f9f4a2ad20af7c5ee3ba3afd8e2d9e56d0720b38d7afc2b01042e440cc85bf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892446"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetEncryptionMethod 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetEncryptionMethod** 方法會指出磁片區上所使用的加密演算法和金鑰大小。

## <a name="syntax"></a>語法


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*EncryptionMethod* \[擴展\]
</dt> <dd>

類型： **uint32**

不帶正負號的整數，指定磁片區上所使用的加密演算法和金鑰大小。



| 值                                                                                                                                                                                                                                          | 意義                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**無**</dt> <dt>0</dt> </dl>                                | 磁片區未加密。<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ 與 \_ 擴散**</dt>器 <dt>1</dt> </dl> | 磁片區已完全或部分加密，使用以擴散器層增強的進階加密標準 (AES) 演算法（使用 AES 金鑰大小128位）。 在執行 Windows 8.1 或更高版本的裝置上，將無法再使用這個方法。<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ 與 \_ 擴散**</dt>器 <dt>2</dt> </dl> | 磁片區已完全或部分加密，使用以擴散器層增強的進階加密標準 (AES) 演算法（使用 AES 金鑰大小256位）。 在執行 Windows 8.1 或更高版本的裝置上，將無法再使用這個方法。<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | 磁片區已使用進階加密標準 (AES) 演算法完整或部分加密，使用 AES 金鑰大小128位。<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | 磁片區已使用進階加密標準 (AES) 演算法完整或部分加密，使用 AES 金鑰大小256位。<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**硬體 \_加密**</dt> <dt>5</dt> </dl>         | 磁片區已使用磁片磁碟機的硬體功能完全或部分加密。<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_AES \_ 128**</dt> <dt>6</dt> </dl>                                | 磁片區已使用進階加密標準 (AES) 和 AES 金鑰大小128位，以完整或部分加密的方式使用 XTS。 此方法僅適用于執行 Windows 10 1511 或更高版本的裝置。<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_AES \_ 256**</dt> <dt>7</dt> </dl>                                | 磁片區已使用進階加密標準 (AES) 和 AES 金鑰大小256位，以完整或部分加密的方式使用 XTS。 此方法僅適用于執行 Windows 10 1511 或更高版本的裝置。<br/>                          |
| <dl> <dt> (uint32) –1</dt> </dl>                                                                                                                                                          | UNKNOWN<br/> 磁片區已完全或部分加密，但有未知的演算法和金鑰大小。<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[擴展\]
</dt> <dd>

類型： **字串**

加密演算法是在自我加密磁片磁碟機上設定的。 Null 字串表示 BitLocker 正在使用軟體加密，或未報告任何加密方法。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

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

 

 
