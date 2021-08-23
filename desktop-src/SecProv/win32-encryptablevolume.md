---
description: 針對磁片磁碟機加密或建立加密安全性軟體，您可以使用 Windows 加密軟體，BitLocker 磁碟機加密，您可以使用 Win32 \_ EncryptableVolume WMI 提供者類別來使用加密 API。
ms.assetid: 464fa664-4330-43fa-a5e0-144d1e73cf58
title: Win32_EncryptableVolume 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume
- Win32_EncryptableVolume.DeviceID
- Win32_EncryptableVolume.PersistentVolumeID
- Win32_EncryptableVolume.DriveLetter
- Win32_EncryptableVolume.ProtectionStatus
api_type:
- Schema
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3beb3498cf9e3d2873ea7dcfe3a108618eeddb513bc8207d1e819cce2fe976d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891001"
---
# <a name="win32_encryptablevolume-class"></a>Win32 \_ EncryptableVolume 類別

**Win32 \_ EncryptableVolume** WMI 提供者類別代表硬碟上的儲存區，可以使用 BitLocker 磁碟機加密來保護。 只有 NTFS 磁片區可以加密。 它可以是包含作業系統的磁片區，也可以是本機磁片上的資料磁片區。 它不能是網路磁碟機機。

若要實現 BitLocker 的優點，您必須指定磁片區加密金鑰的保護方法，然後完整加密該磁片區。

若要保護磁片區的加密金鑰，請使用下列方法來新增金鑰保護裝置：

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

每種類型的金鑰保護裝置都會提供不同的驗證體驗，以解除鎖定加密資料的存取。 外部金鑰和數值密碼可在復原案例中提供驗證。 針對以 TPM 為基礎的金鑰保護裝置，您可能必須先正確地將 TPM 初始化。 如需詳細資訊，請參閱 [**Win32 \_ Tpm**](win32-tpm.md) WMI 提供者類別。

使用 [**Encrypt**](encrypt-win32-encryptablevolume.md) 或 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法來開始加密。 在開始加密之前，必須先新增金鑰保護裝置，否則您必須使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 方法來公開未受保護的清除金鑰。 如果電腦在加密進行時關閉，加密將會在電腦重新開機時自動繼續。

您可以使用 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 和 [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) 方法來檢查可存取磁片區的狀態。

## <a name="syntax"></a>語法

``` syntax
class Win32_EncryptableVolume
{
  string DeviceID;
  string PersistentVolumeID;
  string DriveLetter;
  uint32 ProtectionStatus;
};
```

## <a name="members"></a>成員

**Win32 \_ EncryptableVolume** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ EncryptableVolume** 類別具有這些方法。



