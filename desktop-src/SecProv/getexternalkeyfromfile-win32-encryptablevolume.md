---
description: 從檔案傳回外部金鑰。
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Win32_EncryptableVolume 類別的 GetExternalKeyFromFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988354"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetExternalKeyFromFile 方法 \_

如果指定檔案的位置， [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetExternalKeyFromFile** 方法會從 [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)所建立的檔案傳回外部金鑰。

## <a name="syntax"></a>語法


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PathWithFileName* \[在\]
</dt> <dd>

類型： **字串**

字串，指定包含外部索引鍵之檔案的位置。

</dd> <dt>

*ExternalKey* \[擴展\]
</dt> <dd>

類型： **uint8 \[ \]**

位元組陣列，這是包含在可用來解除鎖定磁片區之檔案中的256位外部金鑰。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                   | Description                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                   | 此方法成功。<br/>                  |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | 檔案不包含外部金鑰。<br/>  |
| <dl> <dt>**錯誤 \_\_找不 \_ 到**</dt>檔案 <dt>2147942402 (0x80070002)</dt> </dl> | 在指定的位置找不到檔案。<br/> |



 

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

 

 
