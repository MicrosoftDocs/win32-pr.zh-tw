---
description: 如果可信賴平臺模組 (TPM) 可供使用，這個方法會保護由外部金鑰增強的磁片區加密金鑰。
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Win32_EncryptableVolume 類別的 ProtectKeyWithTPMAndStartupKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973622"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 ProtectKeyWithTPMAndStartupKey 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithTPMAndStartupKey** 方法會使用可信賴平臺模組 (TPM) 電腦上的安全性硬體（如果有的話）來保護磁片區的加密金鑰（如果有的話），並以必須在啟動時向電腦呈現的外部金鑰增強。

您必須透過 TPM 驗證以及包含外部金鑰的 USB 記憶體裝置輸入，才能存取磁片區的加密金鑰，並將磁片區內容解除鎖定。 使用 [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) 方法，將此外部金鑰儲存至 USB 記憶體裝置上的檔案，以做為啟動金鑰使用。

這個方法僅適用于包含目前正在執行之作業系統的磁片區。

如果磁片區不存在，就會為磁片區建立類型為「TPM 和啟動金鑰」的金鑰保護裝置。

## <a name="syntax"></a>語法


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FriendlyName* \[在中，選擇性\]
</dt> <dd>

類型： **字串**

使用者指派給此金鑰保護裝置的字串識別碼。 如果未指定此參數，則會使用空白值。

</dd> <dt>

*PlatformValidationProfile* \[在中，選擇性\]
</dt> <dd>

類型： **uint8 \[ \]**

整數陣列，指定電腦的信賴平臺模組 (TPM) 安全性硬體如何保護磁片區的加密金鑰。

