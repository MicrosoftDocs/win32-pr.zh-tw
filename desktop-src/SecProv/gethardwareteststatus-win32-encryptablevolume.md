---
description: 提供完整解密作業系統磁片區之硬體測試的相關狀態資訊。
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Win32_EncryptableVolume 類別的 GetHardwareTestStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979818"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7cf4e-103">Win32 EncryptableVolume 類別的 GetHardwareTestStatus 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7cf4e-103">GetHardwareTestStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7cf4e-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetHardwareTestStatus** 方法提供完整解密作業系統磁片區之硬體測試的相關狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-104">The **GetHardwareTestStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class provides status information about a hardware test of a fully decrypted operating system volume.</span></span>

<span data-ttu-id="7cf4e-105">您可以使用此方法來顯示硬體測試是否擱置，以及上次電腦重新開機後完成的硬體測試是否成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-105">Use this method to show whether a hardware test is pending, as well as the success or failure of a hardware test that completed on the last computer restart.</span></span> <span data-ttu-id="7cf4e-106">若要要求硬體測試，請使用 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-106">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf4e-107">語法</span><span class="sxs-lookup"><span data-stu-id="7cf4e-107">Syntax</span></span>


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a><span data-ttu-id="7cf4e-108">參數</span><span class="sxs-lookup"><span data-stu-id="7cf4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf4e-109">*TestStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7cf4e-109">*TestStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf4e-110">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7cf4e-110">Type: **uint32**</span></span>

<span data-ttu-id="7cf4e-111">指定硬體測試是否暫止，以及最後一次電腦重新開機時完成的硬體測試是否成功。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-111">Specifies whether a hardware test is pending, as well as the success of failure of a hardware test that completed on the last computer restart.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cf4e-112">值</span><span class="sxs-lookup"><span data-stu-id="7cf4e-112">Value</span></span></th>
<th><span data-ttu-id="7cf4e-113">意義</span><span class="sxs-lookup"><span data-stu-id="7cf4e-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <span data-ttu-id="7cf4e-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="7cf4e-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="7cf4e-115">如果已要求測試，則測試會在最後一次電腦重新開機時成功，而且磁片區加密現在正在進行中。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-115">If a test was requested, the test has succeeded on the last computer restart and volume encryption is now in progress.</span></span> <span data-ttu-id="7cf4e-116">如需加密狀態，請參閱 <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-116">For the encryption status, see the <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> method.</span></span> <span data-ttu-id="7cf4e-117">否則，在上一次電腦重新開機時不會執行任何測試，且沒有擱置中的測試。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-117">Otherwise, no test ran on the last computer restart and none is pending.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <span data-ttu-id="7cf4e-118"><dt><strong>失敗</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="7cf4e-118"><dt><strong>Failed</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="7cf4e-119">磁片區加密未啟動。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-119">Volume encryption did not start.</span></span> <span data-ttu-id="7cf4e-120">已移除所有金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-120">All key protectors were removed.</span></span><br/> <span data-ttu-id="7cf4e-121">若要解決失敗的測試：</span><span class="sxs-lookup"><span data-stu-id="7cf4e-121">To resolve a failed test:</span></span><br/>
<ul>
<li><span data-ttu-id="7cf4e-122">請參閱 <em>TestError</em> 參數中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-122">Consult the information in the <em>TestError</em> parameter.</span></span></li>
<li><span data-ttu-id="7cf4e-123">新增金鑰保護裝置，並再次使用 <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-123">Add key protectors and use the <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> method again.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <span data-ttu-id="7cf4e-124"><dt><strong>暫</strong></dt>止 <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="7cf4e-124"><dt><strong>Pending</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="7cf4e-125">已要求測試，並將在下一次電腦重新開機時執行。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-125">A test has been requested and will run on the next computer restart.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="7cf4e-126">*TestError* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7cf4e-126">*TestError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf4e-127">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7cf4e-127">Type: **uint32**</span></span>

<span data-ttu-id="7cf4e-128">指定上次完成的硬體測試錯誤。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-128">Specifies the error from the last completed hardware test.</span></span>



