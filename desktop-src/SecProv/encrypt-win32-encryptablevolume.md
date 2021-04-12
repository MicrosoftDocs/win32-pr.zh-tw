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
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027440"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d7a7f-103">Win32 EncryptableVolume 類別的 Encrypt 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d7a7f-103">Encrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d7a7f-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **Encrypt** 方法會開始加密完整解密的磁片區，或繼續加密部分加密的磁片區。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-104">The **Encrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted volume, or resumes encryption of a partially encrypted volume.</span></span> <span data-ttu-id="d7a7f-105">當加密暫停或進行中時，此方法的行為與 [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)相同。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-105">When encryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="d7a7f-106">當解密暫停或進行中時，此方法會停止解密並開始加密。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-106">When decryption is paused or in-progress, this method stops the decryption and begins encryption.</span></span>

> [!Note]  
> <span data-ttu-id="d7a7f-107">如果磁片磁碟機已加密硬體，這個方法不會加密資料。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-107">If the drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="d7a7f-108">相反地，它會將頻外狀態從 [永遠解除鎖定] 設定為 [已解除鎖定]。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-108">Instead, it sets the band status to "unlocked" from "always unlocked".</span></span> <span data-ttu-id="d7a7f-109">如果頻外已鎖定、已解除鎖定或為唯讀，則會將磁片磁碟機視為已加密。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

<span data-ttu-id="d7a7f-110">**Windows Vista：** 不支援加密非目前執行中作業系統磁片區的磁片區。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-110">**Windows Vista:** Encryption of a volume other than the currently running operating system volume is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a7f-111">語法</span><span class="sxs-lookup"><span data-stu-id="d7a7f-111">Syntax</span></span>


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d7a7f-112">參數</span><span class="sxs-lookup"><span data-stu-id="d7a7f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a7f-113">*EncryptionMethod* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d7a7f-113">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7a7f-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d7a7f-114">Type: **uint32**</span></span>

<span data-ttu-id="d7a7f-115">不帶正負號的整數，指定用來加密磁片區的加密演算法和金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-115">An unsigned integer that specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="d7a7f-116">如果此參數大於零，且磁片區為部分或完整加密，則 *EncryptionMethod* 必須符合磁片區的現有加密方法。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-116">If this parameter is greater than zero and the volume is partially or fully encrypted, *EncryptionMethod* must match the volume's existing encryption method.</span></span> <span data-ttu-id="d7a7f-117">如果此參數大於零，且對應的群組原則設定是以有效的值啟用， *EncryptionMethod* 必須符合群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-117">If this parameter is greater than zero and the corresponding Group Policy setting is enabled with a valid value, *EncryptionMethod* must match the Group Policy setting.</span></span>

