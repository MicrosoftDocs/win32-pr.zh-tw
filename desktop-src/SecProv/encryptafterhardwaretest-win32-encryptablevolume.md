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
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1de0a-103">Win32 EncryptableVolume 類別的 EncryptAfterHardwareTest 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1de0a-103">EncryptAfterHardwareTest method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1de0a-104">在硬體測試之後， [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **EncryptAfterHardwareTest** 方法會開始加密完整解密的作業系統磁片區。</span><span class="sxs-lookup"><span data-stu-id="1de0a-104">The **EncryptAfterHardwareTest** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted operating system volume after a hardware test.</span></span> <span data-ttu-id="1de0a-105">需要重新開機才能執行此硬體測試。</span><span class="sxs-lookup"><span data-stu-id="1de0a-105">A reboot is required to perform this hardware test.</span></span> <span data-ttu-id="1de0a-106">使用這個方法，而不是 [**加密**](encrypt-win32-encryptablevolume.md) 方法來檢查 BitLocker 是否如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="1de0a-106">Use this method instead of the [**Encrypt**](encrypt-win32-encryptablevolume.md) method to check that BitLocker will work as expected.</span></span>

> [!Note]  
> <span data-ttu-id="1de0a-107">如果硬碟機硬體已加密，此方法不會加密資料。</span><span class="sxs-lookup"><span data-stu-id="1de0a-107">If the hard drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="1de0a-108">相反地，它會將寬線狀態從「永久解除鎖定」設定為解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="1de0a-108">Instead, it sets the band status to unlocked from "perpetually unlocked".</span></span> <span data-ttu-id="1de0a-109">如果頻外已鎖定、已解除鎖定或為唯讀，則會將磁片磁碟機視為已加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1de0a-110">語法</span><span class="sxs-lookup"><span data-stu-id="1de0a-110">Syntax</span></span>


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1de0a-111">參數</span><span class="sxs-lookup"><span data-stu-id="1de0a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1de0a-112">*EncryptionMethod* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1de0a-112">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1de0a-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1de0a-113">Type: **uint32**</span></span>

<span data-ttu-id="1de0a-114">指定用來加密磁片區的加密演算法和金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="1de0a-114">Specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="1de0a-115">將此參數保留空白，以使用預設值零。</span><span class="sxs-lookup"><span data-stu-id="1de0a-115">Leave this parameter blank to use the default value of zero.</span></span> <span data-ttu-id="1de0a-116">如果磁片區是部分或完整加密，此參數的值必須是0，或符合磁片區的現有加密方法。</span><span class="sxs-lookup"><span data-stu-id="1de0a-116">If the volume is partially or fully encrypted, the value of this parameter must be 0 or match the volume's existing encryption method.</span></span> <span data-ttu-id="1de0a-117">如果已使用有效的值啟用對應的群組原則設定，此參數的值必須是0或符合群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="1de0a-117">If the corresponding Group Policy setting has been enabled with a valid value, the value of this parameter must be 0 or match the Group Policy setting.</span></span>

<span data-ttu-id="1de0a-118">如果對應的群組原則設定無效，則會使用具有擴散器的預設值 AES 128。</span><span class="sxs-lookup"><span data-stu-id="1de0a-118">If the corresponding Group Policy setting is invalid, the default of AES 128 with diffuser is used.</span></span>



| <span data-ttu-id="1de0a-119">值</span><span class="sxs-lookup"><span data-stu-id="1de0a-119">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="1de0a-120">意義</span><span class="sxs-lookup"><span data-stu-id="1de0a-120">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="1de0a-121"><dt>**未指定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-121"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="1de0a-122">使用目前的群組原則設定（如果有的話），否則為預設加密方法。</span><span class="sxs-lookup"><span data-stu-id="1de0a-122">Use the current Group Policy setting, if available and valid, or the default encryption method otherwise.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="1de0a-123"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-123"><dt>1</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="1de0a-124">AES 128 與擴散器</span><span class="sxs-lookup"><span data-stu-id="1de0a-124">AES 128 WITH DIFFUSER</span></span><br/> <span data-ttu-id="1de0a-125">使用以擴散器層增強的進階加密標準 (AES) 演算法，以及使用 AES 金鑰大小128位，將磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-125">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 128 bits.</span></span><br/> |
| <dl> <span data-ttu-id="1de0a-126"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-126"><dt>2</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="1de0a-127">AES 256 與擴散器</span><span class="sxs-lookup"><span data-stu-id="1de0a-127">AES 256 WITH DIFFUSER</span></span><br/> <span data-ttu-id="1de0a-128">使用以擴散器層增強的進階加密標準 (AES) 演算法，以及使用 AES 金鑰大小256位，將磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-128">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 256 bits.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="1de0a-129"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-129"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="1de0a-130">使用進階加密標準 (AES) 演算法以及使用 AES 金鑰大小128位來加密磁片區。</span><span class="sxs-lookup"><span data-stu-id="1de0a-130">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 128 bits.</span></span><br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="1de0a-131"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-131"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="1de0a-132">使用進階加密標準 (AES) 演算法以及使用 AES 金鑰大小256位來加密磁片區。</span><span class="sxs-lookup"><span data-stu-id="1de0a-132">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 256 bits.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="1de0a-133">*EncryptionFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1de0a-133">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1de0a-134">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1de0a-134">Type: **uint32**</span></span>

