---
description: 抓取 BitLocker 已暫止的次數。
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: 'Win32_EncryptableVolume 類別的 GetSuspendCount 方法 (Activdbg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983813"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetSuspendCount 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetSuspendCount** 方法會先抓取重新開機次數，然後才會自動繼續執行保護。

## <a name="syntax"></a>語法


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SuspendCount* 
</dt> <dd>

從0到15的整數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼                                                                                          | Description                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                 | 此方法成功。<br/>                                      |
| <dl> <dt>**\_不 \_ 支援的錯誤**</dt> </dl> | 如果磁片區未暫停或不是 OS 磁片區，則傳回。<br/> |



 

## <a name="remarks"></a>備註

此方法僅適用于 OS 磁片區，而且只有在該磁片區實際暫停時才會套用。 如果磁片區未暫停或不是 OS 磁片區，則會傳回 **\_ 不 \_ 支援的錯誤** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 企業版，僅 Windows 8 Pro \[ 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| 標頭<br/>                   | <dl> <dt>Activdbg。h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




