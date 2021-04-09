---
description: 指出磁片區上的加密或解密狀態。
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Win32_EncryptableVolume 類別的 GetConversionStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847877"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f90f0-103">Win32 EncryptableVolume 類別的 GetConversionStatus 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f90f0-103">GetConversionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f90f0-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetConversionStatus** 方法會指出磁片區上的加密或解密狀態。</span><span class="sxs-lookup"><span data-stu-id="f90f0-104">The **GetConversionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the status of the encryption or decryption on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f90f0-105">語法</span><span class="sxs-lookup"><span data-stu-id="f90f0-105">Syntax</span></span>


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a><span data-ttu-id="f90f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="f90f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f90f0-107">*ConversionStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-107">*ConversionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f90f0-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f90f0-108">Type: **uint32**</span></span>

<span data-ttu-id="f90f0-109">磁片區加密或解密狀態。</span><span class="sxs-lookup"><span data-stu-id="f90f0-109">Volume encryption or decryption status.</span></span> <span data-ttu-id="f90f0-110">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f90f0-110">This can be one of the following values.</span></span>



| <span data-ttu-id="f90f0-111">值</span><span class="sxs-lookup"><span data-stu-id="f90f0-111">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="f90f0-112">意義</span><span class="sxs-lookup"><span data-stu-id="f90f0-112">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <span data-ttu-id="f90f0-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span></span> </dl>                         | <span data-ttu-id="f90f0-114">針對標準硬碟 (HDD) ，磁片區已完全解密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-114">For a standard hard drive (HDD), the volume is fully decrypted.</span></span><br/> <span data-ttu-id="f90f0-115">針對硬體加密硬碟 (EHDD) ，磁片區會永久解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="f90f0-115">For a hardware encrypted hard drive (EHDD), the volume is perpetually unlocked.</span></span><br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <span data-ttu-id="f90f0-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="f90f0-117">若為標準硬碟 (HDD) ，磁片區會完整加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-117">For a standard hard drive (HDD), the volume is fully encrypted.</span></span><br/> <span data-ttu-id="f90f0-118">針對硬體加密硬碟 (EHDD) ，磁片區未永久解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="f90f0-118">For a hardware encrypted hard drive (EHDD), the volume is not perpetually unlocked.</span></span><br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="f90f0-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="f90f0-120">磁片區已部分加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-120">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="f90f0-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="f90f0-122">磁片區已部分加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-122">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <span data-ttu-id="f90f0-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="f90f0-124">磁片區已在加密進度期間暫停。</span><span class="sxs-lookup"><span data-stu-id="f90f0-124">The volume has been paused during the encryption progress.</span></span> <span data-ttu-id="f90f0-125">磁片區已部分加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-125">The volume is partially encrypted.</span></span><br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <span data-ttu-id="f90f0-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="f90f0-127">磁片區已在解密進度期間暫停。</span><span class="sxs-lookup"><span data-stu-id="f90f0-127">The volume has been paused during the decryption progress.</span></span> <span data-ttu-id="f90f0-128">磁片區已部分加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-128">The volume is partially encrypted.</span></span><br/>                                                                  |



 

</dd> <dt>

<span data-ttu-id="f90f0-129">*EncryptionPercentage* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-129">*EncryptionPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f90f0-130">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f90f0-130">Type: **uint32**</span></span>

<span data-ttu-id="f90f0-131">加密的磁片區百分比。</span><span class="sxs-lookup"><span data-stu-id="f90f0-131">Percentage of the volume that is encrypted.</span></span> <span data-ttu-id="f90f0-132">這是從0到100（含）的整數。</span><span class="sxs-lookup"><span data-stu-id="f90f0-132">This is an integer from 0 to 100 inclusive.</span></span>

<span data-ttu-id="f90f0-133">由於數位四捨五入，加密百分比0或100不一定表示磁片已完全解密或完全加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-133">Due to rounding of numbers, an encryption percentage of 0 or 100 does not necessarily indicate that the disk is fully decrypted or fully encrypted.</span></span> <span data-ttu-id="f90f0-134">請一律使用 *ConversionStatus* 來判斷磁片是否已完全解密或完全加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-134">Always use *ConversionStatus* to determine whether the disk is in fact fully decrypted or fully encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="f90f0-135">*EncryptionFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-135">*EncryptionFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f90f0-136">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f90f0-136">Type: **uint32**</span></span>