<span data-ttu-id="1de0a-135">描述加密行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="1de0a-135">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="1de0a-136">**Windows 7、Windows Server 2008 R2、Windows Vista Enterprise 和 Windows Server 2008：** 此參數無法使用。</span><span class="sxs-lookup"><span data-stu-id="1de0a-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="1de0a-137">目前定義了下列位之32位的組合。</span><span class="sxs-lookup"><span data-stu-id="1de0a-137">A combination of 32 bits with the following bits currently defined.</span></span>



| <span data-ttu-id="1de0a-138">值</span><span class="sxs-lookup"><span data-stu-id="1de0a-138">Value</span></span>                                                                                  | <span data-ttu-id="1de0a-139">意義</span><span class="sxs-lookup"><span data-stu-id="1de0a-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1de0a-140"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-140"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="1de0a-141">開始新的加密程式時，以僅限資料的加密模式執行磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-141">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="1de0a-142">如果加密已暫停或停止，呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法會有效地繼續轉換，而且會忽略此位的值。</span><span class="sxs-lookup"><span data-stu-id="1de0a-142">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="1de0a-143">只有當 **Encrypt** 或 **EncryptAfterHardwareTest** 方法從完整解密的狀態、正在進行的解密或解密暫停狀態中啟動加密時，這一點才有作用。</span><span class="sxs-lookup"><span data-stu-id="1de0a-143">This bit only has effect when either the **Encrypt** or **EncryptAfterHardwareTest** methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="1de0a-144">如果這個位為零，表示未設定，則在開始新的加密程式時，將會執行完整模式轉換。</span><span class="sxs-lookup"><span data-stu-id="1de0a-144">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="1de0a-145"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-145"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="1de0a-146">執行磁片區可用空間的隨選抹除。</span><span class="sxs-lookup"><span data-stu-id="1de0a-146">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="1de0a-147">只有當磁片區目前未進行轉換或抹除，且處於「已加密」狀態時，才允許使用此位集呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1de0a-147">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="1de0a-148"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-148"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="1de0a-149">以同步方式執行要求的操作。</span><span class="sxs-lookup"><span data-stu-id="1de0a-149">Perform the requested operation synchronously.</span></span> <span data-ttu-id="1de0a-150">呼叫會封鎖，直到要求的作業完成或中斷為止。</span><span class="sxs-lookup"><span data-stu-id="1de0a-150">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="1de0a-151">只有 [**加密**](encrypt-win32-encryptablevolume.md) 方法支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="1de0a-151">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="1de0a-152">當呼叫 encryption 來繼續停止或中斷加密或抹除，或正在進行加密或抹除 **時，可以** 指定此旗標。</span><span class="sxs-lookup"><span data-stu-id="1de0a-152">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="1de0a-153">這可讓呼叫端繼續同步等候，直到程式完成或中斷為止。</span><span class="sxs-lookup"><span data-stu-id="1de0a-153">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1de0a-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="1de0a-154">Return value</span></span>

<span data-ttu-id="1de0a-155">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1de0a-155">Type: **uint32**</span></span>

