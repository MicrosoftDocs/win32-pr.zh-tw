---
description: 指出磁片區及其加密金鑰是否受到保護。
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Win32_EncryptableVolume 類別的 GetProtectionStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690099"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ece63-103">Win32 EncryptableVolume 類別的 GetProtectionStatus 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ece63-103">GetProtectionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ece63-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetProtectionStatus** 方法會指出如果有任何) 受到保護，是否 (磁片區和其加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="ece63-104">The **GetProtectionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume and its encryption key (if any) are secured.</span></span>

<span data-ttu-id="ece63-105">如果磁片區未加密或部分加密，或磁片區的加密金鑰可在硬碟上以純文字方式提供，則會關閉保護。</span><span class="sxs-lookup"><span data-stu-id="ece63-105">Protection is off if a volume is unencrypted or partially encrypted, or if the volume's encryption key is available in the clear on the hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece63-106">語法</span><span class="sxs-lookup"><span data-stu-id="ece63-106">Syntax</span></span>


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="ece63-107">參數</span><span class="sxs-lookup"><span data-stu-id="ece63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ece63-108">*ProtectionStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ece63-108">*ProtectionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ece63-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ece63-109">Type: **uint32**</span></span>

<span data-ttu-id="ece63-110">指定是否將磁片區和加密金鑰 (（如果有任何) 受到保護）。</span><span class="sxs-lookup"><span data-stu-id="ece63-110">Specifies whether the volume and the encryption key (if any) are secured.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ece63-111">值</span><span class="sxs-lookup"><span data-stu-id="ece63-111">Value</span></span></th>
<th><span data-ttu-id="ece63-112">意義</span><span class="sxs-lookup"><span data-stu-id="ece63-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <span data-ttu-id="ece63-113">未<dt><strong>受保護</strong></dt>的<dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="ece63-113"><dt><strong>Unprotected</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="ece63-114">關閉保護</span><span class="sxs-lookup"><span data-stu-id="ece63-114">PROTECTION OFF</span></span><br/> <span data-ttu-id="ece63-115">針對標準 HDD：</span><span class="sxs-lookup"><span data-stu-id="ece63-115">For a standard HDD:</span></span><br/> <span data-ttu-id="ece63-116">磁片區未加密、部分加密，或磁片區的加密金鑰在硬碟上是以純文字形式提供。</span><span class="sxs-lookup"><span data-stu-id="ece63-116">The volume is unencrypted, partially encrypted, or the volume's encryption key is available in the clear on the hard disk.</span></span> <span data-ttu-id="ece63-117">如果已使用 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法停用金鑰保護裝置，或未使用下列方法指定金鑰保護裝置，則會在硬碟上以純文字方式使用加密金鑰：</span><span class="sxs-lookup"><span data-stu-id="ece63-117">The encryption key is available in the clear on the hard disk if key protectors have been disabled by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or if no key protectors have been specified by using the following methods:</span></span>
<ul>
<li><span data-ttu-id="ece63-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="ece63-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="ece63-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="ece63-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="ece63-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="ece63-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="ece63-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="ece63-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="ece63-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="ece63-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="ece63-127">針對 EHDD：</span><span class="sxs-lookup"><span data-stu-id="ece63-127">For an EHDD:</span></span><br/> <span data-ttu-id="ece63-128">磁片區的頻外永久解除鎖定、沒有金鑰管理員，或由協力廠商金鑰管理員管理。</span><span class="sxs-lookup"><span data-stu-id="ece63-128">The band for the volume is perpetually unlocked, has no key manager, or is managed by a third party key manager.</span></span><br/> <span data-ttu-id="ece63-129">這也可能表示該波段是由 BitLocker 管理，但已呼叫 <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> 方法，而磁片磁碟機已被擱置。</span><span class="sxs-lookup"><span data-stu-id="ece63-129">This can also mean that the band is managed by BitLocker but the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method has been called and the drive is suspended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <span data-ttu-id="ece63-130"><dt><strong>受保護</strong></dt>的 <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="ece63-130"><dt><strong>Protected</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="ece63-131">保護</span><span class="sxs-lookup"><span data-stu-id="ece63-131">PROTECTION ON</span></span><br/> <span data-ttu-id="ece63-132">針對標準 HDD：</span><span class="sxs-lookup"><span data-stu-id="ece63-132">For a standard HDD:</span></span><br/> <span data-ttu-id="ece63-133">磁片區已完全加密，而且磁片區的加密金鑰在硬碟上無法使用。</span><span class="sxs-lookup"><span data-stu-id="ece63-133">The volume is fully encrypted and the encryption key for the volume is not available in the clear on the hard disk.</span></span><br/> <span data-ttu-id="ece63-134">針對 EHDD：</span><span class="sxs-lookup"><span data-stu-id="ece63-134">For an EHDD:</span></span><br/> <span data-ttu-id="ece63-135">BitLocker 是此寬線的金鑰管理員。</span><span class="sxs-lookup"><span data-stu-id="ece63-135">BitLocker is the key manager for the band.</span></span> <span data-ttu-id="ece63-136">磁片磁碟機可以鎖定或解除鎖定，但無法永久解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="ece63-136">The drive can be locked or unlocked but cannot be perpetually unlocked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="ece63-137"><dt><strong>未知</strong></dt>的 <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="ece63-137"><dt><strong>Unknown</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="ece63-138">無法判斷磁片區保護狀態。</span><span class="sxs-lookup"><span data-stu-id="ece63-138">The volume protection status cannot be determined.</span></span> <span data-ttu-id="ece63-139">這可能是因為磁片區處於鎖定狀態。</span><span class="sxs-lookup"><span data-stu-id="ece63-139">This can be caused by the volume being in a locked state.</span></span><br/> <span data-ttu-id="ece63-140"><strong>Windows Vista 旗艦版、Windows Vista Enterprise 和 Windows Server 2008：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="ece63-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise and Windows Server 2008:</strong> This value is not supported.</span></span> <span data-ttu-id="ece63-141">從 Windows 7 和 Windows Server 2008 R2 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="ece63-141">This value is supported beginning with Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ece63-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="ece63-142">Return value</span></span>

