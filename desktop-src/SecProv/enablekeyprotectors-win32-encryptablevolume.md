---
description: 啟用或繼續所有已停用或已暫止的金鑰保護裝置。
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Win32_EncryptableVolume 類別的 EnableKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972831"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c56b6-103">Win32 EncryptableVolume 類別的 EnableKeyProtectors 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c56b6-103">EnableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c56b6-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **EnableKeyProtectors** 方法會啟用或繼續所有已停用或已暫止的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c56b6-104">The **EnableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enables or resumes all disabled or suspended key protectors.</span></span> <span data-ttu-id="c56b6-105">您可以使用這個方法來重新啟用或繼續加密磁片區上的 BitLocker 保護。</span><span class="sxs-lookup"><span data-stu-id="c56b6-105">You can use this method to reenable or resume BitLocker protection on an encrypted volume.</span></span> <span data-ttu-id="c56b6-106">這個方法可確保磁片區的加密金鑰不會在硬碟上以純文字公開。</span><span class="sxs-lookup"><span data-stu-id="c56b6-106">This method ensures that the volume's encryption key is not exposed in the clear on the hard disk.</span></span>

> [!Note]  
> <span data-ttu-id="c56b6-107">如果光碟支援硬體加密，頻外狀態會從「永遠解除鎖定」轉換成「已解除鎖定」。</span><span class="sxs-lookup"><span data-stu-id="c56b6-107">If the disc supports hardware encryption, the band state transitions to "unlocked" from "always unlocked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c56b6-108">語法</span><span class="sxs-lookup"><span data-stu-id="c56b6-108">Syntax</span></span>


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="c56b6-109">參數</span><span class="sxs-lookup"><span data-stu-id="c56b6-109">Parameters</span></span>

<span data-ttu-id="c56b6-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c56b6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c56b6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c56b6-111">Return value</span></span>

<span data-ttu-id="c56b6-112">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c56b6-112">Type: **uint32**</span></span>

<span data-ttu-id="c56b6-113">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c56b6-113">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="c56b6-114">如果已啟用金鑰保護裝置，而且沒有發生其他錯誤，則此方法會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c56b6-114">If key protectors are already enabled and no other errors occur, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c56b6-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c56b6-115">Return code/value</span></span></th>
<th><span data-ttu-id="c56b6-116">Description</span><span class="sxs-lookup"><span data-stu-id="c56b6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="c56b6-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0) </dt> </span><span class="sxs-lookup"><span data-stu-id="c56b6-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="c56b6-118">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="c56b6-118">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c56b6-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007) </dt> </span><span class="sxs-lookup"><span data-stu-id="c56b6-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span></span></dl></td>
<td><span data-ttu-id="c56b6-120">磁片區上不存在任何金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c56b6-120">No key protectors exist on the volume.</span></span> <span data-ttu-id="c56b6-121">使用下列其中一種方法來指定磁片區的金鑰保護裝置：</span><span class="sxs-lookup"><span data-stu-id="c56b6-121">Use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="c56b6-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="c56b6-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="c56b6-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c56b6-131"><dt><strong>FVE_E_NOT_ACTI加值稅ED</strong></dt> <dt>2150694920 (0x80310008) </dt> </span><span class="sxs-lookup"><span data-stu-id="c56b6-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span></span></dl></td>
<td><span data-ttu-id="c56b6-132">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="c56b6-132">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c56b6-133">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="c56b6-133">Add a key protector to enable BitLocker.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c56b6-134">備註</span><span class="sxs-lookup"><span data-stu-id="c56b6-134">Remarks</span></span>

<span data-ttu-id="c56b6-135">如果磁片區已完全加密，則成功執行此方法可確保磁片區受到保護。</span><span class="sxs-lookup"><span data-stu-id="c56b6-135">If the volume is fully encrypted, successfully running this method ensures that the volume is protected.</span></span> <span data-ttu-id="c56b6-136">如果磁片區已部分加密，則成功執行此方法意味著磁片區會在完全加密時受到保護。</span><span class="sxs-lookup"><span data-stu-id="c56b6-136">If the volume is partially encrypted, successfully running this method implies that the volume will be protected when it becomes fully encrypted.</span></span> <span data-ttu-id="c56b6-137">如需詳細資訊，請參閱 [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c56b6-137">For more information, see the [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="c56b6-138">如果磁片區有以 TPM 為基礎的金鑰保護裝置，則成功執行此方法也會重新整理這些保護裝置，以便 TPM 針對平臺上的目前啟動服務進行驗證。</span><span class="sxs-lookup"><span data-stu-id="c56b6-138">If TPM-based key protectors exist for the volume, successfully running this method also refreshes these protectors so that the TPM validates against the current startup services on the platform.</span></span> <span data-ttu-id="c56b6-139">換句話說，您要判斷目前的電腦狀態是 TPM 在未來電腦重新開機時所要檢查的正確狀態。</span><span class="sxs-lookup"><span data-stu-id="c56b6-139">In other words, you are asserting that the current computer state is the correct state that the TPM will check against on future computer restarts.</span></span>

<span data-ttu-id="c56b6-140">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c56b6-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c56b6-141">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c56b6-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c56b6-142">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c56b6-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c56b6-143">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="c56b6-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c56b6-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="c56b6-144">Requirements</span></span>



| <span data-ttu-id="c56b6-145">需求</span><span class="sxs-lookup"><span data-stu-id="c56b6-145">Requirement</span></span> | <span data-ttu-id="c56b6-146">值</span><span class="sxs-lookup"><span data-stu-id="c56b6-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56b6-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c56b6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c56b6-148">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c56b6-148">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c56b6-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c56b6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c56b6-150">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c56b6-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c56b6-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="c56b6-151">Namespace</span></span><br/>                | <span data-ttu-id="c56b6-152">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c56b6-152">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c56b6-153">MOF</span><span class="sxs-lookup"><span data-stu-id="c56b6-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c56b6-154"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="c56b6-154"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56b6-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c56b6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56b6-156">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="c56b6-156">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-157">**DisableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="c56b6-157">**DisableKeyProtectors**</span></span>](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-158">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="c56b6-158">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-159">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="c56b6-159">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-160">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="c56b6-160">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-161">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="c56b6-161">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-162">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="c56b6-162">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-163">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="c56b6-163">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-164">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="c56b6-164">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="c56b6-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c56b6-166">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="c56b6-166">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