平臺驗證設定檔包含一組平臺設定暫存器 (PCR) 索引，範圍從0到23（含）。 參數中的重複值會被忽略。 每個 PCR 索引都會與作業系統啟動時執行的服務相關聯。 每次電腦啟動時，TPM 都會檢查您在平臺驗證設定檔中指定的服務是否未變更。 如果其中任何一項服務在 BitLocker 磁碟機加密)  (的情況下變更，則 TPM 不會釋出加密金鑰來解除鎖定磁片區，而且電腦會進入修復模式。

如果指定了這個參數，但已啟用對應的群組原則設定，它就必須符合群組原則設定。

如果未指定此參數，則會使用預設值0、2、4、5、8、9、10和11。 預設的平臺驗證設定檔會針對下列元素的變更保護加密金鑰：

-   度量 (的核心根信任 CRTM) 
-   BIOS
-    (PCR 0) 的平臺擴充
-   選項 ROM 代碼 (PCR 2) 
-   主開機記錄 (MBR) 代碼 (PCR 4) 
-   主開機記錄 (MBR) 磁碟分割表格 (PCR 5) 
-    (PCR 8) 的 NTFS 開機磁區
-   NTFS 開機區塊 (PCR 9) 
-   開機管理程式 (PCR 10) 
-   BitLocker 存取控制 (PCR 11) 

針對電腦的安全性，建議預設設定檔。 若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。 整合可延伸韌體介面 (UEFI) 型電腦預設不會使用 PCR 5。

變更預設設定檔會影響電腦的安全性與管理性。 BitLocker 對平臺修改的機密性 (惡意或授權的) 會隨著 PCRs 的包含或排除而增加或減少。 若要啟用 BitLocker 保護，平臺驗證設定檔必須包含 PCR 11。



| 值                                                                         | 意義                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  |  (CRTM) 、BIOS 和平臺擴充的測量核心根信任<br/> |
| <dl> <dt>1</dt> </dl>  | 平臺和主機板設定和資料<br/>                         |
| <dl> <dt>2</dt> </dl>  | 選項 ROM 代碼<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | 選項 ROM 設定和資料<br/>                                       |
| <dl> <dt>4</dt> </dl>  | 主開機記錄 (MBR) 碼<br/>                                           |
| <dl> <dt>5</dt> </dl>  | 主開機記錄 (MBR) 磁碟分割資料表<br/>                                |
| <dl> <dt>6</dt> </dl>  | 狀態轉換和喚醒事件<br/>                                        |
| <dl> <dt>7</dt> </dl>  | 電腦 Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | NTFS 開機磁區<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | NTFS 開機區塊<br/>                                                         |
| <dl> <dt>10</dt> </dl> | 開機管理程式<br/>                                                            |
| <dl> <dt>11</dt> </dl> | BitLocker 存取控制<br/>                                                |
| <dl> <dt>12</dt> </dl> | 定義供靜態作業系統使用<br/>                          |
| <dl> <dt>13</dt> </dl> | 定義供靜態作業系統使用<br/>                          |
| <dl> <dt>14</dt> </dl> | 定義供靜態作業系統使用<br/>                          |
| <dl> <dt>15</dt> </dl> | 定義供靜態作業系統使用<br/>                          |
| <dl> <dt>16</dt> </dl> | 用於偵錯工具<br/>                                                      |
| <dl> <dt>17</dt> </dl> | 動態 CRTM<br/>                                                            |
| <dl> <dt>達</dt> </dl> | 已定義平臺<br/>                                                        |
| <dl> <dt>診斷</dt> </dl> | 由受信任的作業系統使用<br/>                                      |
| <dl> <dt>20</dt> </dl> | 由受信任的作業系統使用<br/>                                      |
| <dl> <dt>21</dt> </dl> | 由受信任的作業系統使用<br/>                                      |
| <dl> <dt>22</dt> </dl> | 由受信任的作業系統使用<br/>                                      |
| <dl> <dt>23</dt> </dl> | 應用程式支援<br/>                                                     |



 

</dd> <dt>

*ExternalKey* \[在中，選擇性\]
</dt> <dd>

類型： **uint8 \[ \]**

位元組陣列，指定當電腦啟動時，用來解除鎖定磁片區的256位外部金鑰。

如果未指定外部索引鍵，則會隨機產生一個索引鍵。 使用 [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) 方法來取得隨機產生的金鑰。

</dd> <dt>

*VolumeKeyProtectorID* \[擴展\]
</dt> <dd>

類型： **字串**

字串，這個字串是與建立的金鑰保護裝置相關聯的唯一識別碼，可用於管理金鑰保護裝置。

如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                         | Description                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                         | 此方法成功。<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt> </dl>        | 磁片區已鎖定。<br/>                                                                                                                                                                                                                                       |
| <dl> <dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt> </dl> | 在這部電腦上找不到相容的 TPM。<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt> </dl>       | TPM 無法保護磁片區的加密金鑰，因為磁片區未包含目前執行中的作業系統。<br/>                                                                                                                               |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | 已提供 *PlatformValidationProfile* 參數，但其值不在已知範圍內，或者不符合目前作用中的群組原則設定。<br/> 提供 *ExternalKey* 參數，但不是大小為32的陣列。<br/> |
| <dl> <dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt> </dl>       | 在這部電腦上找到可開機的 CD/DVD。 移除 CD/DVD 並重新啟動電腦。<br/>                                                                                                                                                                    |
| <dl> <dt>**FVE \_E \_ 保護裝置 \_ 存在**</dt> <dt>2150694961 (0x80310031)</dt> </dl>     | 此類型的金鑰保護裝置已經存在。<br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a>安全性考量

針對電腦的安全性，建議預設設定檔。 若要針對早期啟動程式碼變更進行額外的保護，請使用 PCRs 0、2、4、5、8、9、10和11的設定檔。 若要針對早期啟動設定變更進行額外的保護，請使用 PCRs 0、1、2、3、4、5、8、9、10、11的設定檔。

變更預設設定檔會影響您電腦的安全性或可用性。

## <a name="remarks"></a>備註

磁片區最多隻能有一個類型為「TPM 和啟動金鑰」的金鑰保護裝置。 如果您想要變更現有「TPM plus 啟動金鑰」金鑰保護裝置所使用的顯示名稱或平臺驗證設定檔，您必須先移除現有的金鑰保護裝置，然後呼叫 **ProtectKeyWithTPMAndStartupKey** 來建立新的金鑰保護裝置。 您應指定額外的金鑰保護裝置，以在無法取得存取磁片區加密金鑰的復原案例中解除鎖定磁片區;例如，當 TPM 無法成功驗證平臺驗證設定檔，或包含外部金鑰的 USB 記憶體遺失時。

使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 或 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 來建立一或多個金鑰保護裝置，以復原其他鎖定的磁片區。

雖然可以同時有類型為 "TPM" 的金鑰保護裝置，以及另一種類型為「TPM 和啟動金鑰」的金鑰保護裝置，但「TPM」金鑰保護裝置類型的存在會使其他以 TPM 為基礎的金鑰保護裝置產生的影響不會影響。

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

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
