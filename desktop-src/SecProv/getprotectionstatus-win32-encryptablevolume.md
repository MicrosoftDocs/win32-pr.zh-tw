---
description: 指出磁片區及其加密金鑰是否受到保護。
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Win32_EncryptableVolume 類別的 GetProtectionStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690099"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetProtectionStatus 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetProtectionStatus** 方法會指出如果有任何) 受到保護，是否 (磁片區和其加密金鑰。

如果磁片區未加密或部分加密，或磁片區的加密金鑰可在硬碟上以純文字方式提供，則會關閉保護。

## <a name="syntax"></a>語法


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtectionStatus* \[擴展\]
</dt> <dd>

類型： **uint32**

指定是否將磁片區和加密金鑰 (（如果有任何) 受到保護）。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> 未<dt><strong>受保護</strong></dt>的<dt>0</dt> </dl></td>
<td>關閉保護<br/> 針對標準 HDD：<br/> 磁片區未加密、部分加密，或磁片區的加密金鑰在硬碟上是以純文字形式提供。 如果已使用 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法停用金鑰保護裝置，或未使用下列方法指定金鑰保護裝置，則會在硬碟上以純文字方式使用加密金鑰：
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
</ul>
<br/> 針對 EHDD：<br/> 磁片區的頻外永久解除鎖定、沒有金鑰管理員，或由協力廠商金鑰管理員管理。<br/> 這也可能表示該波段是由 BitLocker 管理，但已呼叫 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法，而磁片磁碟機已被擱置。<br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <dt><strong>受保護</strong></dt>的 <dt>1</dt> </dl></td>
<td>保護<br/> 針對標準 HDD：<br/> 磁片區已完全加密，而且磁片區的加密金鑰在硬碟上無法使用。<br/> 針對 EHDD：<br/> BitLocker 是此寬線的金鑰管理員。 磁片磁碟機可以鎖定或解除鎖定，但無法永久解除鎖定。<br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt><strong>未知</strong></dt>的 <dt>2</dt> </dl></td>
<td>無法判斷磁片區保護狀態。 這可能是因為磁片區處於鎖定狀態。<br/> <strong>Windows Vista 旗艦版、Windows Vista Enterprise 和 Windows Server 2008：</strong> 不支援這個值。 從 Windows 7 和 Windows Server 2008 R2 開始支援此值。<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

只有當您先呼叫 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) ，或使用下列其中一個方法時，才可以加密磁片區：

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

因此，如果磁片已加密，而且 *ProtectionStatus* 傳回零 (保護) ，則會停用金鑰。

使用 [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) 來列出已指定用來保護磁片區加密金鑰的金鑰保護裝置。 如果金鑰保護裝置存在但保護為零 (保護) ，請使用 [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) 來開啟磁片區保護。

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

 

 
