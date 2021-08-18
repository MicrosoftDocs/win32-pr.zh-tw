---
description: 指出磁片區上的加密或解密狀態。
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Win32_EncryptableVolume 類別的 GetConversionStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a93e52e0df7f4ab3fdc4c4686ee05e9c1bc9c2c3082604d922da56bc57cb94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004478"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetConversionStatus 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetConversionStatus** 方法會指出磁片區上的加密或解密狀態。

## <a name="syntax"></a>語法


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ConversionStatus* \[擴展\]
</dt> <dd>

類型： **uint32**

磁片區加密或解密狀態。 這可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | 針對標準硬碟 (HDD) ，磁片區已完全解密。<br/> 針對硬體加密硬碟 (EHDD) ，磁片區會永久解除鎖定。<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | 若為標準硬碟 (HDD) ，磁片區會完整加密。<br/> 針對硬體加密硬碟 (EHDD) ，磁片區未永久解除鎖定。<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | 磁片區已部分加密。<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | 磁片區已部分加密。<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | 磁片區已在加密進度期間暫停。 磁片區已部分加密。<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | 磁片區已在解密進度期間暫停。 磁片區已部分加密。<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[擴展\]
</dt> <dd>

類型： **uint32**

加密的磁片區百分比。 這是從0到100（含）的整數。

由於數位四捨五入，加密百分比0或100不一定表示磁片已完全解密或完全加密。 請一律使用 *ConversionStatus* 來判斷磁片是否已完全解密或完全加密。

</dd> <dt>

*EncryptionFlags* \[擴展\]
</dt> <dd>

類型： **uint32**

描述加密行為的旗標。

目前定義了下列位的32位組合。



| 值                                                                                  | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | 開始新的加密程式時，以僅限資料的加密模式執行磁片區加密。 如果加密已暫停或停止，呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法會有效地繼續轉換，而且會忽略此位的值。 只有當 **Encrypt** 或 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法從完整解密的狀態、正在進行的解密或解密暫停狀態中啟動加密時，這一點才有作用。 如果這個位為零，表示未設定，則在開始新的加密程式時，將會執行完整模式轉換。<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | 執行磁片區可用空間的隨選抹除。 只有當磁片區目前未進行轉換或抹除，且處於「已加密」狀態時，才允許使用此位集呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | 以同步方式執行要求的操作。 呼叫會封鎖，直到要求的作業完成或中斷為止。 只有 [**加密**](encrypt-win32-encryptablevolume.md) 方法支援此旗標。 當呼叫 encryption 來繼續停止或中斷加密或抹除，或正在進行加密或抹除 **時，可以** 指定此旗標。 這可讓呼叫端繼續同步等候，直到程式完成或中斷為止。<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[擴展\]
</dt> <dd>

類型： **uint32**

可用空間抹除狀態。 這可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                               | 意義                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | 尚未抹除可用空間。<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | 已抹除可用空間。<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | 正在抹除的可用空間正在進行中。<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | 已暫停釋放空間。<br/>          |



 

</dd> <dt>

*WipingPercentage* \[擴展\]
</dt> <dd>

類型： **uint32**

從0到100的值，指定已抹除的可用空間百分比。

</dd> <dt>

*PrecisionFactor* \[在\]
</dt> <dd>

類型： **uint32**

從0到4指定精確度層級的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                  | 描述                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/> |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl> | 磁片區已鎖定。<br/>      |



 

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

 

 