<span data-ttu-id="d7a7f-118">如需可能 EncryptionMethod 值的清單，請參閱 [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-118">For a list of possible EncryptionMethod values, see the [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="d7a7f-119">Windows 7 或更低的預設值為： 1 (\_ \_ 具有擴散器) 的 AES 128 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-119">Default value for Windows 7 or below is: 1 (AES\_128\_WITH\_DIFFUSER).</span></span>

<span data-ttu-id="d7a7f-120">Windows 8、Windows 8.1 或 1507 Windows 10 的預設值為： 3 (AES \_ 128) 。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-120">Default value for Windows 8, Windows 8.1 or Windows 10, version 1507 is: 3 (AES\_128).</span></span>

<span data-ttu-id="d7a7f-121">Windows 10 1511 版或更新版本的預設值為： 6 (XTS \_ AES \_ 128) 。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-121">Default value for Windows 10, version 1511 or above is: 6 (XTS\_AES\_128).</span></span>

</dd> <dt>

<span data-ttu-id="d7a7f-122">*EncryptionFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d7a7f-122">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7a7f-123">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d7a7f-123">Type: **uint32**</span></span>

<span data-ttu-id="d7a7f-124">描述加密行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-124">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="d7a7f-125">**Windows 7、Windows Server 2008 R2、Windows Vista Enterprise 和 Windows Server 2008：** 此參數無法使用。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="d7a7f-126">目前定義了下列位的32位組合。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-126">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="d7a7f-127">值</span><span class="sxs-lookup"><span data-stu-id="d7a7f-127">Value</span></span>                                                                                  | <span data-ttu-id="d7a7f-128">意義</span><span class="sxs-lookup"><span data-stu-id="d7a7f-128">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7a7f-129"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d7a7f-129"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="d7a7f-130">開始新的加密程式時，以僅限資料的加密模式執行磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-130">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="d7a7f-131">如果加密已暫停或停止，呼叫 **加密** 方法會有效地繼續轉換，而且會忽略此位的值。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-131">If encryption has been paused or stopped, calling the **Encrypt** method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="d7a7f-132">只有當 **Encrypt** 或 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法從完整解密的狀態、正在進行的解密或解密暫停狀態中啟動加密時，這一點才有作用。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-132">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="d7a7f-133">如果這個位為零，表示未設定，則在開始新的加密程式時，將會執行完整模式轉換。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-133">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="d7a7f-134"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d7a7f-134"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="d7a7f-135">執行磁片區可用空間的隨選抹除。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-135">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="d7a7f-136">只有當磁片區目前未進行轉換或抹除，且處於「已加密」狀態時，才允許使用此位集呼叫 **加密** 方法。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-136">Calling the **Encrypt** method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="d7a7f-137"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="d7a7f-137"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="d7a7f-138">以同步方式執行要求的操作。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-138">Perform the requested operation synchronously.</span></span> <span data-ttu-id="d7a7f-139">呼叫會封鎖，直到要求的作業完成或中斷為止。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-139">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="d7a7f-140">只有 **加密** 方法支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-140">This flag is only supported with the **Encrypt** method.</span></span> <span data-ttu-id="d7a7f-141">當呼叫 encryption 來繼續停止或中斷加密或抹除，或正在進行加密或抹除 **時，可以** 指定此旗標。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-141">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="d7a7f-142">這可讓呼叫端繼續同步等候，直到程式完成或中斷為止。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-142">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a7f-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7a7f-143">Return value</span></span>

<span data-ttu-id="d7a7f-144">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d7a7f-144">Type: **uint32**</span></span>

<span data-ttu-id="d7a7f-145">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-145">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="d7a7f-146">這個方法會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-146">This method returns immediately.</span></span> <span data-ttu-id="d7a7f-147">如果磁片區已完全加密，但未傳回任何其他錯誤，則此方法會傳回0。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-147">If the volume is already fully encrypted and no other errors are returned, this method returns 0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7a7f-148">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d7a7f-148">Return code/value</span></span></th>
<th><span data-ttu-id="d7a7f-149">Description</span><span class="sxs-lookup"><span data-stu-id="d7a7f-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="d7a7f-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0) </dt> </span><span class="sxs-lookup"><span data-stu-id="d7a7f-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="d7a7f-151">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-151">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d7a7f-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057) </dt> </span><span class="sxs-lookup"><span data-stu-id="d7a7f-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="d7a7f-153">已提供 <em>EncryptionMethod</em> 參數，但不在已知範圍內，或不符合目前的群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-153">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d7a7f-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E) </dt> </span><span class="sxs-lookup"><span data-stu-id="d7a7f-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="d7a7f-155">磁片區不存在任何加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-155">No encryption key exists for the volume.</span></span> <span data-ttu-id="d7a7f-156">使用 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法來停用金鑰保護裝置，或使用下列其中一種方法來指定磁片區的金鑰保護裝置：</span><span class="sxs-lookup"><span data-stu-id="d7a7f-156">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="d7a7f-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7a7f-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="d7a7f-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7a7f-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="d7a7f-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7a7f-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="d7a7f-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7a7f-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="d7a7f-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7a7f-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="d7a7f-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="d7a7f-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul><span data-ttu-id="d7a7f-163">
<strong>Windows Vista：</strong> 當磁片區不存在任何加密金鑰時，會改為傳回 ERROR_INVALID_OPERATION。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-163">
<strong>Windows Vista:</strong> When no encryption key exists for the volume, ERROR_INVALID_OPERATION is returned instead.</span></span> <span data-ttu-id="d7a7f-164">十進位值是4317，而十六進位值為0x10DD。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-164">The decimal value is 4317 and the hexadecimal value is 0x10DD.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d7a7f-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D) </dt> </span><span class="sxs-lookup"><span data-stu-id="d7a7f-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span></span></dl></td>
<td><span data-ttu-id="d7a7f-166">提供的加密方法與部分或完整加密磁片區的加密方法不相符。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-166">The provided encryption method does not match that of the partially or fully encrypted volume.</span></span> <span data-ttu-id="d7a7f-167">若要繼續加密，請將 <em>EncryptionMethod</em> 參數保留空白或使用零值。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-167">To continue encryption, leave the <em>EncryptionMethod</em> parameter blank or use a value of zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d7a7f-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E) </dt> </span><span class="sxs-lookup"><span data-stu-id="d7a7f-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="d7a7f-169">因為這部電腦已設定為伺服器叢集的一部分，所以無法將磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-169">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d7a7f-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000) </dt> </span><span class="sxs-lookup"><span data-stu-id="d7a7f-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span></span></dl></td>
<td><span data-ttu-id="d7a7f-171">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-171">The volume is locked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d7a7f-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C) </dt> </span><span class="sxs-lookup"><span data-stu-id="d7a7f-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="d7a7f-173">未指定類型數值密碼的金鑰保護裝置 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-173">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="d7a7f-174">群組原則需要將修復資訊備份到 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-174">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="d7a7f-175">若要加入至少一個該類型的金鑰保護裝置，請使用 <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-175">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d7a7f-176">備註</span><span class="sxs-lookup"><span data-stu-id="d7a7f-176">Remarks</span></span>

