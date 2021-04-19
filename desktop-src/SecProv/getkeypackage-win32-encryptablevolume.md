---
description: 匯出可能會在磁片磁碟機嚴重損壞且不存在資料備份檔時，協助搶救加密資料的資訊。
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Win32_EncryptableVolume 類別的 GetKeyPackage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979970"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetKeyPackage 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyPackage** 方法會匯出資訊，當磁片磁碟機嚴重損毀且沒有資料備份檔時，可能有助於搶救加密資料。

匯出的資訊包含由類型為「數位密碼」或「外部金鑰」的金鑰保護裝置所保護的磁片區加密金鑰。 若要使用此封裝，您也必須儲存對應的數值密碼或外部金鑰。

> [!IMPORTANT]
> 如果您選擇匯出金鑰封裝，請務必將這項資訊保存在妥善保護的位置。 請勿將此資訊與您的電腦搭配使用。 如果此金鑰封裝遺失或遭竊，您將需要使用新的金鑰來解密磁片區並加以重新加密。

 

當磁片磁碟機失敗時，BitLocker 修復工具有助回收可用的資料。 如需此工具如何使用金鑰封裝的詳細資訊，請參閱 [如何使用 BitLocker 修復工具協助從 Windows Vista 中的加密磁片區復原資料](https://support.microsoft.com/kb/928201)。

## <a name="syntax"></a>語法


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。 若要匯出金鑰封裝，您必須使用類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。

</dd> <dt>

*\[ KeyPackage \]*\[out\]
</dt> <dd>

類型： **uint8**

包含磁片區之加密金鑰的位元組資料流程，受指定金鑰保護裝置的保護。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                            | 此方法成功。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>           | 磁片區已鎖定。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt> </dl>    | 提供的金鑰保護裝置不存在於磁片區上。<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | *VolumeKeyProtectorID* 參數未參考類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。 您可以使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 或 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法來建立適當類型的金鑰保護裝置。<br/> |



 

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

 

 
