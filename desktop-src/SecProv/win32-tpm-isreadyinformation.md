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
ms.openlocfilehash: 23f3b2f38ea12bac19230f1871d30c84098eb1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944946"
---
# <a name="win32_tpmisreadyinformation-method"></a><span data-ttu-id="662b5-103">Win32 \_ Tpm：： IsReadyInformation 方法</span><span class="sxs-lookup"><span data-stu-id="662b5-103">Win32\_Tpm::IsReadyInformation method</span></span>

<span data-ttu-id="662b5-104">指出 TPM 是否已就緒，並提供 TPM 狀態的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="662b5-104">Indicates whether the TPM is ready and provides additional information on the state of the TPM.</span></span> <span data-ttu-id="662b5-105">Information 參數會傳回完整布建 TPM 所需之資訊的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="662b5-105">The information parameter returns a bitmask of information of what is needed to fully provision the TPM.</span></span>

<span data-ttu-id="662b5-106">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="662b5-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="662b5-107">語法</span><span class="sxs-lookup"><span data-stu-id="662b5-107">Syntax</span></span>


```C++
uint32 IsReadyInformation(
  [out] BOOL   IsReady,
  [out] uint32 Information
);
```



## <a name="parameters"></a><span data-ttu-id="662b5-108">參數</span><span class="sxs-lookup"><span data-stu-id="662b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="662b5-109">*IsReady* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="662b5-109">*IsReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="662b5-110">如果 TPM 和系統已完全布建以供 TPM 使用，則設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="662b5-110">Set to **TRUE** if the TPM and system are fully provisioned for TPM use.</span></span>

</dd> <dt>

<span data-ttu-id="662b5-111">*資訊* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="662b5-111">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="662b5-112">傳回完整布建 TPM 所需內容的最多可用資訊的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="662b5-112">Returns a bitmask of as much information as is available of what is needed to fully provision the TPM.</span></span>

<span data-ttu-id="662b5-113">*資訊* 參數可能包含下列值。</span><span class="sxs-lookup"><span data-stu-id="662b5-113">The *Information* parameter may consist of the following values.</span></span>



