---
description: 停用或暫停與此磁片區相關聯的所有金鑰保護裝置。
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Win32_EncryptableVolume 類別的 DisableKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 79b9db0043e04d3ab6399677a9e103961d5f1a9b5c5214558bcf53359bedc61a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892537"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 DisableKeyProtectors 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **DisableKeyProtectors** 方法會停用或暫停與此磁片區相關聯的所有金鑰保護裝置。

## <a name="syntax"></a>語法


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DisableCount* \[在中，選擇性\]
</dt> <dd>

類型： **uint32**

整數，指定將停用金鑰保護裝置的重新開機次數。 此參數僅適用于 OS 磁片區。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                  | Description                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/> |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl> | 磁片區已鎖定。<br/>      |



 

## <a name="security-considerations"></a>安全性考量

這個方法會在硬碟上以純文字公開磁片區的加密金鑰，並關閉任何磁片區保護。 我們建議您不要以純文字格式輸入任何密碼或加密金鑰。

## <a name="remarks"></a>備註

即使已停用或暫停金鑰保護裝置，也可以新增金鑰保護裝置。 除非呼叫 [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) ，否則這些金鑰保護裝置將維持停用狀態。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
