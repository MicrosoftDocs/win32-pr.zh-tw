---
description: 將磁片區從 Windows Vista 格式升級為 Windows 7 格式。
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: Win32_EncryptableVolume 類別的 UpgradeVolume 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 721676b0aa135903e0e139bf719e072c3af8b6af33118f168453880fb7329413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891038"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 UpgradeVolume 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UpgradeVolume** 方法會將磁片區從 Windows Vista 格式升級為 Windows 7 格式。 這是不可反轉操作。

## <a name="syntax"></a>語法


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

如果磁片區已解除鎖定，而且沒有其他錯誤，則此方法會傳回零。



| 傳回碼/值                                                                                                                                                                  | Description                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/>                                                        |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl>            | 一或多個引數無效。<br/>                                       |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl> | 磁片區已鎖定。<br/>                                                             |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/> |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 企業版， \[ 僅 Windows 7 旗艦版桌面應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