<span data-ttu-id="ece63-143">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ece63-143">Type: **uint32**</span></span>

<span data-ttu-id="ece63-144">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ece63-144">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ece63-145">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ece63-145">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ece63-146">Description</span><span class="sxs-lookup"><span data-stu-id="ece63-146">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ece63-147"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ece63-147"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ece63-148">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="ece63-148">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ece63-149">備註</span><span class="sxs-lookup"><span data-stu-id="ece63-149">Remarks</span></span>

<span data-ttu-id="ece63-150">只有當您先呼叫 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) ，或使用下列其中一個方法時，才可以加密磁片區：</span><span class="sxs-lookup"><span data-stu-id="ece63-150">You can encrypt a volume only if you either call [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) first or use one of the following methods:</span></span>

-   [<span data-ttu-id="ece63-151">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="ece63-151">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-152">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="ece63-152">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-153">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="ece63-153">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-154">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="ece63-154">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-155">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="ece63-155">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-156">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="ece63-156">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-157">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="ece63-157">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="ece63-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="ece63-159">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="ece63-159">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="ece63-160">因此，如果磁片已加密，而且 *ProtectionStatus* 傳回零 (保護) ，則會停用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ece63-160">Therefore, if the disk is encrypted and *ProtectionStatus* returns zero (PROTECTION OFF), keys are disabled.</span></span>

<span data-ttu-id="ece63-161">使用 [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) 來列出已指定用來保護磁片區加密金鑰的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="ece63-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) to list the key protectors that have been specified to secure the volume's encryption key.</span></span> <span data-ttu-id="ece63-162">如果金鑰保護裝置存在但保護為零 (保護) ，請使用 [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) 來開啟磁片區保護。</span><span class="sxs-lookup"><span data-stu-id="ece63-162">If key protectors exist but protection is zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) to turn on volume protection.</span></span>

<span data-ttu-id="ece63-163">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ece63-163">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ece63-164">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ece63-164">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ece63-165">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ece63-165">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ece63-166">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="ece63-166">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ece63-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="ece63-167">Requirements</span></span>



| <span data-ttu-id="ece63-168">需求</span><span class="sxs-lookup"><span data-stu-id="ece63-168">Requirement</span></span> | <span data-ttu-id="ece63-169">值</span><span class="sxs-lookup"><span data-stu-id="ece63-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece63-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ece63-170">Minimum supported client</span></span><br/> | <span data-ttu-id="ece63-171">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ece63-171">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ece63-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ece63-172">Minimum supported server</span></span><br/> | <span data-ttu-id="ece63-173">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ece63-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ece63-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="ece63-174">Namespace</span></span><br/>                | <span data-ttu-id="ece63-175">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ece63-175">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ece63-176">MOF</span><span class="sxs-lookup"><span data-stu-id="ece63-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ece63-177"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="ece63-177"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ece63-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ece63-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece63-179">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="ece63-179">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
