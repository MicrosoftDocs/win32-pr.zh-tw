---
description: 使用提供的外部索引鍵來存取資料磁片區的內容。
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Win32_EncryptableVolume 類別的 UnlockWithExternalKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a61e85608e8ed0f3e5b014d015ce7d59c4f01c8d97ab9092864fe9bb338833ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004216"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 UnlockWithExternalKey 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithExternalKey** 方法會使用提供的外部索引鍵來存取資料磁片區的內容。

您必須使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法，透過此方法將磁片區解除鎖定，才能使用類型為「外部金鑰」的一或多個金鑰保護裝置來保護磁片區的加密金鑰。

> [!Note]  
> 如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。

 

## <a name="syntax"></a>語法


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ExternalKey* \[在\]
</dt> <dd>

類型： **uint8 \[ \]**

位元組陣列，指定用來解除鎖定磁片區的256位外部金鑰。 您可以藉由呼叫 [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) 方法來取得此金鑰。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

如果磁片區已解除鎖定，這個方法會傳回0。



| 傳回碼/值                                                                                                                                                                  | 描述                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/>                                                                                                       |
| <dl> <dt>**錯誤 \_\_找不到**</dt><dt>指定的值 (0x)</dt> </dl>          | 磁片區沒有類型為「外部金鑰」的金鑰保護裝置。<br/>                                                             |
| <dl> <dt>**錯誤 \_不正確 \_ 密碼**</dt><dt>未指定任何值 (0x)</dt> </dl>   | 存在一或多個類型為「外部金鑰」的金鑰保護裝置，但指定的 *ExternalKey* 參數無法解除鎖定磁片區。<br/> |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | *ExternalKey* 參數不是大小為4的陣列。<br/>                                                                           |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/>                                                |



 

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

 

 
