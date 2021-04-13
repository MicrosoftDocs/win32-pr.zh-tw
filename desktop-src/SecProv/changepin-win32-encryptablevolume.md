---
description: 變更與加密磁片區相關聯的 PIN。
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Win32_EncryptableVolume 類別的 ChangePIN 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511160"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c10ac-103">Win32 EncryptableVolume 類別的 ChangePIN 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c10ac-103">ChangePIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c10ac-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ChangePIN** 方法會變更與加密磁片區相關聯的 PIN。</span><span class="sxs-lookup"><span data-stu-id="c10ac-104">The **ChangePIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes the PIN associated with an encrypted volume.</span></span> <span data-ttu-id="c10ac-105">如果啟用 [允許啟動的增強式 Pin] 群組原則，PIN 除了數位之外，還可以包含字母、符號和空格。</span><span class="sxs-lookup"><span data-stu-id="c10ac-105">If the "Allow enhanced PINs for startup" group policy is enabled, a PIN can contain letters, symbols, and spaces in addition to numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c10ac-106">語法</span><span class="sxs-lookup"><span data-stu-id="c10ac-106">Syntax</span></span>


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a><span data-ttu-id="c10ac-107">參數</span><span class="sxs-lookup"><span data-stu-id="c10ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c10ac-108">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c10ac-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c10ac-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c10ac-109">Type: **string**</span></span>

<span data-ttu-id="c10ac-110">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="c10ac-110">The unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="c10ac-111">*NewPIN* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c10ac-111">*NewPIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c10ac-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c10ac-112">Type: **string**</span></span>

<span data-ttu-id="c10ac-113">使用者指定的個人識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="c10ac-113">A user-specified personal identification string.</span></span> <span data-ttu-id="c10ac-114">如果啟用 [允許啟動的增強式 Pin] 群組原則、4到20個字母、符號、空格或數位，則此字串必須包含4到20位數的序列或。</span><span class="sxs-lookup"><span data-stu-id="c10ac-114">This string must consist of a sequence of 4 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c10ac-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c10ac-115">Return value</span></span>

<span data-ttu-id="c10ac-116">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c10ac-116">Type: **uint32**</span></span>

<span data-ttu-id="c10ac-117">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c10ac-117">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c10ac-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c10ac-118">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="c10ac-119">Description</span><span class="sxs-lookup"><span data-stu-id="c10ac-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c10ac-120"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="c10ac-121">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="c10ac-121">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c10ac-122"><dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-122"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="c10ac-123">在這部電腦上找到可開機的 CD/DVD。</span><span class="sxs-lookup"><span data-stu-id="c10ac-123">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="c10ac-124">移除 CD/DVD 並重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="c10ac-124">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="c10ac-125"><dt>**FVE \_E \_ 不正確 \_ PIN \_ 字元**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-125"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="c10ac-126">*NewPIN* 參數包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="c10ac-126">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="c10ac-127">當停用 [允許啟動的增強式 Pin] 群組原則時，只支援數位。</span><span class="sxs-lookup"><span data-stu-id="c10ac-127">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="c10ac-128"><dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-128"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>     | <span data-ttu-id="c10ac-129">*VolumeKeyProtectorID* 參數未參考類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c10ac-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="c10ac-130">您可以使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 或 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法來建立適當類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c10ac-130">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |
| <dl> <span data-ttu-id="c10ac-131"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-131"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="c10ac-132">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="c10ac-132">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="c10ac-133"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-133"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>               | <span data-ttu-id="c10ac-134">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="c10ac-134">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c10ac-135">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="c10ac-135">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="c10ac-136"><dt>**FVE \_E \_ 原則 \_ 不正確 \_ PIN \_ 長度**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-136"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="c10ac-137">提供的 *NewPIN* 參數長度超過20個字元、少於4個字元，或小於群組原則指定的最小長度。</span><span class="sxs-lookup"><span data-stu-id="c10ac-137">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="c10ac-138"><dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-138"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>        | <span data-ttu-id="c10ac-139">提供的金鑰保護裝置不存在於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="c10ac-139">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="c10ac-140"><dt>**Tb \_E \_ 服務 \_ 未 \_**</dt>執行 <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-140"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="c10ac-141">在這部電腦上找不到相容的可信賴平臺模組 (TPM) 。</span><span class="sxs-lookup"><span data-stu-id="c10ac-141">No compatible Trusted Platform Module (TPM) is found on this computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="c10ac-142">備註</span><span class="sxs-lookup"><span data-stu-id="c10ac-142">Remarks</span></span>

<span data-ttu-id="c10ac-143">**ChangePIN** 方法會根據現有的保護裝置資訊和新提供的 pin 來建立新的 TPM 和 pin 保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c10ac-143">The **ChangePIN** method creates a new TPM and PIN protector based on the existing protector information and the newly provided PIN.</span></span> <span data-ttu-id="c10ac-144">新的保護裝置將會有相同的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c10ac-144">The new protector will have the same GUID.</span></span> <span data-ttu-id="c10ac-145">您也可以呼叫 **ChangePIN** 方法來變更任何使用 pin 的金鑰保護裝置的 pin，例如 TPM 和 pin，或使用 PIN 和 USB 的 tpm。</span><span class="sxs-lookup"><span data-stu-id="c10ac-145">The **ChangePIN** method can also be called to change the PIN of any key protector that uses a PIN, for example, TPM and PIN or TPM with PIN and USB.</span></span>

<span data-ttu-id="c10ac-146">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c10ac-146">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c10ac-147">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c10ac-147">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c10ac-148">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c10ac-148">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c10ac-149">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="c10ac-149">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c10ac-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="c10ac-150">Requirements</span></span>



| <span data-ttu-id="c10ac-151">需求</span><span class="sxs-lookup"><span data-stu-id="c10ac-151">Requirement</span></span> | <span data-ttu-id="c10ac-152">值</span><span class="sxs-lookup"><span data-stu-id="c10ac-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c10ac-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c10ac-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c10ac-154">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c10ac-154">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c10ac-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c10ac-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c10ac-156">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c10ac-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c10ac-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="c10ac-157">Namespace</span></span><br/>                | <span data-ttu-id="c10ac-158">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c10ac-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c10ac-159">MOF</span><span class="sxs-lookup"><span data-stu-id="c10ac-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c10ac-160"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="c10ac-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c10ac-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c10ac-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c10ac-162">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="c10ac-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
