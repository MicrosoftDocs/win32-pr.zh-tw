---
description: 嘗試將 TPM 布建至完全就緒狀態，並將 TPM 的擁有權（如果尚未擁有）。
ms.assetid: D0C09A48-00D0-4BF2-8F0A-451A61EA7810
title: Win32_Tpm：:P rovision 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Provision
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 198d7b02b1813002ce55d175ad016ace23ee7da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851515"
---
# <a name="win32_tpmprovision-method"></a><span data-ttu-id="baf3a-103">Win32 \_ Tpm：:P rovision 方法</span><span class="sxs-lookup"><span data-stu-id="baf3a-103">Win32\_Tpm::Provision method</span></span>

<span data-ttu-id="baf3a-104">嘗試將 TPM 布建至完全就緒狀態，並將 TPM 的擁有權（如果尚未擁有）。</span><span class="sxs-lookup"><span data-stu-id="baf3a-104">Attempts to provision the TPM to a completely ready state and will take the ownership of TPM if it is not already owned.</span></span> <span data-ttu-id="baf3a-105">這種方法的執行成本很高，因為它會執行許多檢查。</span><span class="sxs-lookup"><span data-stu-id="baf3a-105">This method is expensive to execute because it performs many checks.</span></span> <span data-ttu-id="baf3a-106">建議的應用程式只在必要時才使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="baf3a-106">It is recommended applications use this method only when necessary.</span></span>

<span data-ttu-id="baf3a-107">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="baf3a-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="baf3a-108">語法</span><span class="sxs-lookup"><span data-stu-id="baf3a-108">Syntax</span></span>


```C++
uint32 Provision(
  [in]  BOOL   ForceClear_Allowed,
  [in]  BOOL   PhysicalPresencePrompts_Allowed,
  [out] uint32 Information
);
```



## <a name="parameters"></a><span data-ttu-id="baf3a-109">參數</span><span class="sxs-lookup"><span data-stu-id="baf3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baf3a-110">*ForceClear \_允許* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="baf3a-110">*ForceClear\_Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baf3a-111">當設為 **TRUE** 時，方法可能會要求實體存在作業來清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="baf3a-111">When set to **TRUE** the method may request physical presence operations to clear the TPM.</span></span> <span data-ttu-id="baf3a-112">如果設定為 **FALSE**，此方法將不會要求實體存在作業來清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="baf3a-112">If set to **FALSE**, the method will not request a physical presence operation to clear the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="baf3a-113">*PhysicalPresencePrompts \_允許* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="baf3a-113">*PhysicalPresencePrompts\_Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baf3a-114">當設為 **TRUE** 時，方法可能會要求在開機過程中需要使用者介入的實體存在作業，以確認 TPM 狀態變更。</span><span class="sxs-lookup"><span data-stu-id="baf3a-114">When set to **TRUE** the method may request physical presence operations that require user involvement during the boot process to confirm the TPM state change.</span></span>

</dd> <dt>

<span data-ttu-id="baf3a-115">*資訊* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="baf3a-115">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="baf3a-116">傳回完整布建 TPM 所需內容的最多可用資訊的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="baf3a-116">Returns a bitmask of as much information as is available of what is needed to fully provision the TPM.</span></span> <span data-ttu-id="baf3a-117">遮罩值（例如資訊 \_ 重新開機）表示方法呼叫應該起始重新開機，以將布建程式轉寄。</span><span class="sxs-lookup"><span data-stu-id="baf3a-117">Mask values like INFORMATION\_REBOOT indicate the method call should initiate a reboot to move the provisioning process forwards.</span></span>

<span data-ttu-id="baf3a-118">*資訊* 參數可能包含下列值。</span><span class="sxs-lookup"><span data-stu-id="baf3a-118">The *Information* parameter may consist of the following values.</span></span>



