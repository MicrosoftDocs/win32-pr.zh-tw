---
description: 指出磁片區載入時是否自動解除鎖定。
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Win32_EncryptableVolume 類別的 IsAutoUnlockEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 19437bf40d27bea87103beecfbe8bee71e404c054ace46cb9728f7ac992b5c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891909"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 IsAutoUnlockEnabled 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsAutoUnlockEnabled** 方法會指出磁片區掛接時是否自動解除鎖定 (例如，卸載式記憶體裝置連接到電腦) 時。

## <a name="syntax"></a>語法


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsAutoUnlockEnabled* \[擴展\]
</dt> <dd>

類型： **布林值**

布林值，如果用來自動解除鎖定磁片區的外部金鑰存在，而且已儲存在目前正在執行的作業系統磁片區中，則為 true，否則為 false。

</dd> <dt>

*VolumeKeyProtectorID* \[擴展\]
</dt> <dd>

類型： **字串**

唯一的字串識別碼，如果 *IsAutoUnlockEnabled* 為 true，則包含相關聯的加密磁片區金鑰保護裝置識別碼。

如果 *IsAutoUnlockEnabled* 為 false，則 *VolumeKeyProtectorID* 為空字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                     | Description                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                     | 此方法成功。<br/>                                                       |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。<br/> |
| <dl> <dt>**FVE \_E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | 無法針對目前正在執行的作業系統磁片區執行此方法。<br/>      |



 

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

 

 
