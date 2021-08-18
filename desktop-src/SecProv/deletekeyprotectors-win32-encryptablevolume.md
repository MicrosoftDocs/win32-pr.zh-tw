---
description: 刪除磁片區的所有金鑰保護裝置。
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Win32_EncryptableVolume 類別的 DeleteKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 49884566a45bde4977d56baa3e83ae4c42fdd676447a3da1f3df528ec823c414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004606"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 DeleteKeyProtectors 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **DeleteKeyProtectors** 方法會刪除磁片區的所有金鑰保護裝置。

如果未加密的磁片區具有金鑰保護裝置，則當 **DeleteKeyProtectors** 執行成功時，磁片區會還原成標準 NTFS 檔案系統。

如果磁片區尚未完整解密，請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再執行 **DeleteKeyProtectors** ，以確保磁片區的加密部分仍然可供存取。

## <a name="syntax"></a>語法


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                          | 描述                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                          | 此方法成功。<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>         | 磁片區已鎖定。<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_\_ \_ 需要 E 鍵**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | 如果啟用金鑰保護裝置，則無法移除部分或完整加密磁片區的最後一個金鑰保護裝置。 請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再移除此最後一個金鑰保護裝置，以確保磁片區的加密部分仍然可供存取。 <br/> |
| <dl> <dt>**FVE \_E \_ 磁片 \_ \_**</dt>區系結已在 <dt>2150694943 (0x8031001F)</dt> </dl> | 無法刪除金鑰保護裝置，因為其中一個金鑰保護裝置會用來自動解除鎖定磁片區。 <br/> 在執行此方法之前，請先使用 [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) 停用自動解除鎖定。<br/>                                                       |



 

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

 

 