<span data-ttu-id="d7a7f-177">當您使用這個方法時，如果沒有第二個選擇性參數 (根據 Windows 7 和 Windows Vista Enterprise 定義) ，方法一律會起始完整模式轉換，以保持回溯相容的行為。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-177">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="d7a7f-178">如此一來，在 Windows 8 和 Windows Server 2012 中新增第二個選擇性參數，就不會中斷現有應用程式和腳本的安全性期望。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-178">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="d7a7f-179">您可以呼叫 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 來判斷加密是否正在進行中，以及已加密之磁片區的百分比。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-179">You can call [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to determine whether encryption is in progress and the percentage of the volume that has been encrypted.</span></span>

<span data-ttu-id="d7a7f-180">當磁片區完整加密，且已新增並啟用金鑰保護裝置時，磁片區的保護狀態會變更為「開啟」。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-180">After the volume is fully encrypted and if key protectors have been added and enabled, the protection status for the volume changes to "on".</span></span>

<span data-ttu-id="d7a7f-181">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d7a7f-182">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-182">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d7a7f-183">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d7a7f-184">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-184">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a7f-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7a7f-185">Requirements</span></span>



| <span data-ttu-id="d7a7f-186">需求</span><span class="sxs-lookup"><span data-stu-id="d7a7f-186">Requirement</span></span> | <span data-ttu-id="d7a7f-187">值</span><span class="sxs-lookup"><span data-stu-id="d7a7f-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a7f-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7a7f-188">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a7f-189">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7a7f-189">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7a7f-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7a7f-190">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a7f-191">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7a7f-191">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7a7f-192">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7a7f-192">Namespace</span></span><br/>                | <span data-ttu-id="d7a7f-193">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="d7a7f-193">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d7a7f-194">MOF</span><span class="sxs-lookup"><span data-stu-id="d7a7f-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7a7f-195"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7a7f-195"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a7f-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7a7f-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a7f-197">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d7a7f-197">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
