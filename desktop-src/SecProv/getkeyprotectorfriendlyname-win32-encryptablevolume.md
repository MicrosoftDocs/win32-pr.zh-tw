---
description: 抓取用來識別指定金鑰保護裝置的顯示名稱。
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Win32_EncryptableVolume 類別的 GetKeyProtectorFriendlyName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f319d555396efdf46d3511a9ca0a3088de8d4a48d032da01415c0d6fee0bcdf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892034"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetKeyProtectorFriendlyName 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorFriendlyName** 方法會抓取用來識別指定金鑰保護裝置的顯示名稱。

## <a name="syntax"></a>語法


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> <dt>

*FriendlyName* \[擴展\]
</dt> <dd>

類型： **字串**

字串，其中包含使用者指定的名稱，用來識別指定的金鑰保護裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                  | Description                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/>                                                        |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | *VolumeKeyProtectorID* 參數未參考有效的金鑰保護裝置。<br/>     |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/> |



 

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

 

 