| <span data-ttu-id="662b5-114">值</span><span class="sxs-lookup"><span data-stu-id="662b5-114">Value</span></span>                                                                                                                                                                                                                                                                                              | <span data-ttu-id="662b5-115">意義</span><span class="sxs-lookup"><span data-stu-id="662b5-115">Meaning</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <span data-ttu-id="662b5-116"><dt>**資訊 \_關機**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-116"><dt>**INFORMATION\_SHUTDOWN**</dt> <dt>0x00000002</dt></span></span> </dl>                                                 | <span data-ttu-id="662b5-117">需要重新開機平臺 (關機) 。</span><span class="sxs-lookup"><span data-stu-id="662b5-117">Platform restart is required (shutdown).</span></span><br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <span data-ttu-id="662b5-118"><dt>**資訊 \_重新開機**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-118"><dt>**INFORMATION\_REBOOT**</dt> <dt>0x00000004</dt></span></span> </dl>                                                       | <span data-ttu-id="662b5-119">需要重新開機平臺 (重新開機) 。</span><span class="sxs-lookup"><span data-stu-id="662b5-119">Platform restart is required (reboot).</span></span><br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <span data-ttu-id="662b5-120"><dt>**資訊 \_TPM \_ 強制 \_ 清除**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-120"><dt>**INFORMATION\_TPM\_FORCE\_CLEAR**</dt> <dt>0x00000008</dt></span></span> </dl>                          | <span data-ttu-id="662b5-121">TPM 已經擁有。</span><span class="sxs-lookup"><span data-stu-id="662b5-121">The TPM is already owned.</span></span> <span data-ttu-id="662b5-122">必須清除 TPM，或需要匯入 TPM 擁有者授權值。</span><span class="sxs-lookup"><span data-stu-id="662b5-122">Either the TPM needs to be cleared or the TPM owner authorization value needs to be imported.</span></span><br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <span data-ttu-id="662b5-123"><dt>**資訊 \_實體 \_ 狀態**</dt>的 <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-123"><dt>**INFORMATION\_PHYSICAL\_PRESENCE**</dt> <dt>0x00000010</dt></span></span> </dl>                     | <span data-ttu-id="662b5-124">布建 TPM 需要實體存在。</span><span class="sxs-lookup"><span data-stu-id="662b5-124">Physical Presence is required to provision the TPM.</span></span><br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <span data-ttu-id="662b5-125"><dt>**資訊 \_TPM \_ 啟動**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-125"><dt>**INFORMATION\_TPM\_ACTIVATE**</dt> <dt>0x00000020</dt></span></span> </dl>                                    | <span data-ttu-id="662b5-126">TPM 已停用或停用。</span><span class="sxs-lookup"><span data-stu-id="662b5-126">The TPM is disabled or deactivated.</span></span><br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <span data-ttu-id="662b5-127"><dt>**資訊 \_TPM \_ 取得 \_ 擁有權**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-127"><dt>**INFORMATION\_TPM\_TAKE\_OWNERSHIP**</dt> <dt>0x00000040</dt></span></span> </dl>                 | <span data-ttu-id="662b5-128">已取得 TPM 擁有權。</span><span class="sxs-lookup"><span data-stu-id="662b5-128">The TPM ownership was taken.</span></span><br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <span data-ttu-id="662b5-129"><dt>**資訊 \_TPM \_ 建立 \_ EK**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-129"><dt>**INFORMATION\_TPM\_CREATE\_EK**</dt> <dt>0x00000080</dt></span></span> </dl>                                | <span data-ttu-id="662b5-130">TPM 中有 (EK) 的簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="662b5-130">An Endorsement Key (EK) exists in the TPM.</span></span> <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <span data-ttu-id="662b5-131"><dt>**資訊 \_TPM \_ OWNERAUTH**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-131"><dt>**INFORMATION\_TPM\_OWNERAUTH**</dt> <dt>0x00000100</dt></span></span> </dl>                                 | <span data-ttu-id="662b5-132">TPM 擁有者授權未正確儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="662b5-132">The TPM owner authorization is not properly stored in the registry.</span></span><br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <span data-ttu-id="662b5-133"><dt>**資訊 \_TPM \_ SRK \_ 驗證**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-133"><dt>**INFORMATION\_TPM\_SRK\_AUTH**</dt> <dt>0x00000200</dt></span></span> </dl>                                  | <span data-ttu-id="662b5-134">儲存體根金鑰 (SRK) 授權值並非全部為零。</span><span class="sxs-lookup"><span data-stu-id="662b5-134">The Storage Root Key (SRK) authorization value is not all zeros.</span></span><br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <span data-ttu-id="662b5-135"><dt>**資訊 \_TPM \_ 停用 \_ 擁有者 \_ 清除**</dt> <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-135"><dt>**INFORMATION\_TPM\_DISABLE\_OWNER\_CLEAR**</dt> <dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="662b5-136">如果作業系統設定為停用 tpm 擁有者授權值的 TPM 清除，但 TPM 尚未設定為防止以 TPM 擁有者授權值清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="662b5-136">If the operating system is configured to disable clearing of the TPM with the TPM owner authorization value and the TPM has not yet been configured to prevent clearing of the TPM with the TPM owner authorization value .</span></span><br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <span data-ttu-id="662b5-137"><dt>**資訊 \_TPM \_ SRKPUB**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-137"><dt>**INFORMATION\_TPM\_SRKPUB**</dt> <dt>0x00000800</dt></span></span> </dl>                                          | <span data-ttu-id="662b5-138">與 tpm 儲存根金鑰相關的作業系統登錄資訊不符合 TPM 儲存根金鑰。</span><span class="sxs-lookup"><span data-stu-id="662b5-138">The operating system's registry information about the TPM’s Storage Root Key does not match the TPM Storage Root Key.</span></span><br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <span data-ttu-id="662b5-139"><dt>**資訊 \_TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-139"><dt>**INFORMATION\_TPM\_READ\_SRKPUB**</dt> <dt>0x00001000</dt></span></span> </dl>                          | <span data-ttu-id="662b5-140">TPM 永久旗標允許讀取儲存體根金鑰公用值未設定。</span><span class="sxs-lookup"><span data-stu-id="662b5-140">The TPM permanent flag to allow reading of the Storage Root Key public value is not set.</span></span><br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <span data-ttu-id="662b5-141"><dt>**資訊 \_TPM \_ 開機 \_ 計數器**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-141"><dt>**INFORMATION\_TPM\_BOOT\_COUNTER**</dt> <dt>0x00002000</dt></span></span> </dl>                       | <span data-ttu-id="662b5-142">未建立開機期間遞增的單純計數器。</span><span class="sxs-lookup"><span data-stu-id="662b5-142">The monotonic counter incremented during boot has not been created.</span></span><br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <span data-ttu-id="662b5-143"><dt>**資訊 \_TPM \_ AD \_ 備份**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-143"><dt>**INFORMATION\_TPM\_AD\_BACKUP**</dt> <dt>0x00004000</dt></span></span> </dl>                                | <span data-ttu-id="662b5-144">TPM 的擁有者授權尚未備份至 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="662b5-144">The TPM’s owner authorization has not been backed up to Active Directory.</span></span><br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <span data-ttu-id="662b5-145"><dt>**資訊 \_TPM \_ AD \_ 備份 \_ 階段 \_ I**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-145"><dt>**INFORMATION\_TPM\_AD\_BACKUP\_PHASE\_I**</dt> <dt>0x00008000</dt></span></span> </dl>      | <span data-ttu-id="662b5-146">Active Directory 中 TPM 擁有者授權資訊儲存區的第一個部分正在進行中。</span><span class="sxs-lookup"><span data-stu-id="662b5-146">The first portion of the TPM owner authorization information storage in Active Directory is in progress.</span></span><br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <span data-ttu-id="662b5-147"><dt>**資訊 \_TPM \_ AD \_ 備份 \_ 第 \_ 二階段**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-147"><dt>**INFORMATION\_TPM\_AD\_BACKUP\_PHASE\_II**</dt> <dt>0x00010000</dt></span></span> </dl>   | <span data-ttu-id="662b5-148">Active Directory 中 TPM 擁有者授權資訊儲存的第二個部分正在進行中。</span><span class="sxs-lookup"><span data-stu-id="662b5-148">The second portion of the TPM owner authorization information storage in Active Directory is in progress.</span></span><br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <span data-ttu-id="662b5-149"><dt>**資訊 \_舊版 \_**</dt>設定 <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-149"><dt>**INFORMATION\_LEGACY\_CONFIGURATION**</dt> <dt>0x00020000</dt></span></span> </dl>            | <span data-ttu-id="662b5-150">Windows 群組原則設定為不儲存任何 TPM 擁有者授權，因此 TPM 無法完全就緒。</span><span class="sxs-lookup"><span data-stu-id="662b5-150">Windows Group Policy is configured to not store any TPM owner authorization so the TPM cannot be fully ready.</span></span><br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <span data-ttu-id="662b5-151"><dt>**資訊 \_EK \_ 憑證**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-151"><dt>**INFORMATION\_EK\_CERTIFICATE**</dt> <dt>0x00040000</dt></span></span> </dl>                              | <span data-ttu-id="662b5-152">未從 TPM NV Ram 讀取 EK 憑證，並將其儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="662b5-152">The EK Certificate was not read from the TPM NV Ram and stored in the registry.</span></span> <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <span data-ttu-id="662b5-153"><dt>**資訊 \_TCG \_ 事件 \_ 記錄**</dt>檔 <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-153"><dt>**INFORMATION\_TCG\_EVENT\_LOG**</dt> <dt>0x00080000</dt></span></span> </dl>                                | <span data-ttu-id="662b5-154">TCG 事件記錄檔是空的或無法讀取。</span><span class="sxs-lookup"><span data-stu-id="662b5-154">The TCG event log is empty or cannot be read.</span></span> <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <span data-ttu-id="662b5-155"><dt>**資訊 \_未 \_ 減少**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-155"><dt>**INFORMATION\_NOT\_REDUCED**</dt> <dt>0x00100000</dt></span></span> </dl>                                       | <span data-ttu-id="662b5-156">未擁有 TPM。</span><span class="sxs-lookup"><span data-stu-id="662b5-156">The TPM is not owned.</span></span><br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <span data-ttu-id="662b5-157"><dt>**資訊 \_一般 \_ 錯誤**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-157"><dt>**INFORMATION\_GENERIC\_ERROR**</dt> <dt>0x00200000</dt></span></span> </dl>                                 | <span data-ttu-id="662b5-158">發生錯誤，但不是特定工作特有的。</span><span class="sxs-lookup"><span data-stu-id="662b5-158">An error occurred, but not specific to a particular task.</span></span><br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <span data-ttu-id="662b5-159"><dt>**資訊 \_裝置 \_ 鎖定 \_ 計數器**</dt> <dt>0x00400000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-159"><dt>**INFORMATION\_DEVICE\_LOCK\_COUNTER**</dt> <dt>0x00400000</dt></span></span> </dl>              | <span data-ttu-id="662b5-160">尚未建立裝置鎖定計數器。</span><span class="sxs-lookup"><span data-stu-id="662b5-160">The device lock counter has not been created.</span></span><br/>                                                                                                                                                                               |
| <span id="INFORMATION_DEVICEID"></span><span id="information_deviceid"></span><dl> <span data-ttu-id="662b5-161"><dt>**資訊 \_DEVICEID**</dt> <dt> 0x00800000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-161"><dt>**INFORMATION\_DEVICEID**</dt> <dt> 0x00800000</dt></span></span> </dl>                                                | <span data-ttu-id="662b5-162">尚未建立裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="662b5-162">The device identifier has not been created.</span></span><br/>                                                                                                                                                                                 |
| <span id="INFORMATION_ATTESTATION_VULNERABILITY"></span><span id="information_attestation_vulnerability"></span><dl> <span data-ttu-id="662b5-163"><dt>**資訊 \_證明 \_ 弱點**</dt> <dt> 0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-163"><dt>**INFORMATION\_ATTESTATION\_VULNERABILITY**</dt> <dt> 0x01000000</dt></span></span> </dl>                                                | <span data-ttu-id="662b5-164">TPM 具有健康情況證明相關的弱點。</span><span class="sxs-lookup"><span data-stu-id="662b5-164">The TPM has a Health Attestation related vulnerability.</span></span><br/>                                                                                                                                                                                 |


 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="662b5-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="662b5-165">Return value</span></span>

