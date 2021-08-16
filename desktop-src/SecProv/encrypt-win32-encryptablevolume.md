---
description: 開始加密完整解密的磁片區，或繼續加密部分加密的磁片區。
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Win32_EncryptableVolume 類別的 Encrypt 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e6e2ed0eea4bb9c70949a3916733bf2777397fcb509ba0ce2f91633bf15a74d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892466"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 Encrypt 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **Encrypt** 方法會開始加密完整解密的磁片區，或繼續加密部分加密的磁片區。 當加密暫停或進行中時，此方法的行為與 [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)相同。 當解密暫停或進行中時，此方法會停止解密並開始加密。

> [!Note]  
> 如果磁片磁碟機已加密硬體，這個方法不會加密資料。 相反地，它會將頻外狀態從 [永遠解除鎖定] 設定為 [已解除鎖定]。 如果頻外已鎖定、已解除鎖定或為唯讀，則會將磁片磁碟機視為已加密。

 

**Windows Vista：** 不支援加密非目前執行中作業系統磁片區的磁片區。

## <a name="syntax"></a>語法


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*EncryptionMethod* \[在中，選擇性\]
</dt> <dd>

類型： **uint32**

不帶正負號的整數，指定用來加密磁片區的加密演算法和金鑰大小。 如果此參數大於零，且磁片區為部分或完整加密，則 *EncryptionMethod* 必須符合磁片區的現有加密方法。 如果此參數大於零，且對應的群組原則設定是以有效的值啟用， *EncryptionMethod* 必須符合群組原則設定。

如需可能 EncryptionMethod 值的清單，請參閱 [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) 方法。

Windows 7 或以下的預設值為： 1 (AES \_ 128 \_ （具有 \_ 擴散器) ）。

Windows 8、Windows 8.1 或 1507 Windows 10 的預設值為： 3 (AES \_ 128) 。

Windows 10 1511 版或更新版本的預設值為： 6 (XTS \_ AES \_ 128) 。

</dd> <dt>

*EncryptionFlags* \[在中，選擇性\]
</dt> <dd>

類型： **uint32**

描述加密行為的旗標。

**Windows 7、Windows server 2008 R2、Windows Vista Enterprise 和 Windows Server 2008：** 此參數無法使用。

目前定義了下列位的32位組合。



| 值                                                                                  | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | 開始新的加密程式時，以僅限資料的加密模式執行磁片區加密。 如果加密已暫停或停止，呼叫 **加密** 方法會有效地繼續轉換，而且會忽略此位的值。 只有當 **Encrypt** 或 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法從完整解密的狀態、正在進行的解密或解密暫停狀態中啟動加密時，這一點才有作用。 如果這個位為零，表示未設定，則在開始新的加密程式時，將會執行完整模式轉換。<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | 執行磁片區可用空間的隨選抹除。 只有當磁片區目前未進行轉換或抹除，且處於「已加密」狀態時，才允許使用此位集呼叫 **加密** 方法。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | 以同步方式執行要求的操作。 呼叫會封鎖，直到要求的作業完成或中斷為止。 只有 **加密** 方法支援此旗標。 當呼叫 encryption 來繼續停止或中斷加密或抹除，或正在進行加密或抹除 **時，可以** 指定此旗標。 這可讓呼叫端繼續同步等候，直到程式完成或中斷為止。<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

這個方法會立即傳回。 如果磁片區已完全加密，但未傳回任何其他錯誤，則此方法會傳回0。



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
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057) </dt> </dl></td>
<td>已提供 <em>EncryptionMethod</em> 參數，但不在已知範圍內，或不符合目前的群組原則設定。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E) </dt> </dl></td>
<td>磁片區不存在任何加密金鑰。 使用 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法來停用金鑰保護裝置，或使用下列其中一種方法來指定磁片區的金鑰保護裝置：<br/>
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<strong>Windows Vista：</strong>當磁片區不存在任何加密金鑰時，會改為傳回 ERROR_INVALID_OPERATION。 十進位值是4317，而十六進位值為0x10DD。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D) </dt> </dl></td>
<td>提供的加密方法與部分或完整加密磁片區的加密方法不相符。 若要繼續加密，請將 <em>EncryptionMethod</em> 參數保留空白或使用零值。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E) </dt> </dl></td>
<td>因為這部電腦已設定為伺服器叢集的一部分，所以無法將磁片區加密。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000) </dt> </dl></td>
<td>磁片區已鎖定。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C) </dt> </dl></td>
<td>未指定類型數值密碼的金鑰保護裝置 &quot; &quot; 。 群組原則需要將修復資訊備份到 Active Directory Domain Services。 若要加入至少一個該類型的金鑰保護裝置，請使用 <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> 方法。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

當您使用這個方法時，如果沒有第二個選擇性參數 (根據 Windows 7 和 Windows Vista Enterprise 定義) ，此方法一律會起始完整模式轉換，以維持回溯相容的行為。 如此一來，現有應用程式和腳本的安全性期望將不會在 Windows 8 和 Windows Server 2012 中新增第二個選擇性參數的情況下中斷。

您可以呼叫 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 來判斷加密是否正在進行中，以及已加密之磁片區的百分比。

當磁片區完整加密，且已新增並啟用金鑰保護裝置時，磁片區的保護狀態會變更為「開啟」。

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

 

 
