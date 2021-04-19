---
description: 使用 Active Directory 的安全識別碼 (SID) 來保護磁片區的加密金鑰。
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Win32_EncryptableVolume 類別的 ProtectKeyWithAdSid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990350"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ProtectKeyWithAdSid 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithAdSid** 方法會使用 ACTIVE DIRECTORY 的安全識別碼 (SID) 來保護磁片區的加密金鑰。

## <a name="syntax"></a>語法


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FriendlyName* \[在中，選擇性\]
</dt> <dd>

字串，指定此金鑰保護裝置的使用者指派識別碼。 如果未指定此參數，則會使用空白值。

</dd> <dt>

*SidString* \[在\]
</dt> <dd>

包含用來保護加密金鑰之 Active Directory SID 的字串。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

變更函數行為的旗標。 這可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_DPAPI \_ NG \_ 旗標 \_ 無**</dt> <dt>0x0000</dt> </dl>                                                                   | 沒有影響。<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_DPAPI \_ NG \_ 旗標 \_ 解除鎖定 \_ 為 \_ 服務 \_ 帳戶**</dt> <dt>0x0001</dt> </dl> | 指定以 SID 為基礎的保護裝置受到服務帳戶的保護。 如果指定此旗標，呼叫端應該先確認它是以適當的服務帳戶執行，然後再藉由暫時卸載模擬來呼叫 [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (，例如) 。<br/> |



 

</dd> <dt>

*VolumeKeyProtectorID* \[擴展\]
</dt> <dd>

與建立的保護裝置相關聯的唯一識別碼。 您可以使用此字串來管理金鑰保護裝置。

如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)

根據預設，您無法從遠端新增 Active Directory 帳戶或群組保護裝置。 您必須在網域控制站和來源電腦上啟用限制委派。 在網域控制站上，執行下列步驟：

1.  開啟伺服器管理員
2.  選取 Active Directory 角色的電腦
3.  選取目標用戶端電腦，然後以滑鼠右鍵按一下
4.  選取 [委派] 索引標籤
5.  選取 [信任這台電腦，但只委派指定的服務] 選項按鈕
6.  選取 [僅使用 Kerberos] 選項按鈕
7.  按一下 [新增]
8.  選取 [使用者或電腦]
9.  選取主機/作為服務主體名稱

在來源電腦上執行步驟3到步驟9。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 企業版，僅 Windows 8 Pro \[ 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