| 方法                                                                                                                   | 描述                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRecoveryInformationToActiveDirectory**](backuprecoveryinformationtoactivedirectory-win32-encryptablevolume.md) | 儲存復原至 Active Directory 所需的所有外部金鑰和相關資訊。<br/>                                                                                                                                                                       |
| [**ChangeExternalKey**](changeexternalkey-win32-encryptablevolume.md)                                                   | 變更與加密磁片區相關聯的外部金鑰。<br/>                                                                                                                                                                                                              |
| [**ChangePassphrase**](changepassphrase-win32-encryptablevolume.md)                                                     | 使用新的複雜密碼來取得新的衍生金鑰。<br/>                                                                                                                                                                                                                       |
| [**ChangePIN**](changepin-win32-encryptablevolume.md)                                                                   | 變更與加密磁片區相關聯的 PIN。<br/>                                                                                                                                                                                                                         |
| [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)                                         | 移除儲存在目前正在執行的作業系統磁片區上的所有外部金鑰和相關資訊，以用來自動解除鎖定資料磁片區。<br/>                                                                                                             |
| [**解密**](decrypt-win32-encryptablevolume.md)                                                                       | 開始解密完整加密的磁片區，或繼續解密部分加密的磁片區。<br/>                                                                                                                                                                       |
| [**DeleteKeyProtector**](deletekeyprotector-win32-encryptablevolume.md)                                                 | 刪除磁片區的指定金鑰保護裝置。<br/>                                                                                                                                                                                                                              |
| [**DeleteKeyProtectors**](deletekeyprotectors-win32-encryptablevolume.md)                                               | 刪除磁片區的所有金鑰保護裝置。<br/>                                                                                                                                                                                                                                 |
| [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md)                                                   | 移除在目前正在執行的作業系統磁片區上儲存的外部金鑰，使磁片區在掛接時不會自動解除鎖定。<br/>                                                                                                                       |
| [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)                                             | 停用與此磁片區相關聯的所有金鑰保護裝置。<br/>                                                                                                                                                                                                                   |
| [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)                                                     | 允許在掛接磁片區時自動解除鎖定資料磁片區。<br/>                                                                                                                                                                                              |
| [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)                                               | 啟用所有已停用的金鑰保護裝置。<br/>                                                                                                                                                                                                                                       |
| [**加密**](encrypt-win32-encryptablevolume.md)                                                                       | 開始加密完整解密的磁片區，或繼續加密部分加密的磁片區。<br/>                                                                                                                                                                       |
| [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md)                                     | 在硬體測試之後開始加密完整解密的磁片區。<br/>                                                                                                                                                                                                       |
| [**FindValidCertificates**](findvalidcertificates-win32-encryptablevolume.md)                                           | 列舉系統上符合指定準則的所有憑證，並傳回指紋清單。<br/>                                                                                                                                                             |
| [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md)                                               | 指出磁片區上的加密或解密狀態。<br/>                                                                                                                                                                                                        |
| [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md)                                               | 指出磁片區上所使用的加密演算法和金鑰大小。<br/>                                                                                                                                                                                                        |
| [**GetExternalKeyFileName**](getexternalkeyfilename-win32-encryptablevolume.md)                                         | 傳回包含外部索引鍵的檔案名。<br/>                                                                                                                                                                                                               |
| [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md)                                         | 從檔案傳回外部金鑰。<br/>                                                                                                                                                                                                                                      |
| [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md)                                           | 傳回硬體測試的狀態資訊。<br/>                                                                                                                                                                                                                             |
| [**GetIdentificationField**](getidentificationfield-win32-encryptablevolume.md)                                         | 傳回可用於磁片區中繼資料的識別碼字串。<br/>                                                                                                                                                                                                  |
| [**GetKeyPackage**](getkeypackage-win32-encryptablevolume.md)                                                           | 傳回信息，當磁片磁碟機嚴重損毀時，協助搶救加密的資料。<br/>                                                                                                                                                                              |
| [**GetKeyProtectorCertificate**](getkeyprotectorcertificate-win32-encryptablevolume.md)                                 | 捕獲公開金鑰保護裝置的公開金鑰和憑證指紋。<br/>                                                                                                                                                                                            |
| [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md)                                 | 抓取適當類型之指定金鑰保護裝置的外部金鑰。<br/>                                                                                                                                                                                              |
| [**GetKeyProtectorFriendlyName**](getkeyprotectorfriendlyname-win32-encryptablevolume.md)                               | 抓取用來識別指定金鑰保護裝置的顯示名稱。<br/>                                                                                                                                                                                                         |
| [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md)                     | 抓取適當類型之指定金鑰保護裝置的數值密碼。<br/>                                                                                                                                                                                        |
| [**GetKeyProtectorPlatformValidationProfile**](getkeyprotectorplatformvalidationprofile-win32-encryptablevolume.md)     | 抓取適當類型之指定金鑰保護裝置的平臺驗證設定檔。<br/>                                                                                                                                                                               |
| [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md)                                                     | 列出用來保護磁片區加密金鑰的保護裝置。<br/>                                                                                                                                                                                                           |
| [**GetKeyProtectorType**](getkeyprotectortype-win32-encryptablevolume.md)                                               | 表示指定金鑰保護裝置的類型。<br/>                                                                                                                                                                                                                               |
| [**GetLockStatus**](getlockstatus-win32-encryptablevolume.md)                                                           | 指出是否可從目前正在執行的作業系統存取磁片區的內容。<br/>                                                                                                                                                                   |
| [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md)                                               | 指出如果有任何) 受到保護，是否 (磁片區和其加密金鑰。<br/>                                                                                                                                                                                                  |
| [**GetVersion**](getversion-win32-encryptablevolume.md)                                                                 | 指出磁片區的 FVE 中繼資料版本。<br/>                                                                                                                                                                                                                          |
| [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md)                                               | 指出磁片區是否會在裝載時自動解除鎖定。<br/>                                                                                                                                                                                                       |
| [**IsAutoUnlockKeyStored**](isautounlockkeystored-win32-encryptablevolume.md)                                           | 指出目前正在執行的作業系統磁片區中是否有任何外部金鑰，以及可用來自動解除鎖定資料磁片區的相關資訊。<br/>                                                                                           |
| [**IsKeyProtectorAvailable**](iskeyprotectoravailable-win32-encryptablevolume.md)                                       | 指出磁片區是否可供磁片區使用。<br/>                                                                                                                                                                                                                 |
| [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md)                                     | 指出數值密碼是否符合特殊的格式需求。<br/>                                                                                                                                                                                            |
| [**鎖定**](lock-win32-encryptablevolume.md)                                                                             | 卸下磁片區，並從系統記憶體移除磁片區的加密金鑰。<br/>                                                                                                                                                                                           |
| [**PauseConversion**](pauseconversion-win32-encryptablevolume.md)                                                       | 暫停磁片區的加密或解密。<br/>                                                                                                                                                                                                                           |
| [**PrepareVolume**](preparevolume-win32-encryptablevolume.md)                                                           | 使用探索磁片區的指定檔案系統類型建立 BitLocker 磁片區。<br/>                                                                                                                                                                                    |
| [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)                           | 驗證所提供憑證檔案的增強金鑰使用方法 (EKU) 物件識別碼 (OID) 。<br/>                                                                                                                                                                           |
| [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)               | 驗證所提供憑證指紋的 (EKU) 物件識別碼 (OID) 的增強金鑰使用方法。<br/>                                                                                                                                                                     |
| [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)                                   | 使用256位的外部金鑰保護磁片區的加密金鑰。<br/>                                                                                                                                                                                                           |
| [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)                       | 使用特殊格式的48位數密碼來保護磁片區的加密金鑰。<br/>                                                                                                                                                                                          |
| [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)                                     | 使用複雜密碼來取得衍生金鑰。<br/>                                                                                                                                                                                                                             |
| [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)                                                   | 使用可信賴平臺模組 (電腦上的 TPM) 安全性硬體（如果有的話），以保護磁片區的加密金鑰。<br/>                                                                                                                                            |
| [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)                                       | 使用受信任的平臺模組 (TPM) 電腦上的安全性硬體（如果有的話），以使用者指定的個人識別碼（若有的話）增強磁片區的加密金鑰， (PIN) 必須在啟動時提供給電腦。<br/>                        |
| [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)             | 使用受信任的平臺模組 (TPM) 電腦上的安全性硬體（如果有的話），透過使用者指定的個人識別碼 (PIN) 以及必須在啟動時提供給電腦的外部金鑰，來保護磁片區的加密金鑰。<br/> |
| [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)                         | 使用可信賴平臺模組 (TPM) 電腦上的安全性硬體（如果有的話）來保護磁片區的加密金鑰（如果有的話），並以必須在啟動時提供給電腦的外部金鑰增強。<br/>                                                              |
| [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)                                                     | 繼續加密或解密磁片區。<br/>                                                                                                                                                                                                                          |
| [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)                                           | 將與指定之磁片區金鑰保護裝置相關聯的外部金鑰寫入至指定的檔案位置。<br/>                                                                                                                                                                   |
| [**SetIdentificationField**](setidentificationfield-win32-encryptablevolume.md)                                         | 在磁片區的中繼資料中設定指定的識別碼字串。<br/>                                                                                                                                                                                                             |
| [**UnlockWithCertificateFile**](unlockwithcertificatefile-win32-encryptablevolume.md)                                   | 使用提供的憑證檔案來取得衍生金鑰，並解除鎖定加密的磁片區。<br/>                                                                                                                                                                              |
| [**UnlockWithCertificateThumbprint**](unlockwithcertificatethumbprint-win32-encryptablevolume.md)                       | 使用提供的憑證指紋來取得衍生金鑰，並解除鎖定加密的磁片區。<br/>                                                                                                                                                                        |
| [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md)                                           | 使用提供的外部索引鍵來存取資料磁片區的內容。<br/>                                                                                                                                                                                                      |
| [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md)                               | 使用提供的數值密碼來存取資料磁片區的內容。<br/>                                                                                                                                                                                                |
| [**UnlockWithPassphrase**](unlockwithpassphrase-win32-encryptablevolume.md)                                             | 使用複雜密碼來取得衍生金鑰。 匯出衍生金鑰之後，會使用衍生金鑰來解除鎖定加密的磁片區主要金鑰。<br/>                                                                                                                   |
| [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md)                                                           | 將磁片區從 Windows Vista 格式升級為 Windows 7 格式。<br/>                                                                                                                                                                                                   |



 

### <a name="properties"></a>屬性

**Win32 \_ EncryptableVolume** 類別具有這些屬性。

<dl> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

這個系統上的磁片區唯一識別碼。 您可以使用這個來建立磁片區與其他 WMI 提供者類別（例如 **Win32 \_ 磁片** 區）的關聯。

</dd> <dt>

**DriveLetter**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

磁片區的磁碟機號。 此識別碼可以用來將磁片區與其他 WMI 提供者類別產生關聯，例如 [**Win32 \_ 磁片**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))區。

