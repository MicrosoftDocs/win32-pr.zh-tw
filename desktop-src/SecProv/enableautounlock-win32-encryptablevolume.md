---
description: 允許在掛接磁片區時自動解除鎖定資料磁片區。
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Win32_EncryptableVolume 類別的 EnableAutoUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849444"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7fe02-103">Win32 EncryptableVolume 類別的 EnableAutoUnlock 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7fe02-103">EnableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7fe02-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **EnableAutoUnlock** 方法可讓您在掛接磁片區時自動解除鎖定資料磁片區。</span><span class="sxs-lookup"><span data-stu-id="7fe02-104">The **EnableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class allows a data volume to be automatically unlocked when the volume is mounted.</span></span>

<span data-ttu-id="7fe02-105">自動解除鎖定可將外部金鑰儲存至作業系統，以將磁片區自動解除鎖定至目前執行中的作業系統磁片區。</span><span class="sxs-lookup"><span data-stu-id="7fe02-105">Automatic unlocking saves an external key to the operating system that can automatically unlock the volume onto the currently running operating system volume.</span></span>

<span data-ttu-id="7fe02-106">若要使用此方法，作業系統磁片區必須已受 BitLocker 磁碟機加密保護，或必須進行加密。</span><span class="sxs-lookup"><span data-stu-id="7fe02-106">To use this method, the operating system volume must already be protected by BitLocker Drive Encryption or must have encryption in progress.</span></span> <span data-ttu-id="7fe02-107">此外，資料磁片區必須已經存在外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="7fe02-107">In addition, there must already exist an external key for the data volume.</span></span> <span data-ttu-id="7fe02-108">使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 建立可自動解除鎖定磁片區的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="7fe02-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) to create the external key that can automatically unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe02-109">語法</span><span class="sxs-lookup"><span data-stu-id="7fe02-109">Syntax</span></span>


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="7fe02-110">參數</span><span class="sxs-lookup"><span data-stu-id="7fe02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe02-111">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7fe02-111">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe02-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7fe02-112">Type: **string**</span></span>

<span data-ttu-id="7fe02-113">字串，識別用來自動解除鎖定磁片區類型「外部金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="7fe02-113">A string that identifies the key protector of the type "External Key" used to automatically unlock the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe02-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fe02-114">Return value</span></span>

<span data-ttu-id="7fe02-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fe02-115">Type: **uint32**</span></span>

<span data-ttu-id="7fe02-116">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7fe02-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7fe02-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="7fe02-117">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="7fe02-118">Description</span><span class="sxs-lookup"><span data-stu-id="7fe02-118">Description</span></span>                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fe02-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="7fe02-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="7fe02-120">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="7fe02-121"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>          | <span data-ttu-id="7fe02-122">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="7fe02-122">The volume is locked.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="7fe02-123"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>          | <span data-ttu-id="7fe02-124">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="7fe02-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7fe02-125">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="7fe02-125">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                 |
| <dl> <span data-ttu-id="7fe02-126"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-126"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                   | <span data-ttu-id="7fe02-127">*VolumeKeyProtectorID* 參數未參考「外部金鑰」類型的有效金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="7fe02-127">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector of the type "External Key".</span></span><br/>                                                          |
| <dl> <span data-ttu-id="7fe02-128"><dt>**FVE \_E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-128"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>       | <span data-ttu-id="7fe02-129">無法針對目前正在執行的作業系統磁片區執行此方法。</span><span class="sxs-lookup"><span data-stu-id="7fe02-129">The method cannot be run for the currently running operating system volume.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="7fe02-130"><dt>**FVE \_E \_ OS \_ 未 \_ 受保護**</dt> <dt>2150694944 (0x80310020)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-130"><dt>**FVE\_E\_OS\_NOT\_PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt></span></span> </dl>      | <span data-ttu-id="7fe02-131">如果目前正在執行的作業系統磁片區未受 BitLocker 磁碟機加密保護，或沒有進行中的加密，則無法執行此方法。</span><span class="sxs-lookup"><span data-stu-id="7fe02-131">The method cannot be run if the currently running operating system volume is not protected by BitLocker Drive Encryption or does not have encryption in progress.</span></span><br/> |
| <dl> <span data-ttu-id="7fe02-132"><dt> **FVE \_ E \_ 磁片 \_ \_**</dt>區系結已在 <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-132"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY** </dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="7fe02-133">先前已啟用磁片區上的自動解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="7fe02-133">Automatic unlocking on the volume has previously been enabled.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="7fe02-134">備註</span><span class="sxs-lookup"><span data-stu-id="7fe02-134">Remarks</span></span>

<span data-ttu-id="7fe02-135">假設有一個類型為「外部金鑰」的有效磁片區金鑰保護裝置，則會從保護裝置解壓縮相關的256位外部金鑰，並將其儲存到目前執行中作業系統的登錄，以及磁片區金鑰保護裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fe02-135">Given a valid volume key protector of the type "External Key", the related 256-bit external key is extracted from the protector and stored into the registry of the currently running operating system, along with the volume key protector ID.</span></span>

<span data-ttu-id="7fe02-136">如果刪除與磁片區金鑰保護裝置識別碼相關聯的外部金鑰，則會停用或暫停自動解除鎖定磁片區的功能。</span><span class="sxs-lookup"><span data-stu-id="7fe02-136">If the external key associated with the volume key protector ID is deleted, the functionality to automatically unlock the volume is disabled or suspended.</span></span>

> [!Note]  
> <span data-ttu-id="7fe02-137">目前不支援卸載式媒體。</span><span class="sxs-lookup"><span data-stu-id="7fe02-137">Removable media is not currently supported.</span></span>

 

<span data-ttu-id="7fe02-138">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7fe02-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fe02-139">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7fe02-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7fe02-140">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="7fe02-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fe02-141">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="7fe02-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe02-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fe02-142">Requirements</span></span>



| <span data-ttu-id="7fe02-143">需求</span><span class="sxs-lookup"><span data-stu-id="7fe02-143">Requirement</span></span> | <span data-ttu-id="7fe02-144">值</span><span class="sxs-lookup"><span data-stu-id="7fe02-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe02-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fe02-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe02-146">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fe02-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7fe02-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fe02-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe02-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fe02-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fe02-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="7fe02-149">Namespace</span></span><br/>                | <span data-ttu-id="7fe02-150">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="7fe02-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7fe02-151">MOF</span><span class="sxs-lookup"><span data-stu-id="7fe02-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fe02-152"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fe02-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe02-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fe02-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe02-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="7fe02-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
