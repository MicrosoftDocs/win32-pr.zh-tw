---
description: 卸下磁片區，並從系統記憶體移除磁片區的加密金鑰。
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Win32_EncryptableVolume 類別的鎖定方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f5053fe027bbae51ce93feb11de5f95bde1d7b17c85a05df1386e5470b1b20fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867658"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 Lock 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **鎖定** 方法會卸載磁片區，並從系統記憶體中移除磁片區的加密金鑰。 磁片區的內容會一直變成無法存取，直到 [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) 方法或 [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) 方法解除鎖定為止。 無法針對目前正在執行的作業系統磁片區成功執行此方法。

> [!Note]  
> 如果光碟支援硬體加密，則會將此波段設定為 [已鎖定]。

 

## <a name="syntax"></a>語法


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ForceDismount* \[在中，選擇性\]
</dt> <dd>

類型： **布林值**

若 **為 true** ，則會強制卸載磁片。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                           | 描述                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                           | 此方法成功。<br/>                                                                                                                                     |
| <dl> <dt>**E \_\_拒絕存取**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | 應用程式正在存取此磁片區。 如果所有存取都是非獨佔的，則將 *ForceDismount* 參數指定為 true，可讓方法順利執行。<br/> |
| <dl> <dt>**FVE \_E \_ 未 \_ 加密**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | 磁片區已完全解密且無法鎖定。<br/>                                                                                                            |
| <dl> <dt>**FVE \_E \_ 保護 \_ 停用**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | 磁片區的加密金鑰會在磁片上以純文字方式提供，使磁片區無法鎖定。<br/>                                                    |
| <dl> <dt>**FVE \_E \_ 修復 \_ 金鑰 \_ 需要**</dt> <dt>2150694946 (0x80310022)</dt> </dl> | 磁片區沒有將磁片區解除鎖定所需之類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。<br/>                            |



 

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

 

 