<span data-ttu-id="662b5-166">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="662b5-166">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="662b5-167">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="662b5-167">Common return codes are listed below.</span></span>



| <span data-ttu-id="662b5-168">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="662b5-168">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="662b5-169">Description</span><span class="sxs-lookup"><span data-stu-id="662b5-169">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="662b5-170"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-170"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="662b5-171">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="662b5-171">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="662b5-172">備註</span><span class="sxs-lookup"><span data-stu-id="662b5-172">Remarks</span></span>

<span data-ttu-id="662b5-173">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="662b5-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="662b5-174">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="662b5-174">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="662b5-175">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="662b5-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="662b5-176">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="662b5-176">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="662b5-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="662b5-177">Requirements</span></span>



| <span data-ttu-id="662b5-178">需求</span><span class="sxs-lookup"><span data-stu-id="662b5-178">Requirement</span></span> | <span data-ttu-id="662b5-179">值</span><span class="sxs-lookup"><span data-stu-id="662b5-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="662b5-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="662b5-180">Minimum supported client</span></span><br/> | <span data-ttu-id="662b5-181">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="662b5-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="662b5-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="662b5-182">Minimum supported server</span></span><br/> | <span data-ttu-id="662b5-183">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="662b5-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="662b5-184">命名空間</span><span class="sxs-lookup"><span data-stu-id="662b5-184">Namespace</span></span><br/>                | <span data-ttu-id="662b5-185">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="662b5-185">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="662b5-186">MOF</span><span class="sxs-lookup"><span data-stu-id="662b5-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="662b5-187"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-187"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="662b5-188">DLL</span><span class="sxs-lookup"><span data-stu-id="662b5-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="662b5-189"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="662b5-189"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="662b5-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="662b5-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="662b5-191">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="662b5-191">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
