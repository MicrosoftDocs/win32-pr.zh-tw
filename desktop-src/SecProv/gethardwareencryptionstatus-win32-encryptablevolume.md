---
description: 判斷磁片區是否位於支援或可支援硬體加密的磁片磁碟機上。
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Win32_EncryptableVolume 類別的 GetHardwareEncryptionStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 434c074260a07a251ac81148616c434cb9f7de74d799a42c71bd81451a1bd3b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667998"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetHardwareEncryptionStatus 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetHardwareEncryptionStatus** 方法會判斷磁片區是否位於支援或可支援硬體加密的磁片磁碟機上。

## <a name="syntax"></a>語法


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*HardwareEncryptionStatus* \[擴展\]
</dt> <dd>

指定磁片磁碟機是否可以支援硬體加密。 這可以是下列其中一個值。



| 值                                                                                                                                                                                                                                               | 意義                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**不支援**</dt> <dt>0</dt> </dl> | 不支援硬體加密。<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**無保護措施**</dt> <dt>1</dt> </dl> | 不支援磁片磁碟機加密。<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**使用軟體**</dt> <dt>2</dt> </dl> | 加密方法是以軟體為基礎。<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**使用硬體**</dt> <dt>3</dt> </dl> | 磁片磁碟機支援硬體加密。<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果磁片區與 BitLocker 硬體加密相容，則此函式會傳回零 (0) 。 否則，函數會傳回錯誤。



| 傳回碼/值                                                                                                                                 | 描述                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 磁片區與 BitLocker 硬體加密相容。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 企業版， \[ 僅 Windows 8 專業版桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




