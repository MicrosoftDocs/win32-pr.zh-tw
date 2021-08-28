---
description: 使用提供的 Active Directory 安全識別碼 (SID) 字串來取得衍生金鑰，並解除鎖定加密的磁片區。
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Win32_EncryptableVolume 類別的 UnlockWithAdSid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 14aaa82ff4b17b551ba595d2ea0c33737d651ca0236448d1d089caa82bd5f841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891383"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 UnlockWithAdSid 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithAdSid** 方法會使用提供的 Active Directory 安全識別碼 (SID) 字串來取得衍生金鑰，並解除鎖定加密的磁片區。

> [!Note]  
> 如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。

 

## <a name="syntax"></a>語法


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SidString* \[在\]
</dt> <dd>

包含 Active Directory SID 的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 企業版， \[ 僅 Windows 8 專業版桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