| <span data-ttu-id="7cf4e-129">值</span><span class="sxs-lookup"><span data-stu-id="7cf4e-129">Value</span></span>                                                                                               | <span data-ttu-id="7cf4e-130">意義</span><span class="sxs-lookup"><span data-stu-id="7cf4e-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7cf4e-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-131"><dt>0</dt></span></span> </dl>                        | <span data-ttu-id="7cf4e-132">未發生任何錯誤，或未在最後一次電腦重新開機時執行硬體測試。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-132">No errors occurred or no hardware test ran on the last computer restart.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="7cf4e-133"><dt> 2150694972 (0x8031003C) </dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-133"><dt> 2150694972 (0x8031003C)</dt></span></span> </dl> | <span data-ttu-id="7cf4e-134">\_ \_ \_ \_ 找不到 FVE E KEYFILE</span><span class="sxs-lookup"><span data-stu-id="7cf4e-134">FVE\_E\_KEYFILE\_NOT\_FOUND</span></span><br/> <span data-ttu-id="7cf4e-135">找不到具有外部金鑰檔的 USB 快閃磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-135">A USB flash drive with an external key file was not found.</span></span> <span data-ttu-id="7cf4e-136">如果此失敗持續發生，電腦將無法在重新開機期間讀取 USB 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-136">If this failure persists, the computer cannot read USB drives during restart.</span></span> <span data-ttu-id="7cf4e-137">在重新開機期間，您可能無法使用外部金鑰來解除鎖定作業系統磁片區。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-137">You may not be able to use external keys to unlock the operating system volume during restart.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7cf4e-138"><dt> 2150694973 (0x8031003D) </dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-138"><dt> 2150694973 (0x8031003D)</dt></span></span> </dl> | <span data-ttu-id="7cf4e-139">FVE \_ E \_ KEYFILE \_ 無效</span><span class="sxs-lookup"><span data-stu-id="7cf4e-139">FVE\_E\_KEYFILE\_INVALID</span></span><br/> <span data-ttu-id="7cf4e-140">USB 快閃磁片磁碟機上的外部金鑰檔已損毀。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-140">The external key file on the USB flash drive was corrupt.</span></span> <span data-ttu-id="7cf4e-141">請嘗試其他 USB 快閃磁片磁碟機來儲存外部金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-141">Try a different USB flash drive to store the external key file.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="7cf4e-142"><dt> 2150694975 (0x8031003F) </dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-142"><dt> 2150694975 (0x8031003F)</dt></span></span> </dl> | <span data-ttu-id="7cf4e-143">\_ \_ \_ 已停用 FVE E TPM</span><span class="sxs-lookup"><span data-stu-id="7cf4e-143">FVE\_E\_TPM\_DISABLED</span></span><br/> <span data-ttu-id="7cf4e-144">TPM 已停用或停用，或已停用或停用。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-144">The TPM is either disabled or deactivated or both disabled and deactivated.</span></span> <span data-ttu-id="7cf4e-145">若要開啟 TPM，請使用 [**Win32 \_ tpm**](win32-tpm.md) WMI 提供者，或執行 tpm 管理嵌入式管理單元 (的) 。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-145">To turn on the TPM, use the [**Win32\_Tpm**](win32-tpm.md) WMI provider or run the TPM management snap-in (Tpm.msc).</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="7cf4e-146"><dt> 2150694977 (0x80310041) </dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-146"><dt> 2150694977 (0x80310041)</dt></span></span> </dl> | <span data-ttu-id="7cf4e-147">FVE \_ E \_ TPM \_ 不正確 \_ PCR</span><span class="sxs-lookup"><span data-stu-id="7cf4e-147">FVE\_E\_TPM\_INVALID\_PCR</span></span><br/> <span data-ttu-id="7cf4e-148">TPM 偵測到目前平臺驗證設定檔內作業系統重新開機服務的變更。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-148">The TPM detected a change in operating system restart services within the current platform validation profile.</span></span> <span data-ttu-id="7cf4e-149">從電腦移除任何啟動 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-149">Remove any startup CD or DVD from the computer.</span></span> <span data-ttu-id="7cf4e-150">如果此失敗持續發生，請檢查是否已安裝最新的固件和 BIOS 升級，以及 TPM 是否正常運作。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-150">If this failure persists, check that the latest firmware and BIOS upgrades are installed, and that the TPM is otherwise working properly.</span></span><br/> |
| <dl> <span data-ttu-id="7cf4e-151"><dt>2150694979 (0x80310043) </dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-151"><dt>2150694979 (0x80310043)</dt></span></span> </dl>  | <span data-ttu-id="7cf4e-152">FVE \_ E \_ PIN \_ 無效</span><span class="sxs-lookup"><span data-stu-id="7cf4e-152">FVE\_E\_PIN\_INVALID</span></span><br/> <span data-ttu-id="7cf4e-153">提供的 PIN 不正確。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-153">The provided PIN was incorrect.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf4e-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cf4e-154">Return value</span></span>