<span data-ttu-id="1de0a-156">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1de0a-156">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="1de0a-157">這個方法會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="1de0a-157">This method returns immediately.</span></span> <span data-ttu-id="1de0a-158">如果磁片區已完全加密，但未傳回任何其他錯誤，則此方法會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1de0a-158">If the volume is already fully encrypted and no other errors are returned, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1de0a-159">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1de0a-159">Return code/value</span></span></th>
<th><span data-ttu-id="1de0a-160">Description</span><span class="sxs-lookup"><span data-stu-id="1de0a-160">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="1de0a-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-162">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1de0a-162">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="1de0a-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-164">已提供 <em>EncryptionMethod</em> 參數，但不在已知範圍內，或不符合目前的群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="1de0a-164">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="1de0a-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-166">磁片區不存在任何加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="1de0a-166">No encryption key exists for the volume.</span></span><br/> <span data-ttu-id="1de0a-167">請使用 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法來停用金鑰保護裝置，或使用下列其中一種方法來指定磁片區的金鑰保護裝置：</span><span class="sxs-lookup"><span data-stu-id="1de0a-167">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method, or use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="1de0a-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="1de0a-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-175">因為這部電腦已設定為伺服器叢集的一部分，所以無法將磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-175">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="1de0a-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-177">找不到類型為 &quot; tpm &quot; 、 &quot; tpm 和 Pin &quot; 、 &quot; Tpm 和 pin 碼、啟動金鑰 &quot; 、 &quot; tpm 和啟動金鑰 &quot; 或 &quot; 外部金鑰 &quot; 的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="1de0a-177">No key protectors of the type &quot;TPM&quot;, &quot;TPM And PIN&quot;, &quot;TPM And PIN And Startup Key&quot;, &quot;TPM And Startup Key&quot;, or &quot;External Key&quot; can be found.</span></span> <span data-ttu-id="1de0a-178">硬體測試只牽涉到先前的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="1de0a-178">The hardware test only involves the previous key protectors.</span></span><br/> <span data-ttu-id="1de0a-179">如果您仍想要執行硬體測試，您必須使用下列其中一種方法來指定磁片區的金鑰保護裝置：</span><span class="sxs-lookup"><span data-stu-id="1de0a-179">If you still want to run a hardware test, you must use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="1de0a-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="1de0a-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-187">磁片區已部分或完整加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-187">The volume is partially or fully encrypted.</span></span><br/> <span data-ttu-id="1de0a-188">硬體測試會在進行加密之前套用。</span><span class="sxs-lookup"><span data-stu-id="1de0a-188">The hardware test applies before encryption occurs.</span></span> <span data-ttu-id="1de0a-189">如果您仍想要執行測試，請先使用 [ <a href="decrypt-win32-encryptablevolume.md"><strong>解密</strong></a> ] 方法，然後使用下列其中一種方法來新增金鑰保護裝置：</span><span class="sxs-lookup"><span data-stu-id="1de0a-189">If you still want to run the test, first use the <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> method and then use one of the following methods to add key protectors:</span></span>
<ul>
<li><span data-ttu-id="1de0a-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="1de0a-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1de0a-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="1de0a-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-196">磁片區是資料磁片區。</span><span class="sxs-lookup"><span data-stu-id="1de0a-196">The volume is a data volume.</span></span><br/> <span data-ttu-id="1de0a-197">硬體測試只適用于可以啟動作業系統的磁片區。</span><span class="sxs-lookup"><span data-stu-id="1de0a-197">The hardware test applies only to volumes that can start the operating system.</span></span> <span data-ttu-id="1de0a-198">在目前啟動的作業系統磁片區上執行此方法。</span><span class="sxs-lookup"><span data-stu-id="1de0a-198">Run this method on the currently started operating system volume.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="1de0a-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C) </dt> </span><span class="sxs-lookup"><span data-stu-id="1de0a-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="1de0a-200">未指定類型數值密碼的金鑰保護裝置 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="1de0a-200">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="1de0a-201">群組原則需要將修復資訊備份到 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="1de0a-201">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="1de0a-202">若要加入至少一個該類型的金鑰保護裝置，請使用 <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="1de0a-202">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1de0a-203">備註</span><span class="sxs-lookup"><span data-stu-id="1de0a-203">Remarks</span></span>

<span data-ttu-id="1de0a-204">當您使用這個方法時，如果沒有第二個選擇性參數 (根據 Windows 7 和 Windows Vista Enterprise 定義) ，方法一律會起始完整模式轉換，以保持回溯相容的行為。</span><span class="sxs-lookup"><span data-stu-id="1de0a-204">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="1de0a-205">如此一來，在 Windows 8 和 Windows Server 2012 中新增第二個選擇性參數，就不會中斷現有應用程式和腳本的安全性期望。</span><span class="sxs-lookup"><span data-stu-id="1de0a-205">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="1de0a-206">與 [**Encrypt**](encrypt-win32-encryptablevolume.md) 方法不同的是，此方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1de0a-206">Unlike the [**Encrypt**](encrypt-win32-encryptablevolume.md) method, this method does the following:</span></span>

