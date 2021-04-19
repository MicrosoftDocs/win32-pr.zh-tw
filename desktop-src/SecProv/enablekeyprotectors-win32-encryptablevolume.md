---
description: 啟用或繼續所有已停用或已暫止的金鑰保護裝置。
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Win32_EncryptableVolume 類別的 EnableKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972831"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 EnableKeyProtectors 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **EnableKeyProtectors** 方法會啟用或繼續所有已停用或已暫止的金鑰保護裝置。 您可以使用這個方法來重新啟用或繼續加密磁片區上的 BitLocker 保護。 這個方法可確保磁片區的加密金鑰不會在硬碟上以純文字公開。

> [!Note]  
> 如果光碟支援硬體加密，頻外狀態會從「永遠解除鎖定」轉換成「已解除鎖定」。

 

## <a name="syntax"></a>語法


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

如果已啟用金鑰保護裝置，而且沒有發生其他錯誤，則此方法會傳回零。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>傳回碼/值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>S_OK</strong></dt> <dt>0 (0x0) </dt> </dl></td>
<td>此方法成功。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007) </dt> </dl></td>
<td>磁片區上不存在任何金鑰保護裝置。 使用下列其中一種方法來指定磁片區的金鑰保護裝置：<br/>
<ul>
<li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li>
<li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_ACTI加值稅ED</strong></dt> <dt>2150694920 (0x80310008) </dt> </dl></td>
<td>磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。 <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

如果磁片區已完全加密，則成功執行此方法可確保磁片區受到保護。 如果磁片區已部分加密，則成功執行此方法意味著磁片區會在完全加密時受到保護。 如需詳細資訊，請參閱 [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) 方法。

如果磁片區有以 TPM 為基礎的金鑰保護裝置，則成功執行此方法也會重新整理這些保護裝置，以便 TPM 針對平臺上的目前啟動服務進行驗證。 換句話說，您要判斷目前的電腦狀態是 TPM 在未來電腦重新開機時所要檢查的正確狀態。

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
</dt> <dt>

[**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
