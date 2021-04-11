---
description: 使用提供的數值密碼來存取資料磁片區的內容。
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Win32_EncryptableVolume 類別的 UnlockWithNumericalPassword 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847869"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 UnlockWithNumericalPassword 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithNumericalPassword** 方法會使用提供的數值密碼來存取資料磁片區的內容。

磁片區的加密金鑰必須以「數位密碼」類型的一或多個金鑰保護裝置來保護 (使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 方法) ，才能使用此方法將磁片區解除鎖定。

> [!Note]  
> 如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。

 

## <a name="syntax"></a>語法


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumericalPassword* \[在\]
</dt> <dd>

類型： **字串**

指定數位密碼的字串。

數值密碼必須包含48位數。 這些數位可以分為6位數的8個群組，每個群組中的最後一個數位指出群組的總和檢查碼值。 6位數的每個群組都必須可以整除11個，且必須小於65536。 假設有一組六位數標示為 x1、x2、x3、x4、x5 和 x6，則總和檢查碼 x6 數位的計算方式為– x1 + x2 – x3 + x4 – x5 mod 11。

您可以選擇性地以空格或連字號分隔數位群組。 因此，"xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" 或 "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" 也可能包含有效的數值密碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

如果磁片區已解除鎖定，而且沒有其他錯誤，則此方法會傳回0。



| 傳回碼/值                                                                                                                                                                             | Description                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                             | 此方法成功。<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt> </dl>     | 磁片區沒有類型為「數位密碼」的金鑰保護裝置。<br/> *NumericalPassword* 參數的格式有效，但您無法使用數值密碼來解除鎖定磁片區。<br/>           |
| <dl> <dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | *NumericalPassword* 參數無法解除鎖定磁片區。<br/> 有一或多個類型為「數位密碼」的金鑰保護裝置存在，但指定的 *NumericalPassword* 參數無法解除鎖定磁片區。<br/> |
| <dl> <dt>**FVE \_E \_ 不正確 \_ 密碼 \_ 格式**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | *NumericalPassword* 參數的格式無效。<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>備註

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

 

 