| <span data-ttu-id="baf3a-119">值</span><span class="sxs-lookup"><span data-stu-id="baf3a-119">Value</span></span>                                                                                                                                                                                                                                                                                              | <span data-ttu-id="baf3a-120">意義</span><span class="sxs-lookup"><span data-stu-id="baf3a-120">Meaning</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <span data-ttu-id="baf3a-121"><dt>**資訊 \_關機**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-121"><dt>**INFORMATION\_SHUTDOWN**</dt> <dt>0x00000002</dt></span></span> </dl>                                                 | <span data-ttu-id="baf3a-122">需要重新開機平臺 (關機) 。</span><span class="sxs-lookup"><span data-stu-id="baf3a-122">Platform restart is required (shutdown).</span></span><br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <span data-ttu-id="baf3a-123"><dt>**資訊 \_重新開機**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-123"><dt>**INFORMATION\_REBOOT**</dt> <dt>0x00000004</dt></span></span> </dl>                                                       | <span data-ttu-id="baf3a-124">需要重新開機平臺 (重新開機) 。</span><span class="sxs-lookup"><span data-stu-id="baf3a-124">Platform restart is required (reboot).</span></span><br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <span data-ttu-id="baf3a-125"><dt>**資訊 \_TPM \_ 強制 \_ 清除**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-125"><dt>**INFORMATION\_TPM\_FORCE\_CLEAR**</dt> <dt>0x00000008</dt></span></span> </dl>                          | <span data-ttu-id="baf3a-126">TPM 已經擁有。</span><span class="sxs-lookup"><span data-stu-id="baf3a-126">The TPM is already owned.</span></span> <span data-ttu-id="baf3a-127">必須清除 TPM，或需要匯入 TPM 擁有者授權值。</span><span class="sxs-lookup"><span data-stu-id="baf3a-127">Either the TPM needs to be cleared or the TPM owner authorization value needs to be imported.</span></span><br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <span data-ttu-id="baf3a-128"><dt>**資訊 \_實體 \_ 狀態**</dt>的 <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-128"><dt>**INFORMATION\_PHYSICAL\_PRESENCE**</dt> <dt>0x00000010</dt></span></span> </dl>                     | <span data-ttu-id="baf3a-129">布建 TPM 需要實體存在。</span><span class="sxs-lookup"><span data-stu-id="baf3a-129">Physical Presence is required to provision the TPM.</span></span><br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <span data-ttu-id="baf3a-130"><dt>**資訊 \_TPM \_ 啟動**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-130"><dt>**INFORMATION\_TPM\_ACTIVATE**</dt> <dt>0x00000020</dt></span></span> </dl>                                    | <span data-ttu-id="baf3a-131">TPM 已停用或停用。</span><span class="sxs-lookup"><span data-stu-id="baf3a-131">The TPM is disabled or deactivated.</span></span><br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <span data-ttu-id="baf3a-132"><dt>**資訊 \_TPM \_ 取得 \_ 擁有權**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-132"><dt>**INFORMATION\_TPM\_TAKE\_OWNERSHIP**</dt> <dt>0x00000040</dt></span></span> </dl>                 | <span data-ttu-id="baf3a-133">已取得 TPM 擁有權。</span><span class="sxs-lookup"><span data-stu-id="baf3a-133">The TPM ownership was taken.</span></span><br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <span data-ttu-id="baf3a-134"><dt>**資訊 \_TPM \_ 建立 \_ EK**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-134"><dt>**INFORMATION\_TPM\_CREATE\_EK**</dt> <dt>0x00000080</dt></span></span> </dl>                                | <span data-ttu-id="baf3a-135">TPM 中有 (EK) 的簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="baf3a-135">An Endorsement Key (EK) exists in the TPM.</span></span> <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <span data-ttu-id="baf3a-136"><dt>**資訊 \_TPM \_ OWNERAUTH**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-136"><dt>**INFORMATION\_TPM\_OWNERAUTH**</dt> <dt>0x00000100</dt></span></span> </dl>                                 | <span data-ttu-id="baf3a-137">TPM 擁有者授權未正確儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="baf3a-137">The TPM owner authorization is not properly stored in the registry.</span></span><br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <span data-ttu-id="baf3a-138"><dt>**資訊 \_TPM \_ SRK \_ 驗證**</dt> <dt>0x000000200</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-138"><dt>**INFORMATION\_TPM\_SRK\_AUTH**</dt> <dt>0x000000200</dt></span></span> </dl>                                  | <span data-ttu-id="baf3a-139">儲存體根金鑰 (SRK) 授權值並非全部為零。</span><span class="sxs-lookup"><span data-stu-id="baf3a-139">The Storage Root Key (SRK) authorization value is not all zeros.</span></span><br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <span data-ttu-id="baf3a-140"><dt>**資訊 \_TPM \_ 停用 \_ 擁有者 \_ 清除**</dt> <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-140"><dt>**INFORMATION\_TPM\_DISABLE\_OWNER\_CLEAR**</dt> <dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="baf3a-141">如果作業系統設定為停用 tpm 擁有者授權值的 TPM 清除，但 TPM 尚未設定為防止以 TPM 擁有者授權值清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="baf3a-141">If the operating system is configured to disable clearing of the TPM with the TPM owner authorization value and the TPM has not yet been configured to prevent clearing of the TPM with the TPM owner authorization value .</span></span><br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <span data-ttu-id="baf3a-142"><dt>**資訊 \_TPM \_ SRKPUB**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-142"><dt>**INFORMATION\_TPM\_SRKPUB**</dt> <dt>0x00000800</dt></span></span> </dl>                                          | <span data-ttu-id="baf3a-143">與 tpm 儲存根金鑰相關的作業系統登錄資訊不符合 TPM 儲存根金鑰。</span><span class="sxs-lookup"><span data-stu-id="baf3a-143">The operating system's registry information about the TPM’s Storage Root Key does not match the TPM Storage Root Key.</span></span><br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <span data-ttu-id="baf3a-144"><dt>**資訊 \_TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-144"><dt>**INFORMATION\_TPM\_READ\_SRKPUB**</dt> <dt>0x00001000</dt></span></span> </dl>                          | <span data-ttu-id="baf3a-145">TPM 永久旗標允許讀取儲存體根金鑰公用值未設定。</span><span class="sxs-lookup"><span data-stu-id="baf3a-145">The TPM permanent flag to allow reading of the Storage Root Key public value is not set.</span></span><br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <span data-ttu-id="baf3a-146"><dt>**資訊 \_TPM \_ 開機 \_ 計數器**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-146"><dt>**INFORMATION\_TPM\_BOOT\_COUNTER**</dt> <dt>0x00002000</dt></span></span> </dl>                       | <span data-ttu-id="baf3a-147">未建立開機期間遞增的單純計數器。</span><span class="sxs-lookup"><span data-stu-id="baf3a-147">The monotonic counter incremented during boot has not been created.</span></span><br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <span data-ttu-id="baf3a-148"><dt>**資訊 \_TPM \_ AD \_ 備份**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-148"><dt>**INFORMATION\_TPM\_AD\_BACKUP**</dt> <dt>0x00004000</dt></span></span> </dl>                                | <span data-ttu-id="baf3a-149">TPM 的擁有者授權尚未備份至 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="baf3a-149">The TPM’s owner authorization has not been backed up to Active Directory.</span></span><br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <span data-ttu-id="baf3a-150"><dt>**資訊 \_TPM \_ AD \_ 備份 \_ 階段 \_ I**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-150"><dt>**INFORMATION\_TPM\_AD\_BACKUP\_PHASE\_I**</dt> <dt>0x00008000</dt></span></span> </dl>      | <span data-ttu-id="baf3a-151">Active Directory 中 TPM 擁有者授權資訊儲存區的第一個部分正在進行中。</span><span class="sxs-lookup"><span data-stu-id="baf3a-151">The first portion of the TPM owner authorization information storage in Active Directory is in progress.</span></span><br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <span data-ttu-id="baf3a-152"><dt>**資訊 \_TPM \_ AD \_ 備份 \_ 第 \_ 二階段**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-152"><dt>**INFORMATION\_TPM\_AD\_BACKUP\_PHASE\_II**</dt> <dt>0x00010000</dt></span></span> </dl>   | <span data-ttu-id="baf3a-153">Active Directory 中 TPM 擁有者授權資訊儲存的第二個部分正在進行中。</span><span class="sxs-lookup"><span data-stu-id="baf3a-153">The second portion of the TPM owner authorization information storage in Active Directory is in progress.</span></span><br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <span data-ttu-id="baf3a-154"><dt>**資訊 \_舊版 \_**</dt>設定 <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-154"><dt>**INFORMATION\_LEGACY\_CONFIGURATION**</dt> <dt>0x00020000</dt></span></span> </dl>            | <span data-ttu-id="baf3a-155">Windows 群組原則設定為不儲存任何 TPM 擁有者授權，因此 TPM 無法完全就緒。</span><span class="sxs-lookup"><span data-stu-id="baf3a-155">Windows Group Policy is configured to not store any TPM owner authorization so the TPM cannot be fully ready.</span></span><br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <span data-ttu-id="baf3a-156"><dt>**資訊 \_EK \_ 憑證**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-156"><dt>**INFORMATION\_EK\_CERTIFICATE**</dt> <dt>0x00040000</dt></span></span> </dl>                              | <span data-ttu-id="baf3a-157">未從 TPM NV Ram 讀取 EK 憑證，並將其儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="baf3a-157">The EK Certificate was not read from the TPM NV Ram and stored in the registry.</span></span> <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <span data-ttu-id="baf3a-158"><dt>**資訊 \_TCG \_ 事件 \_ 記錄**</dt>檔 <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-158"><dt>**INFORMATION\_TCG\_EVENT\_LOG**</dt> <dt>0x00080000</dt></span></span> </dl>                                | <span data-ttu-id="baf3a-159">TCG 事件記錄檔是空的或無法讀取。</span><span class="sxs-lookup"><span data-stu-id="baf3a-159">The TCG event log is empty or cannot be read.</span></span> <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <span data-ttu-id="baf3a-160"><dt>**資訊 \_未 \_ 減少**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-160"><dt>**INFORMATION\_NOT\_REDUCED**</dt> <dt>0x00100000</dt></span></span> </dl>                                       | <span data-ttu-id="baf3a-161">未擁有 TPM。</span><span class="sxs-lookup"><span data-stu-id="baf3a-161">The TPM is not owned.</span></span><br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <span data-ttu-id="baf3a-162"><dt>**資訊 \_一般 \_ 錯誤**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-162"><dt>**INFORMATION\_GENERIC\_ERROR**</dt> <dt>0x00200000</dt></span></span> </dl>                                 | <span data-ttu-id="baf3a-163">發生錯誤，但不是特定工作特有的。</span><span class="sxs-lookup"><span data-stu-id="baf3a-163">An error occurred, but not specific to a particular task.</span></span><br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <span data-ttu-id="baf3a-164"><dt>**資訊 \_裝置 \_ 鎖定 \_ 計數器**</dt> <dt>0x00400000</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-164"><dt>**INFORMATION\_DEVICE\_LOCK\_COUNTER**</dt> <dt>0x00400000</dt></span></span> </dl>              | <span data-ttu-id="baf3a-165">尚未建立裝置鎖定計數器。</span><span class="sxs-lookup"><span data-stu-id="baf3a-165">The device lock counter has not been created.</span></span><br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baf3a-166">傳回值</span><span class="sxs-lookup"><span data-stu-id="baf3a-166">Return value</span></span>

