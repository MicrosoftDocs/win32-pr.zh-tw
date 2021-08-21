---
description: Win32_EncryptableVolume 類別的 UnlockWithPassphrase 方法-使用複雜密碼來取得衍生金鑰。
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Win32_EncryptableVolume 類別的 UnlockWithPassphrase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7b8a1ef65fd1ca3e279631a1add00ad7c07e2ff870bc24c883fd1877a3800d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004166"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 UnlockWithPassphrase 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithPassphrase** 方法會使用複雜密碼來取得衍生金鑰。 匯出衍生金鑰之後，會使用衍生金鑰來解除鎖定加密的磁片區主要金鑰。

> [!Note]  
> 如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。

 

## <a name="syntax"></a>語法


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>參數

<dl> <dt>

複雜 *密碼* \[在\]
</dt> <dd>

類型： **字串**

指定複雜密碼的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                                       | 描述                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                                       | 此方法成功。<br/>                                                                                     |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                              |
| <dl> <dt>**FVE \_E \_ FIPS \_ 可防止複雜 \_ 密碼**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | 需要 FIPS 合規性的群組原則設定導致無法產生或使用複雜密碼。 <br/> |
| <dl> <dt>**FVE \_E \_ 原則 \_ 不正確複雜 \_ 密碼 \_ 長度**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | 提供的複雜密碼不符合最小或最大長度需求。<br/>                              |
| <dl> <dt>**FVE \_E \_ 原則 \_ \_ \_ 複雜密碼太簡單**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | 複雜密碼不符合系統管理員在群組原則中設定的複雜性需求。<br/>             |
| <dl> <dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | 無法使用所提供的資訊來解除鎖定磁片區。 <br/>                                                  |
| <dl> <dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt> </dl>               | 提供的金鑰保護裝置不存在於磁片區上。 您必須輸入其他金鑰保護裝置。<br/>                 |



 

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

 

 




