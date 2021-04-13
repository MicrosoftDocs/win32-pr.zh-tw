---
description: 在硬體測試之後，開始加密完整解密的作業系統磁片區。
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Win32_EncryptableVolume 類別的 EncryptAfterHardwareTest 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511158"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 EncryptAfterHardwareTest 方法 \_

在硬體測試之後， [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **EncryptAfterHardwareTest** 方法會開始加密完整解密的作業系統磁片區。 需要重新開機才能執行此硬體測試。 使用這個方法，而不是 [**加密**](encrypt-win32-encryptablevolume.md) 方法來檢查 BitLocker 是否如預期般運作。

> [!Note]  
> 如果硬碟機硬體已加密，此方法不會加密資料。 相反地，它會將寬線狀態從「永久解除鎖定」設定為解除鎖定。 如果頻外已鎖定、已解除鎖定或為唯讀，則會將磁片磁碟機視為已加密。

 

## <a name="syntax"></a>語法


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*EncryptionMethod* \[在中，選擇性\]
</dt> <dd>

類型： **uint32**

指定用來加密磁片區的加密演算法和金鑰大小。 將此參數保留空白，以使用預設值零。 如果磁片區是部分或完整加密，此參數的值必須是0，或符合磁片區的現有加密方法。 如果已使用有效的值啟用對應的群組原則設定，此參數的值必須是0或符合群組原則設定。

如果對應的群組原則設定無效，則會使用具有擴散器的預設值 AES 128。



| 值                                                                                                                                                                                                                                       | 意義                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**未指定**</dt> <dt>0</dt> </dl> | 使用目前的群組原則設定（如果有的話），否則為預設加密方法。<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 與擴散器<br/> 使用以擴散器層增強的進階加密標準 (AES) 演算法，以及使用 AES 金鑰大小128位，將磁片區加密。<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 與擴散器<br/> 使用以擴散器層增強的進階加密標準 (AES) 演算法，以及使用 AES 金鑰大小256位，將磁片區加密。<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | 使用進階加密標準 (AES) 演算法以及使用 AES 金鑰大小128位來加密磁片區。<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | 使用進階加密標準 (AES) 演算法以及使用 AES 金鑰大小256位來加密磁片區。<br/>                                                                 |



 

</dd> <dt>

*EncryptionFlags* \[在中，選擇性\]
</dt> <dd>

類型： **uint32**

描述加密行為的旗標。

**Windows 7、Windows Server 2008 R2、Windows Vista Enterprise 和 Windows Server 2008：** 此參數無法使用。

目前定義了下列位之32位的組合。



| 值                                                                                  | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | 開始新的加密程式時，以僅限資料的加密模式執行磁片區加密。 如果加密已暫停或停止，呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法會有效地繼續轉換，而且會忽略此位的值。 只有當 **Encrypt** 或 **EncryptAfterHardwareTest** 方法從完整解密的狀態、正在進行的解密或解密暫停狀態中啟動加密時，這一點才有作用。 如果這個位為零，表示未設定，則在開始新的加密程式時，將會執行完整模式轉換。<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | 執行磁片區可用空間的隨選抹除。 只有當磁片區目前未進行轉換或抹除，且處於「已加密」狀態時，才允許使用此位集呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 </dt> </dl> | 以同步方式執行要求的操作。 呼叫會封鎖，直到要求的作業完成或中斷為止。 只有 [**加密**](encrypt-win32-encryptablevolume.md) 方法支援此旗標。 當呼叫 encryption 來繼續停止或中斷加密或抹除，或正在進行加密或抹除 **時，可以** 指定此旗標。 這可讓呼叫端繼續同步等候，直到程式完成或中斷為止。<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

這個方法會立即傳回。 如果磁片區已完全加密，但未傳回任何其他錯誤，則此方法會傳回零。



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
<td>磁片區不存在任何加密金鑰。<br/> 請使用 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法來停用金鑰保護裝置，或使用下列其中一種方法來指定磁片區的金鑰保護裝置：
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E) </dt> </dl></td>
<td>因為這部電腦已設定為伺服器叢集的一部分，所以無法將磁片區加密。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B) </dt> </dl></td>
<td>找不到類型為 &quot; tpm &quot; 、 &quot; tpm 和 Pin &quot; 、 &quot; Tpm 和 pin 碼、啟動金鑰 &quot; 、 &quot; tpm 和啟動金鑰 &quot; 或 &quot; 外部金鑰 &quot; 的金鑰保護裝置。 硬體測試只牽涉到先前的金鑰保護裝置。<br/> 如果您仍想要執行硬體測試，您必須使用下列其中一種方法來指定磁片區的金鑰保護裝置：
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039) </dt> </dl></td>
<td>磁片區已部分或完整加密。<br/> 硬體測試會在進行加密之前套用。 如果您仍想要執行測試，請先使用 [ <a href="decrypt-win32-encryptablevolume.md"><strong>解密</strong></a> ] 方法，然後使用下列其中一種方法來新增金鑰保護裝置：
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028) </dt> </dl></td>
<td>磁片區是資料磁片區。<br/> 硬體測試只適用于可以啟動作業系統的磁片區。 在目前啟動的作業系統磁片區上執行此方法。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C) </dt> </dl></td>
<td>未指定類型數值密碼的金鑰保護裝置 &quot; &quot; 。 群組原則需要將修復資訊備份到 Active Directory Domain Services。 若要加入至少一個該類型的金鑰保護裝置，請使用 <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> 方法。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

當您使用這個方法時，如果沒有第二個選擇性參數 (根據 Windows 7 和 Windows Vista Enterprise 定義) ，方法一律會起始完整模式轉換，以保持回溯相容的行為。 如此一來，在 Windows 8 和 Windows Server 2012 中新增第二個選擇性參數，就不會中斷現有應用程式和腳本的安全性期望。

與 [**Encrypt**](encrypt-win32-encryptablevolume.md) 方法不同的是，此方法會執行下列動作：

-   測試 TPM 是否能夠在有 TPM 相關的金鑰保護裝置時解除鎖定磁片區。
-   測試電腦是否可以在啟動期間讀取包含外部金鑰檔案的 USB 快閃磁片磁碟機（如果磁片區將由外部金鑰解除鎖定， (包括啟動金鑰) ）。
-   需要重新開機電腦，才能執行硬體測試。
-   只有當硬體測試成功時，才開始加密。
-   無法用於資料磁片區、部分或完整加密的磁片區，或繼續加密。

執行此方法之前，請使用下列方法來建立相關的金鑰保護裝置：

-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

執行此方法之後，請採取下列額外步驟：

1.  將包含外部金鑰檔案的 USB 快閃磁片磁碟機插入電腦。 只有當磁片區具有「外部金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置時，才適用此步驟。
2.  重新啟動電腦。

電腦重新開機時，會自動執行硬體測試。

如果硬體測試成功，就會開始加密。 否則，請嘗試解決任何硬體失敗。 重新開機電腦後執行 [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) ，以取得測試結果。

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

 

 