<span data-ttu-id="7cf4e-155">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7cf4e-155">Type: **uint32**</span></span>

<span data-ttu-id="7cf4e-156">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-156">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="7cf4e-157">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="7cf4e-157">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="7cf4e-158">Description</span><span class="sxs-lookup"><span data-stu-id="7cf4e-158">Description</span></span>                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7cf4e-159"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-159"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="7cf4e-160">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-160">The method succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="7cf4e-161"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-161"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="7cf4e-162">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-162">The volume is locked.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7cf4e-163">備註</span><span class="sxs-lookup"><span data-stu-id="7cf4e-163">Remarks</span></span>

<span data-ttu-id="7cf4e-164">若要要求硬體測試，請使用 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-164">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="7cf4e-165">若要在狀態為 [擱置中] 時執行硬體測試，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="7cf4e-165">To run a hardware test when its status is pending, follow these steps:</span></span>

1.  <span data-ttu-id="7cf4e-166">將包含外部金鑰檔案的 USB 快閃磁片磁碟機插入電腦。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-166">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="7cf4e-167">只有當磁片區具有「外部金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置時，才適用此步驟。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-167">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="7cf4e-168">重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-168">Restart the computer.</span></span> <span data-ttu-id="7cf4e-169">電腦重新開機時，會自動執行硬體測試。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-169">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="7cf4e-170">若要取消硬體測試，請使用 [**加密**](encrypt-win32-encryptablevolume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-170">To cancel the hardware test, use the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="7cf4e-171">成功的測試會判斷：</span><span class="sxs-lookup"><span data-stu-id="7cf4e-171">A successful test determines that:</span></span>

-   <span data-ttu-id="7cf4e-172">如果有 TPM 相關的金鑰保護裝置，TPM 就可以將磁片區解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-172">The TPM can unlock the volume if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="7cf4e-173">如果磁片區可由外部 (金鑰（包括啟動金鑰) ）解除鎖定，電腦就可以在啟動期間讀取包含外部金鑰檔的 USB 快閃磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-173">The computer can read a USB flash drive that contains an external key file during startup if the volume can be unlocked by an external key (including a startup key).</span></span>

<span data-ttu-id="7cf4e-174">在轉換任何變更之後或下次電腦重新開機之後，將無法使用硬體測試結果。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-174">Hardware test results will not be available after any changes in conversion or after the next computer restart.</span></span> <span data-ttu-id="7cf4e-175">檢查系統事件記錄檔，以取得先前在電腦上執行之任何硬體測試的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-175">Check the System event log for the information about any hardware tests that previously ran on the computer.</span></span>

<span data-ttu-id="7cf4e-176">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-176">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7cf4e-177">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-177">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7cf4e-178">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-178">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7cf4e-179">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="7cf4e-179">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf4e-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cf4e-180">Requirements</span></span>



| <span data-ttu-id="7cf4e-181">需求</span><span class="sxs-lookup"><span data-stu-id="7cf4e-181">Requirement</span></span> | <span data-ttu-id="7cf4e-182">值</span><span class="sxs-lookup"><span data-stu-id="7cf4e-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf4e-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cf4e-183">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf4e-184">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cf4e-184">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7cf4e-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cf4e-185">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf4e-186">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cf4e-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cf4e-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="7cf4e-187">Namespace</span></span><br/>                | <span data-ttu-id="7cf4e-188">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="7cf4e-188">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7cf4e-189">MOF</span><span class="sxs-lookup"><span data-stu-id="7cf4e-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cf4e-190"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cf4e-190"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf4e-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cf4e-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf4e-192">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="7cf4e-192">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
