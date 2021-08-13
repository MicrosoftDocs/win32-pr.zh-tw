---
description: 變更與加密磁片區相關聯的外部金鑰。
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Win32_EncryptableVolume 類別的 ChangeExternalKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3f5a8a9664c48451083808cc0e7a5f3448dbd5a87756503add896e278845421b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892895"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ChangeExternalKey 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ChangeExternalKey** 方法會變更與加密磁片區相關聯的外部金鑰。

## <a name="syntax"></a>語法


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> <dt>

 *NewExternalKey* \[在中，選擇性\]
</dt> <dd>

類型： **uint8 \[ \]**

位元組陣列，指定用來解除鎖定磁片區的256位外部金鑰。

</dd> <dt>

*NewVolumeKeyProtectorID* \[擴展\]
</dt> <dd>

類型： **字串**

更新的唯一字串識別碼，可用來管理加密的磁片區金鑰保護裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                            | 此方法成功。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                    | *NewExternalKey* 參數不是大小為32的陣列。<br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>           | 磁片區已鎖定。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt> </dl>          | 在這部電腦上找到可開機的 CD/DVD。 移除 CD/DVD 並重新啟動電腦。<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt> </dl>    | 提供的金鑰保護裝置不存在於磁片區上。<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | *VolumeKeyProtectorID* 參數未參考類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。 您可以使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 或 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法來建立適當類型的金鑰保護裝置。<br/> |



 

## <a name="remarks"></a>備註

這個方法可以用來變更使用外部金鑰之任何金鑰保護裝置的外部金鑰。

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

 

 