針對沒有磁碟機號的磁片區，此值為 **Null**。

</dd> <dt>

**PersistentVolumeID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個系統上的磁片區的持續性識別碼。 此識別碼是 **Win32 \_ EncryptableVolume** 專屬的。

如果磁片區是標準的完整解密 NTFS 磁片區，此識別碼會是空字串;否則，它會有唯一的值。

</dd> <dt>

**ProtectionStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

磁片區的狀態，無論 BitLocker 是否正在保護磁片區。 當具現化類別時，會儲存這個值。 保護狀態可能會在具現化和您檢查值之間變更狀態。 若要即時檢查 **ProtectionStatus** 屬性的值，請使用 [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) 方法。



| 值                                                                        | 意義                                                                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 關閉保護<br/> 磁片區未加密、部分加密，或是磁片區的磁片區加密金鑰可在硬碟上以純文字方式使用。 <br/> |
| <dl> <dt>1</dt> </dl> | 保護<br/> 磁片區已完全加密，而且磁片區的加密金鑰在硬碟上無法使用。 <br/>                          |
| <dl> <dt>2</dt> </dl> | 保護不明<br/> 無法判斷磁片區保護狀態。 其中一個可能原因是磁片區處於鎖定狀態。<br/>                          |



 

</dd> </dl>

## <a name="security-considerations"></a>安全性考量

**Win32 \_ EncryptableVolume** wmi 提供者類別依賴 WMI 命名空間安全性以及 BitLocker 磁碟機加密子系統進行存取控制。

若要使用 **Win32 \_ EncryptableVolume** 方法，必須符合下列條件：

-   您必須擁有系統管理員許可權。
-   連接加密必須能夠連接到提供者。

    如需建立加密連接的詳細資訊，請參閱 [要求命名空間的加密連接](../wmisdk/requiring-an-encrypted-connection-to-a-namespace.md)。

若要啟用遠端連線，則必須允許遠端 WMI 流量。 如需啟用 WMI 流量的詳細資訊，請參閱 [從 Vista 遠端連線至 wmi](../wmisdk/connecting-to-wmi-remotely-starting-with-vista.md)。

預設命名空間安全性設定包含預設允許編輯的專案。 如需有關 WMI 命名空間審核的詳細資訊，請參閱 [Wmi 命名空間的存取](../wmisdk/access-to-wmi-namespaces.md)。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Enterprise，僅 Windows vista 旗艦版傳統型 \[ 應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



 

 
