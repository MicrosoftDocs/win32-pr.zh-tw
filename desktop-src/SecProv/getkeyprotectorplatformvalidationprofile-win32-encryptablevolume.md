---
description: 抓取適當類型之指定金鑰保護裝置的平臺驗證設定檔。
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Win32_EncryptableVolume 類別的 GetKeyProtectorPlatformValidationProfile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998146"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 GetKeyProtectorPlatformValidationProfile 方法 \_

**GetKeyProtectorPlatformValidationProfile** 方法會針對適當類型的指定金鑰保護裝置，抓取平臺驗證設定檔。

金鑰保護裝置識別碼必須參考「TPM」、「TPM 和 PIN」、「TPM 和 PIN 和啟動金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置。

## <a name="syntax"></a>語法


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeKeyProtectorID* \[在\]
</dt> <dd>

類型： **字串**

用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。

</dd> <dt>

*PlatformValidationProfile* \[擴展\]
</dt> <dd>

類型： **uint8 \[ \]**

整數的陣列，指定可信賴平臺模組如何 (TPM) 電腦的安全性硬體，以保護磁片區的加密金鑰。



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



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                  | Description                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                  | 此方法成功。<br/>                                                                                                                                        |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | *VolumeKeyProtectorID* 參數未參考「tpm」、「TPM 和 pin」、「TPM 和 Pin 和啟動金鑰」或「Tpm 和啟動金鑰」類型的金鑰保護裝置。<br/> |
| <dl> <dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | 磁碟區上未啟用 BitLocker。 新增金鑰保護裝置以啟用 BitLocker。<br/>                                                                                  |



 

## <a name="remarks"></a>備註

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

 

 
