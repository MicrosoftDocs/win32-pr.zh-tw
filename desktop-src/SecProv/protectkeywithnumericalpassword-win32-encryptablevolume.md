---
description: 使用特殊格式的48位數密碼來保護磁片區的加密金鑰。
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Win32_EncryptableVolume 類別的 ProtectKeyWithNumericalPassword 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850836"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ProtectKeyWithNumericalPassword 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithNumericalPassword** 方法會使用特殊格式化的48位數密碼來保護磁片區的加密金鑰。 您可以使用此數值密碼從其他金鑰保護裝置的驗證失敗中復原 (例如 TPM) 。

為磁片區建立類型為「數位密碼」的金鑰保護裝置。

使用 [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) 方法來驗證數值密碼的格式。

## <a name="syntax"></a>語法


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FriendlyName* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

字串，指定此金鑰保護裝置的使用者指派識別碼。 如果未指定此參數，則會使用空白值。

</dd> <dt>

*NumericalPassword* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

字串，指定特殊格式化的48位數數位密碼。

數值密碼必須包含48位數。 這些數位可以分為6位數的8個群組，每個群組中的最後一個數位指出群組的總和檢查碼值。 6位數的每個群組都必須可以整除11個，且必須小於720896。 假設有一組六位數標示為 x1、x2、x3、x4、x5 和 x6，則總和檢查碼 x6 數位的計算方式為– x1 + x2 – x3 + x4 – x5 mod 11。

您可以選擇性地以空格或連字號分隔數位群組。 因此，"xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" 或 "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" 也可能包含有效的數值密碼。

如果未指定任何數值密碼，則會隨機產生一個密碼。 使用 [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) 方法來取得隨機產生的密碼。

</dd> <dt>

*VolumeKeyProtectorID* \[擴展\]
</dt> <dd>

類型： **字串**

字串，這個字串是與建立的保護裝置相關聯的唯一識別碼，可用於管理金鑰保護裝置。

如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                  | Description                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/>                                      |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | *NumericalPassword* 參數的格式無效。<br/> |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl> | 磁片區已鎖定。<br/>                                           |
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

 

 