<span data-ttu-id="f90f0-137">描述加密行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="f90f0-137">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="f90f0-138">目前定義了下列位的32位組合。</span><span class="sxs-lookup"><span data-stu-id="f90f0-138">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="f90f0-139">值</span><span class="sxs-lookup"><span data-stu-id="f90f0-139">Value</span></span>                                                                                  | <span data-ttu-id="f90f0-140">意義</span><span class="sxs-lookup"><span data-stu-id="f90f0-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f90f0-141"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-141"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="f90f0-142">開始新的加密程式時，以僅限資料的加密模式執行磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="f90f0-142">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="f90f0-143">如果加密已暫停或停止，呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法會有效地繼續轉換，而且會忽略此位的值。</span><span class="sxs-lookup"><span data-stu-id="f90f0-143">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="f90f0-144">只有當 **Encrypt** 或 [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) 方法從完整解密的狀態、正在進行的解密或解密暫停狀態中啟動加密時，這一點才有作用。</span><span class="sxs-lookup"><span data-stu-id="f90f0-144">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="f90f0-145">如果這個位為零，表示未設定，則在開始新的加密程式時，將會執行完整模式轉換。</span><span class="sxs-lookup"><span data-stu-id="f90f0-145">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="f90f0-146"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-146"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="f90f0-147">執行磁片區可用空間的隨選抹除。</span><span class="sxs-lookup"><span data-stu-id="f90f0-147">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="f90f0-148">只有當磁片區目前未進行轉換或抹除，且處於「已加密」狀態時，才允許使用此位集呼叫 [**加密**](encrypt-win32-encryptablevolume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f90f0-148">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f90f0-149"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-149"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="f90f0-150">以同步方式執行要求的操作。</span><span class="sxs-lookup"><span data-stu-id="f90f0-150">Perform the requested operation synchronously.</span></span> <span data-ttu-id="f90f0-151">呼叫會封鎖，直到要求的作業完成或中斷為止。</span><span class="sxs-lookup"><span data-stu-id="f90f0-151">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="f90f0-152">只有 [**加密**](encrypt-win32-encryptablevolume.md) 方法支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="f90f0-152">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="f90f0-153">當呼叫 encryption 來繼續停止或中斷加密或抹除，或正在進行加密或抹除 **時，可以** 指定此旗標。</span><span class="sxs-lookup"><span data-stu-id="f90f0-153">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="f90f0-154">這可讓呼叫端繼續同步等候，直到程式完成或中斷為止。</span><span class="sxs-lookup"><span data-stu-id="f90f0-154">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="f90f0-155">*WipingStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-155">*WipingStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f90f0-156">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f90f0-156">Type: **uint32**</span></span>

<span data-ttu-id="f90f0-157">可用空間抹除狀態。</span><span class="sxs-lookup"><span data-stu-id="f90f0-157">Free space wiping status.</span></span> <span data-ttu-id="f90f0-158">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f90f0-158">This can be one of the following values.</span></span>



| <span data-ttu-id="f90f0-159">值</span><span class="sxs-lookup"><span data-stu-id="f90f0-159">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="f90f0-160">意義</span><span class="sxs-lookup"><span data-stu-id="f90f0-160">Meaning</span></span>                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <span data-ttu-id="f90f0-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="f90f0-162">尚未抹除可用空間。</span><span class="sxs-lookup"><span data-stu-id="f90f0-162">The free space has not been wiped.</span></span><br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <span data-ttu-id="f90f0-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span></span> </dl>                                             | <span data-ttu-id="f90f0-164">已抹除可用空間。</span><span class="sxs-lookup"><span data-stu-id="f90f0-164">The free space has been wiped.</span></span><br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <span data-ttu-id="f90f0-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="f90f0-166">正在抹除的可用空間正在進行中。</span><span class="sxs-lookup"><span data-stu-id="f90f0-166">Free space wiping is currently in progress.</span></span><br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <span data-ttu-id="f90f0-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="f90f0-168">已暫停釋放空間。</span><span class="sxs-lookup"><span data-stu-id="f90f0-168">Free space wiping has been paused.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="f90f0-169">*WipingPercentage* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-169">*WipingPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f90f0-170">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f90f0-170">Type: **uint32**</span></span>

<span data-ttu-id="f90f0-171">從0到100的值，指定已抹除的可用空間百分比。</span><span class="sxs-lookup"><span data-stu-id="f90f0-171">A value from 0 to 100 that specifies the percentage of free space that has been wiped.</span></span>

</dd> <dt>

<span data-ttu-id="f90f0-172">*PrecisionFactor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-172">*PrecisionFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f90f0-173">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f90f0-173">Type: **uint32**</span></span>

<span data-ttu-id="f90f0-174">從0到4指定精確度層級的值。</span><span class="sxs-lookup"><span data-stu-id="f90f0-174">A value from 0 to 4 that specifies the precision level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f90f0-175">傳回值</span><span class="sxs-lookup"><span data-stu-id="f90f0-175">Return value</span></span>

<span data-ttu-id="f90f0-176">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f90f0-176">Type: **uint32**</span></span>

<span data-ttu-id="f90f0-177">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f90f0-177">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f90f0-178">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f90f0-178">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f90f0-179">Description</span><span class="sxs-lookup"><span data-stu-id="f90f0-179">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f90f0-180"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-180"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f90f0-181">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="f90f0-181">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="f90f0-182"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-182"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="f90f0-183">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="f90f0-183">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="f90f0-184">備註</span><span class="sxs-lookup"><span data-stu-id="f90f0-184">Remarks</span></span>

<span data-ttu-id="f90f0-185">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f90f0-185">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f90f0-186">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f90f0-186">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f90f0-187">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f90f0-187">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f90f0-188">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="f90f0-188">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f90f0-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="f90f0-189">Requirements</span></span>



| <span data-ttu-id="f90f0-190">需求</span><span class="sxs-lookup"><span data-stu-id="f90f0-190">Requirement</span></span> | <span data-ttu-id="f90f0-191">值</span><span class="sxs-lookup"><span data-stu-id="f90f0-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f90f0-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f90f0-192">Minimum supported client</span></span><br/> | <span data-ttu-id="f90f0-193">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-193">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f90f0-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f90f0-194">Minimum supported server</span></span><br/> | <span data-ttu-id="f90f0-195">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f90f0-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f90f0-196">命名空間</span><span class="sxs-lookup"><span data-stu-id="f90f0-196">Namespace</span></span><br/>                | <span data-ttu-id="f90f0-197">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f90f0-197">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f90f0-198">MOF</span><span class="sxs-lookup"><span data-stu-id="f90f0-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f90f0-199"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="f90f0-199"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f90f0-200">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f90f0-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f90f0-201">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="f90f0-201">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
