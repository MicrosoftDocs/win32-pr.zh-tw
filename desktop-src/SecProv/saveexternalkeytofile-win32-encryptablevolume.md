---
description: 將與指定之磁片區金鑰保護裝置相關聯的外部金鑰寫入指定資料夾中的系統、隱藏、唯讀檔案。
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Win32_EncryptableVolume 類別的 SaveExternalKeyToFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985469"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 SaveExternalKeyToFile 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **SaveExternalKeyToFile** 方法會將與指定之磁片區金鑰保護裝置相關聯的外部金鑰，寫入指定之資料夾中的系統、隱藏的唯讀檔案。

此方法僅適用于類型為「外部金鑰」或「TPM 和啟動金鑰」的金鑰保護裝置。

## <a name="syntax"></a>語法


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> <dt>

*路徑* \[在\]
</dt> <dd>

類型： **字串**

字串，其中包含要儲存與指定金鑰保護裝置相關聯的外部金鑰之磁片區或資料夾位置。 這個路徑不包含檔案的名稱，它是內部版本，可能會從版本變更為版本。 使用 **GetExternalKeyFileName** 來取得檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                   | Description                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                   | 此方法成功。<br/>                                                                                                             |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>  | 磁片區已鎖定。<br/>                                                                                                                  |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | *VolumeKeyProtectorID* 參數未參考「外部金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置。<br/>            |
| <dl> <dt>**錯誤 \_\_找不 \_ 到路徑**</dt> <dt>2147942403 (0x80070003)</dt> </dl> | *Path* 參數未參考有效的位置。<br/> 確定檔案名未包含在 *Path* 參數中。<br/> |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                      |



 

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

 

 
