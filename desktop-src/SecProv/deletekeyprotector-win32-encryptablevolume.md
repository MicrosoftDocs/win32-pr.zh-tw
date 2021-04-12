---
description: 刪除磁片區的指定金鑰保護裝置。
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Win32_EncryptableVolume 類別的 DeleteKeyProtector 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318207"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4596f-103">Win32 EncryptableVolume 類別的 DeleteKeyProtector 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4596f-103">DeleteKeyProtector method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4596f-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **DeleteKeyProtector** 方法會刪除磁片區的指定金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4596f-104">The **DeleteKeyProtector** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes a given key protector for the volume.</span></span>

<span data-ttu-id="4596f-105">如果未加密的磁片區具有金鑰保護裝置，則當 **DeleteKeyProtector** 移除最後一個金鑰保護裝置時，磁片區會還原成標準 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="4596f-105">If an unencrypted volume has key protectors, when **DeleteKeyProtector** removes the last key protector, the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="4596f-106">如果磁片區從未經過加密，則刪除金鑰保護裝置將會還原為 NTFS。</span><span class="sxs-lookup"><span data-stu-id="4596f-106">If a volume has never been encrypted, deleting the key protector will revert to NTFS.</span></span>

<span data-ttu-id="4596f-107">如果磁片區尚未完整解密，請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再移除磁片區的最後一個金鑰保護裝置，以確保磁片區的加密部分仍然可供存取。</span><span class="sxs-lookup"><span data-stu-id="4596f-107">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing the volume's last key protector to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="4596f-108">語法</span><span class="sxs-lookup"><span data-stu-id="4596f-108">Syntax</span></span>


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="4596f-109">參數</span><span class="sxs-lookup"><span data-stu-id="4596f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4596f-110">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4596f-110">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4596f-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4596f-111">Type: **string**</span></span>

<span data-ttu-id="4596f-112">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="4596f-112">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4596f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4596f-113">Return value</span></span>

<span data-ttu-id="4596f-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4596f-114">Type: **uint32**</span></span>

<span data-ttu-id="4596f-115">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4596f-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4596f-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4596f-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="4596f-117">Description</span><span class="sxs-lookup"><span data-stu-id="4596f-117">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4596f-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4596f-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="4596f-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="4596f-119">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="4596f-120"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="4596f-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="4596f-121">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="4596f-121">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="4596f-122"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="4596f-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>         | <span data-ttu-id="4596f-123">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="4596f-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="4596f-124">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="4596f-124">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="4596f-125"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4596f-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                  | <span data-ttu-id="4596f-126">*VolumeKeyProtectorID* 參數未參考有效的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4596f-126">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="4596f-127"><dt>**FVE \_\_ \_ 需要 E 鍵**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="4596f-127"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="4596f-128">如果啟用金鑰保護裝置，則無法移除部分或完整加密磁片區的最後一個金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4596f-128">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="4596f-129">請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再移除此最後一個金鑰保護裝置，以確保磁片區的加密部分仍然可供存取。</span><span class="sxs-lookup"><span data-stu-id="4596f-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="4596f-130"><dt>**FVE \_E \_ 磁片 \_ \_**</dt>區系結已在 <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="4596f-130"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="4596f-131">無法刪除此金鑰保護裝置，因為它已用來自動解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="4596f-131">This key protector cannot be deleted because it is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="4596f-132">請先使用 [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) 停用自動解除鎖定，再刪除此金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4596f-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before deleting this key protector.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="4596f-133">備註</span><span class="sxs-lookup"><span data-stu-id="4596f-133">Remarks</span></span>

<span data-ttu-id="4596f-134">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4596f-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4596f-135">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4596f-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4596f-136">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4596f-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4596f-137">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="4596f-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4596f-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="4596f-138">Requirements</span></span>



| <span data-ttu-id="4596f-139">需求</span><span class="sxs-lookup"><span data-stu-id="4596f-139">Requirement</span></span> | <span data-ttu-id="4596f-140">值</span><span class="sxs-lookup"><span data-stu-id="4596f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4596f-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4596f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4596f-142">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4596f-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4596f-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4596f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4596f-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4596f-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4596f-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="4596f-145">Namespace</span></span><br/>                | <span data-ttu-id="4596f-146">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4596f-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4596f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4596f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4596f-148"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="4596f-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4596f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4596f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4596f-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="4596f-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