-   <span data-ttu-id="1de0a-207">測試 TPM 是否能夠在有 TPM 相關的金鑰保護裝置時解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="1de0a-207">Tests whether the TPM will be able to unlock the volume, if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="1de0a-208">測試電腦是否可以在啟動期間讀取包含外部金鑰檔案的 USB 快閃磁片磁碟機（如果磁片區將由外部金鑰解除鎖定， (包括啟動金鑰) ）。</span><span class="sxs-lookup"><span data-stu-id="1de0a-208">Tests whether the computer can read a USB flash drive that contains an external key file during start, if the volume will be unlocked by an external key (including a startup key).</span></span>
-   <span data-ttu-id="1de0a-209">需要重新開機電腦，才能執行硬體測試。</span><span class="sxs-lookup"><span data-stu-id="1de0a-209">Requires a computer restart to run the hardware test.</span></span>
-   <span data-ttu-id="1de0a-210">只有當硬體測試成功時，才開始加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-210">Begins encryption only if the hardware test succeeds.</span></span>
-   <span data-ttu-id="1de0a-211">無法用於資料磁片區、部分或完整加密的磁片區，或繼續加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-211">Cannot be used on a data volume, on a partially or fully encrypted volume, or to resume encryption.</span></span>

<span data-ttu-id="1de0a-212">執行此方法之前，請使用下列方法來建立相關的金鑰保護裝置：</span><span class="sxs-lookup"><span data-stu-id="1de0a-212">Before running this method, use the following methods to create the related key protectors:</span></span>

-   [<span data-ttu-id="1de0a-213">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="1de0a-213">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="1de0a-214">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="1de0a-214">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="1de0a-215">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="1de0a-215">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="1de0a-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="1de0a-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="1de0a-217">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="1de0a-217">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="1de0a-218">執行此方法之後，請採取下列額外步驟：</span><span class="sxs-lookup"><span data-stu-id="1de0a-218">After running this method, take these additional steps:</span></span>

1.  <span data-ttu-id="1de0a-219">將包含外部金鑰檔案的 USB 快閃磁片磁碟機插入電腦。</span><span class="sxs-lookup"><span data-stu-id="1de0a-219">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="1de0a-220">只有當磁片區具有「外部金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置時，才適用此步驟。</span><span class="sxs-lookup"><span data-stu-id="1de0a-220">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="1de0a-221">重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="1de0a-221">Restart the computer.</span></span>

<span data-ttu-id="1de0a-222">電腦重新開機時，會自動執行硬體測試。</span><span class="sxs-lookup"><span data-stu-id="1de0a-222">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="1de0a-223">如果硬體測試成功，就會開始加密。</span><span class="sxs-lookup"><span data-stu-id="1de0a-223">Encryption begins if the hardware test succeeds.</span></span> <span data-ttu-id="1de0a-224">否則，請嘗試解決任何硬體失敗。</span><span class="sxs-lookup"><span data-stu-id="1de0a-224">Otherwise, attempt to resolve any hardware failures.</span></span> <span data-ttu-id="1de0a-225">重新開機電腦後執行 [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) ，以取得測試結果。</span><span class="sxs-lookup"><span data-stu-id="1de0a-225">Run [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) after restarting the computer to get test results.</span></span>

<span data-ttu-id="1de0a-226">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1de0a-226">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1de0a-227">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1de0a-227">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1de0a-228">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1de0a-228">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1de0a-229">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="1de0a-229">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1de0a-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="1de0a-230">Requirements</span></span>



| <span data-ttu-id="1de0a-231">需求</span><span class="sxs-lookup"><span data-stu-id="1de0a-231">Requirement</span></span> | <span data-ttu-id="1de0a-232">值</span><span class="sxs-lookup"><span data-stu-id="1de0a-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de0a-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1de0a-233">Minimum supported client</span></span><br/> | <span data-ttu-id="1de0a-234">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1de0a-234">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1de0a-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1de0a-235">Minimum supported server</span></span><br/> | <span data-ttu-id="1de0a-236">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1de0a-236">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1de0a-237">命名空間</span><span class="sxs-lookup"><span data-stu-id="1de0a-237">Namespace</span></span><br/>                | <span data-ttu-id="1de0a-238">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1de0a-238">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1de0a-239">MOF</span><span class="sxs-lookup"><span data-stu-id="1de0a-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1de0a-240"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="1de0a-240"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1de0a-241">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1de0a-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de0a-242">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="1de0a-242">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
