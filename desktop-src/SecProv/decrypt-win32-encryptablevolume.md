---
description: 開始解密完整加密的磁片區，或繼續解密部分加密的磁片區。
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: 'Win32_EncryptableVolume 類別的解密方法 (Infocard) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849450"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="24798-103">Win32 EncryptableVolume 類別的解密方法 \_</span><span class="sxs-lookup"><span data-stu-id="24798-103">Decrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="24798-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **解密** 方法會開始解密完整加密的磁片區，或繼續解密部分加密的磁片區。</span><span class="sxs-lookup"><span data-stu-id="24798-104">The **Decrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.</span></span>

<span data-ttu-id="24798-105">當解密暫停或進行中時，此方法的行為與 [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)相同。</span><span class="sxs-lookup"><span data-stu-id="24798-105">When decryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="24798-106">當加密暫停或進行中時，此方法會還原加密並開始解密。</span><span class="sxs-lookup"><span data-stu-id="24798-106">When encryption is paused or in-progress, this method reverts the encryption and begins decryption.</span></span> <span data-ttu-id="24798-107">解密完成之後，這個磁片區上的所有金鑰保護裝置都會從系統中移除，而磁片區會轉換成標準 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="24798-107">After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.</span></span>

> [!Note]  
> <span data-ttu-id="24798-108">如果光碟已加密硬體，則 **解密** 方法會將頻外狀態設為「永遠解除鎖定」、移除所有相關聯的中繼資料，以及將磁片磁碟機的安全識別碼設為零。</span><span class="sxs-lookup"><span data-stu-id="24798-108">If the disc is hardware encrypted, the **Decrypt** method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="24798-109">語法</span><span class="sxs-lookup"><span data-stu-id="24798-109">Syntax</span></span>


```mof
uint32 Decrypt();
```



## <a name="parameters"></a><span data-ttu-id="24798-110">參數</span><span class="sxs-lookup"><span data-stu-id="24798-110">Parameters</span></span>

<span data-ttu-id="24798-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="24798-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24798-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="24798-112">Return value</span></span>

<span data-ttu-id="24798-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="24798-113">Type: **uint32**</span></span>

<span data-ttu-id="24798-114">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24798-114">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="24798-115">這個方法會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="24798-115">This method returns immediately.</span></span> <span data-ttu-id="24798-116">如果磁片區已經完全解密，而且沒有其他錯誤存在，這個方法會傳回0。</span><span class="sxs-lookup"><span data-stu-id="24798-116">If the volume is already fully decrypted and no other errors exist, this method returns 0.</span></span>



| <span data-ttu-id="24798-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="24798-117">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="24798-118">Description</span><span class="sxs-lookup"><span data-stu-id="24798-118">Description</span></span>                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24798-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="24798-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="24798-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="24798-120">The method was successful.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="24798-121"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="24798-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>      | <span data-ttu-id="24798-122">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="24798-122">The volume is locked.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="24798-123"><dt>**FVE \_E \_ 再次 \_ 已啟用**</dt> <dt>2150694953 (0x80310029)</dt></span><span class="sxs-lookup"><span data-stu-id="24798-123"><dt>**FVE\_E\_AUTOUNLOCK\_ENABLED**</dt> <dt>2150694953 (0x80310029)</dt></span></span> </dl> | <span data-ttu-id="24798-124">此磁片區無法解密，因為可用來自動解除鎖定資料磁片區的金鑰可以使用。</span><span class="sxs-lookup"><span data-stu-id="24798-124">This volume cannot be decrypted because keys used to automatically unlock data volumes are available.</span></span> <br/> <span data-ttu-id="24798-125">使用 [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) 來移除這些金鑰。</span><span class="sxs-lookup"><span data-stu-id="24798-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove these keys.</span></span><br/> |



 

## <a name="security-considerations"></a><span data-ttu-id="24798-126">安全性考量</span><span class="sxs-lookup"><span data-stu-id="24798-126">Security Considerations</span></span>

<span data-ttu-id="24798-127">呼叫 **解密** 方法會讓資料保持未受保護。</span><span class="sxs-lookup"><span data-stu-id="24798-127">Calling the **Decrypt** method leaves data unprotected.</span></span>

<span data-ttu-id="24798-128">如果在使用此方法之前，磁片區的保護狀態為 1 () 保護，此方法的成功完成會將保護狀態變更為 0 (保護關閉) ，因為依定義，部分加密的磁片區不受保護。</span><span class="sxs-lookup"><span data-stu-id="24798-128">If the protection status of the volume is 1 (PROTECTION ON) before this method is used, successful completion of this method changes the protection status to 0 (PROTECTION OFF), since by definition a partially encrypted volume is not protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="24798-129">備註</span><span class="sxs-lookup"><span data-stu-id="24798-129">Remarks</span></span>

<span data-ttu-id="24798-130">如果磁片區尚未完全解密，執行 **解密** 會導致 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 表示解密正在進行中，並顯示維持加密的磁片區百分比。</span><span class="sxs-lookup"><span data-stu-id="24798-130">If the volume is not already fully decrypted, running **Decrypt** causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.</span></span>

<span data-ttu-id="24798-131">如果在執行此方法之前，磁片區的保護狀態是「開啟」，則執行此方法會將保護狀態變更為「關閉」，因為依定義，部分加密的磁片區不受保護。</span><span class="sxs-lookup"><span data-stu-id="24798-131">If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.</span></span>

<span data-ttu-id="24798-132">如果這個方法是在目前正在執行的作業系統磁片區上執行，而這個作業系統磁片區是用來自動解除鎖定資料磁片區 (請參閱方法 [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) 您必須先呼叫方法 [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)。</span><span class="sxs-lookup"><span data-stu-id="24798-132">If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) you must first call the method [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span></span>

<span data-ttu-id="24798-133">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="24798-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24798-134">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="24798-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="24798-135">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="24798-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24798-136">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="24798-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24798-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="24798-137">Requirements</span></span>



| <span data-ttu-id="24798-138">需求</span><span class="sxs-lookup"><span data-stu-id="24798-138">Requirement</span></span> | <span data-ttu-id="24798-139">值</span><span class="sxs-lookup"><span data-stu-id="24798-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24798-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24798-140">Minimum supported client</span></span><br/> | <span data-ttu-id="24798-141">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24798-141">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="24798-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24798-142">Minimum supported server</span></span><br/> | <span data-ttu-id="24798-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24798-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="24798-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="24798-144">Namespace</span></span><br/>                | <span data-ttu-id="24798-145">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="24798-145">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="24798-146">標頭</span><span class="sxs-lookup"><span data-stu-id="24798-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="24798-147"><dt>Infocard。h</dt></span><span class="sxs-lookup"><span data-stu-id="24798-147"><dt>Infocard.h</dt></span></span> </dl>                   |
| <span data-ttu-id="24798-148">MOF</span><span class="sxs-lookup"><span data-stu-id="24798-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24798-149"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="24798-149"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24798-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24798-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24798-151">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="24798-151">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