<span data-ttu-id="baf3a-167">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="baf3a-167">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="baf3a-168">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="baf3a-168">Common return codes are listed below.</span></span>



| <span data-ttu-id="baf3a-169">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="baf3a-169">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="baf3a-170">Description</span><span class="sxs-lookup"><span data-stu-id="baf3a-170">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="baf3a-171"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-171"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="baf3a-172">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="baf3a-172">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="baf3a-173">備註</span><span class="sxs-lookup"><span data-stu-id="baf3a-173">Remarks</span></span>

<span data-ttu-id="baf3a-174">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="baf3a-174">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="baf3a-175">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="baf3a-175">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="baf3a-176">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="baf3a-176">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="baf3a-177">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="baf3a-177">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="baf3a-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="baf3a-178">Requirements</span></span>



| <span data-ttu-id="baf3a-179">需求</span><span class="sxs-lookup"><span data-stu-id="baf3a-179">Requirement</span></span> | <span data-ttu-id="baf3a-180">值</span><span class="sxs-lookup"><span data-stu-id="baf3a-180">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf3a-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="baf3a-181">Minimum supported client</span></span><br/> | <span data-ttu-id="baf3a-182">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="baf3a-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="baf3a-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="baf3a-183">Minimum supported server</span></span><br/> | <span data-ttu-id="baf3a-184">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="baf3a-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="baf3a-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="baf3a-185">Namespace</span></span><br/>                | <span data-ttu-id="baf3a-186">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="baf3a-186">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="baf3a-187">MOF</span><span class="sxs-lookup"><span data-stu-id="baf3a-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="baf3a-188"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-188"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="baf3a-189">DLL</span><span class="sxs-lookup"><span data-stu-id="baf3a-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baf3a-190"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baf3a-190"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baf3a-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baf3a-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf3a-192">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="baf3a-192">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
