---
description: 暫停磁片區的加密或解密。
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Win32_EncryptableVolume 類別的 PauseConversion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975374"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 PauseConversion 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **PauseConversion** 方法會暫停磁片區的加密或解密。

> [!Note]  
> 如果光碟支援硬體加密，此函式可以暫停抹除操作，但無法暫停以硬體為基礎的加密。

 

## <a name="syntax"></a>語法


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

如果此方法用於完整加密或完整解密的磁片區，或磁片區上已暫停加密/解密，則會傳回0，假設沒有其他錯誤發生。



| 傳回碼/值                                                                                                                                                                  | Description                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/> |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl> | 磁片區已鎖定。<br/>      |



 

## <a name="remarks"></a>備註

如果在進行加密/解密的磁片區上使用此方法，成功執行此方法會導致 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 指出加密或解密已暫停。

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

 

 
