---
description: 指出 TPM 是否已就緒，並提供 TPM 狀態的其他相關資訊。
ms.assetid: 1E348D77-979C-42FC-824D-7C57F7BAABE5
title: Win32_Tpm：： IsReadyInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReadyInformation
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 319152da3604044500c107520cf1afd1d04e16fc2c7f54f0ecebf7b49d81f0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890835"
---
# <a name="win32_tpmisreadyinformation-method"></a>Win32 \_ Tpm：： IsReadyInformation 方法

指出 TPM 是否已就緒，並提供 TPM 狀態的其他相關資訊。 Information 參數會傳回完整布建 TPM 所需之資訊的位元遮罩。

只有本機系統管理員才能存取此方法。

## <a name="syntax"></a>語法


```C++
uint32 IsReadyInformation(
  [out] BOOL   IsReady,
  [out] uint32 Information
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsReady* \[擴展\]
</dt> <dd>

如果 TPM 和系統已完全布建以供 TPM 使用，則設定為 **TRUE** 。

</dd> <dt>

*資訊* \[擴展\]
</dt> <dd>

傳回完整布建 TPM 所需內容的最多可用資訊的位元遮罩。

*資訊* 參數可能包含下列值。



| 值                                                                                                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**資訊 \_關機**</dt> <dt>0x00000002</dt> </dl>                                                 | 需要重新開機平臺 (關機) 。<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**資訊 \_重新開機**</dt> <dt>0x00000004</dt> </dl>                                                       | 需要重新開機平臺 (重新開機) 。<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**資訊 \_TPM \_ 強制 \_ 清除**</dt> <dt>0x00000008</dt> </dl>                          | TPM 已經擁有。 必須清除 TPM，或需要匯入 TPM 擁有者授權值。<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**資訊 \_實體 \_ 狀態**</dt>的 <dt>0x00000010</dt> </dl>                     | 布建 TPM 需要實體存在。<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**資訊 \_TPM \_ 啟動**</dt> <dt>0x00000020</dt> </dl>                                    | TPM 已停用或停用。<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**資訊 \_TPM \_ 取得 \_ 擁有權**</dt> <dt>0x00000040</dt> </dl>                 | 已取得 TPM 擁有權。<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**資訊 \_TPM \_ 建立 \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | TPM 中有 (EK) 的簽署金鑰。 <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**資訊 \_TPM \_ OWNERAUTH**</dt> <dt>0x00000100</dt> </dl>                                 | TPM 擁有者授權未正確儲存在登錄中。<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**資訊 \_TPM \_ SRK \_ 驗證**</dt> <dt>0x00000200</dt> </dl>                                  |  (SRK) 授權值的儲存體根金鑰並非全部為零。<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**資訊 \_TPM \_ 停用 \_ 擁有者 \_ 清除**</dt> <dt>0x00000400</dt> </dl> | 如果作業系統設定為停用 tpm 擁有者授權值的 TPM 清除，但 TPM 尚未設定為防止以 TPM 擁有者授權值清除 TPM。<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**資訊 \_TPM \_ SRKPUB**</dt> <dt>0x00000800</dt> </dl>                                          | 作業系統與 TPM 儲存體根金鑰相關的登錄資訊，與 TPM 儲存體根金鑰不符。<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**資訊 \_TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt> </dl>                          | TPM 永久旗標允許讀取儲存體根金鑰公用值未設定。<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**資訊 \_TPM \_ 開機 \_ 計數器**</dt> <dt>0x00002000</dt> </dl>                       | 未建立開機期間遞增的單純計數器。<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**資訊 \_TPM \_ AD \_ 備份**</dt> <dt>0x00004000</dt> </dl>                                | TPM 的擁有者授權尚未備份至 Active Directory。<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**資訊 \_TPM \_ AD \_ 備份 \_ 階段 \_ I**</dt> <dt>0x00008000</dt> </dl>      | Active Directory 中 TPM 擁有者授權資訊儲存區的第一個部分正在進行中。<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**資訊 \_TPM \_ AD \_ 備份 \_ 第 \_ 二階段**</dt> <dt>0x00010000</dt> </dl>   | Active Directory 中 TPM 擁有者授權資訊儲存的第二個部分正在進行中。<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**資訊 \_舊版 \_**</dt>設定 <dt>0x00020000</dt> </dl>            | Windows群組原則設定為不儲存任何 TPM 擁有者授權，因此 TPM 無法完全就緒。<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**資訊 \_EK \_ 憑證**</dt> <dt>0x00040000</dt> </dl>                              | 未從 TPM NV Ram 讀取 EK 憑證，並將其儲存在登錄中。 <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**資訊 \_TCG \_ 事件 \_ 記錄**</dt>檔 <dt>0x00080000</dt> </dl>                                | TCG 事件記錄檔是空的或無法讀取。 <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**資訊 \_未 \_ 減少**</dt> <dt>0x00100000</dt> </dl>                                       | 未擁有 TPM。<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**資訊 \_一般 \_ 錯誤**</dt> <dt>0x00200000</dt> </dl>                                 | 發生錯誤，但不是特定工作特有的。<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**資訊 \_裝置 \_ 鎖定 \_ 計數器**</dt> <dt>0x00400000</dt> </dl>              | 尚未建立裝置鎖定計數器。<br/>                                                                                                                                                                               |
| <span id="INFORMATION_DEVICEID"></span><span id="information_deviceid"></span><dl> <dt>**資訊 \_DEVICEID**</dt> <dt> 0x00800000</dt> </dl>                                                | 尚未建立裝置識別碼。<br/>                                                                                                                                                                                 |
| <span id="INFORMATION_ATTESTATION_VULNERABILITY"></span><span id="information_attestation_vulnerability"></span><dl> <dt>**資訊 \_證明 \_ 弱點**</dt> <dt> 0x01000000</dt> </dl>                                                | TPM 具有健康情況證明相關的弱點。<br/>                                                                                                                                                                                 |


 

</dd> </dl>

## <a name="return-value"></a>傳回值

您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。

常見的傳回碼如下所示。



| 傳回碼/值                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Windows SDK 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                      |
| 命名空間<br/>                | \\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
